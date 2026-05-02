---
name: github-readiness-maintenance
description: Use when preparing this planning repository for GitHub, checking Markdown links, removing local machine paths, updating README navigation, validating .agents registry paths, and preventing local metadata noise.
triggers:
  - github
  - relative links
  - repo hygiene
  - link check
  - ready to push
outputs:
  - relative links
  - validated Markdown navigation
  - registry path validation
  - git hygiene notes
version: 0.1.0
---

# GitHub Readiness Maintenance

## Process

1. Search Markdown for local absolute paths such as `/Users/`.
2. Convert links to GitHub-compatible relative links.
3. Validate all Markdown links.
4. Validate `.agents/registry.yaml` paths.
5. Ensure `.gitignore` excludes local metadata such as `.DS_Store`.
6. Check `git status --short` and summarize untracked or modified files.

## Useful Commands

```sh
rg -n '/Users|construction-operational-plan/' . -g '*.md'
```

```sh
ruby - <<'RUBY'
files = Dir['**/*.md', '.agents/**/*.md']
missing = []
files.each do |file|
  text = File.read(file)
  text.scan(/\[[^\]]+\]\(([^)]+)\)/).flatten.each do |url|
    next if url =~ /\A[a-z]+:\/\//
    next if url.start_with?('#', 'mailto:')
    path = url.split('#', 2).first.gsub('%20', ' ')
    next if path.empty?
    target = path.start_with?('/') ? File.expand_path('.' + path, Dir.pwd) : File.expand_path(path, File.dirname(File.expand_path(file)))
    missing << [file, url, target.sub(Dir.pwd + '/', '')] unless File.exist?(target)
  end
end
if missing.empty?
  puts 'markdown links ok'
else
  missing.each { |file, url, target| puts "#{file}: missing #{url} -> #{target}" }
  exit 1
end
RUBY
```

```sh
ruby -e 'require "yaml"; y=YAML.load_file(".agents/registry.yaml"); missing=[]; (y["canonical_files"]||{}).each{|k,p| missing << "#{k}: #{p}" unless File.exist?(p)}; (y["skills"]||[]).each{|s| missing << "skill #{s["name"]}: #{s["path"]}" unless File.exist?(s["path"])}; (y["prompts"]||{}).each{|k,p| missing << "prompt #{k}: #{p}" unless File.exist?(p)}; (y["templates"]||{}).each{|k,p| missing << "template #{k}: #{p}" unless File.exist?(p)}; if missing.empty?; puts "registry paths ok"; else puts missing; exit 1; end'
```

## Guardrails

- Use relative links in Markdown so GitHub navigation works.
- Do not link to local absolute filesystem paths.
- Keep `.agents/registry.yaml` path strings repo-relative.

