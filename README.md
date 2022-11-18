# gha-pr-approved

Pull request approving review count check GitHub composite action, used by Minerva as of Nov 2022.

Composite GitHub action that checks from GitHub API whether the pull request
has enough approving reviews. Will either return truth value or fail on request.

Requires the pull-requests read permission to your workflow:

```yaml
permissions:
  pull-requests: read
```

# usage

```yaml
  - uses: FinnishRail/gha-pr-approved@v1
    with:
      pr-number: 123
      fail: false
```