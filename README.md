# inngest/setup-inngest

This action installs the Inngest CLI ([inngest/inngest](https://github.com/inngest/inngest))

## Usage

```yaml
steps:
  - uses: actions/checkout@v3
  - uses: inngest/setup-inngest@v1
    with:
      version: 0.5.2
```

The `version` input is optional. If not supplied, the latest version will be used.
