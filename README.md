# github-workflows

Collection of Github workflow jobs

View the various workflow jobs under .github/workflows/

## How to use

In your repos .github/workflows folder add a .yml file and under the jobs section add a workflow from here.

```yaml
jobs:
  markdown-lint:
    uses: chef/github-workflows/.github/workflows/markdownlint.yml@main
```

- Various linters have configuration files that can be added to the root of your repo to adjust behaviour as desired
- Some workflows need input, please review the workflow to understand what input is required

```yaml
jobs:
  terraformplan:
    uses: chef/github-workflows/.github/workflows/terraform-plan.yml@main
    secrets: inherit
```

```yaml
jobs:
  supermarket-deploy:
    uses: chef/github-workflows/.github/workflows/cookbook-supermarket-deploy.yml@main
    secrets: inherit
    with:
      SUPERMARKET_USER: "chef"
      SUPERMARKET_URL: "https://supermarket.chef.io"
```
