# inngest/setup-inngest

This action installs the Inngest CLI ([inngest/inngest](https://github.com/inngest/inngest)) on your Linux, Mac, or Windows runner in GitHub Actions.

You probably want to use a more specific action that uses this internally - see:

- [inngest/action-deploy-functions](https://github.com/inngest/action-deploy-functions)
- [inngest/action-test-functions](https://github.com/inngest/action-test-functions)

## Usage

```yaml
steps:
  - uses: actions/checkout@v3
  - uses: inngest/setup-inngest@v1
    with:
      version: 0.5.2
      key: ${{ secrets.INNGEST_API_KEY }}
```

The `version` input is optional. If not supplied, the `"latest"` version will be used.

The `key` input is also optional. If supplied, we'll log in to the CLI for you (synonymous with using `inngest login --token [key]`). This is useful if you wish to perform authenticated commands with the CLI, like [deploying functions](https://github.com/inngest/action-deploy-functions) or [testing against production data](https://github.com/inngest/action-test-functions).
