# gha-pr-approved
Composite GitHub action that checks from GitHub API whether the pull request
has enough approving reviews. Will either return truth value or fail on request.

Requires the pull-requests read permission to your workflow:

```yaml
permissions:
  pull-requests: read
```
