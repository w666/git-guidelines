# git-guidelines

## Commit Messages

- Add issue number followed by colon `:`
  - For GitHIb and GitLab issue numbers use square brackets `[#123]:`
  - For Jira issues brackets are not needed `PROJ-123:`
- Use the imperative, present tense: "Change" not "Changed" nor "Changes"
- Do capitalize the first letter
- Do not end the first line with a period `.`

## Branch Names

Branch names must all lowercase and follow the pattern

```bash
${BRANCH_TYPE}-${ISSUE_NUMBER}-${SHORT_DESCRIPTION}
```

for example `fix-123-handle-null-pointer`

### Branch Types

- `feature` or `feat`: when contains new feature or code refactoring
- `documentation` or `doc`: any documentation chages
- `test`: when adding tests
- `fix`: for bug fixes

## Commands

TODO
