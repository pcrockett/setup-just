# setup-just action

easy way to install [just](https://just.systems/) in your GitHub Actions
workflows.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0  # v7.0.0
      - uses: pcrockett/setup-just@LATEST_RELEASE_TAG
```

if you don't want to use the default version of just that comes with this action, you
can specify your own version and checksum:

```yaml
- uses: pcrockett/setup-just@LATEST_RELEASE_TAG
  with:
    version: '1.55.1'
    checksum: 'b0ef600f0df20d5ae91ae931627c499fc52b477ffe5f5ea7b7b3ec616b16c778'
```

**recommended:** run [pinact](https://github.com/suzuki-shunsuke/pinact) to pin your
actions to a specific release. don't worry, if you're using Dependabot, Renovate, etc.,
they will update your pins correctly for you.

```bash
pinact run --update
```
