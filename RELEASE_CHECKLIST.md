# Release Checklist

Before publishing to GitHub:

- [ ] Replace `YOUR-USER` in `README.md` with the GitHub owner or organization.
- [ ] Confirm the copyright holder in `LICENSE`.
- [ ] Review `references/handbook.md` for any private names, paths, unpublished project details, or lab-only material.
- [ ] Confirm that the handbook can be released under MIT.
- [ ] Run a local sensitive-string scan.
- [ ] Create a clean git repository.
- [ ] Add a short GitHub repository description, for example:
  - `Codex skill for evidence-first experimental CS research coaching.`
- [ ] Add topics:
  - `codex-skill`
  - `research-assistant`
  - `computer-science`
  - `research-workflow`
  - `ai-tools`

Suggested local check:

```bash
rg -n "api[_-]?key|token|secret|password|/Users|private|confidential|未公开|内部" .
```

Suggested initial release commands:

```bash
git init
git add .
git commit -m "Initial open-source release"
git branch -M main
git remote add origin git@github.com:YOUR-USER/research-assistant-skill.git
git push -u origin main
```
