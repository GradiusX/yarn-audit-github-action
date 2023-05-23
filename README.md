# Yarn Audit Github Action

## Example usage

```yaml
name: Security Checker
run-name: Running Security Checker 🚀
on:
  push:
    branches: [main]
jobs:
  Run-Yarn-Audit:
    runs-on: ubuntu-latest
    steps:
      - name: Check out repository code
        uses: actions/checkout@v3
      - run: echo "💡 The ${{ github.repository }} repository has been cloned to the runner."
      - run: echo "🖥️ The workflow is now ready to test your code on the runner."
      - name: Running Yarn Audit on Repo
        id: yarn_audit
        uses: GradiusX/yarn-audit-github-action@v1.5
        with:
          # Report only this level and above (info|low|moderate|high|critical)
          severity-level: 'critical'
```