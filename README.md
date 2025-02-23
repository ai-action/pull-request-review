# pull-request-review

[![version](https://badgen.net/github/release/ai-action/pull-request-review)](https://github.com/ai-action/pull-request-review/releases)
[![test](https://github.com/ai-action/pull-request-review/actions/workflows/test.yml/badge.svg)](https://github.com/ai-action/pull-request-review/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

👀 Review pull request code with AI.

## Quick Start

```yaml
# .github/workflows/pr-review.yml
on: push
jobs:
  pr-review:
    runs-on: ubuntu-latest
    steps:
      - name: PR review
        uses: ai-action/pull-request-review@v1
```

## Usage

```yaml
- uses: ai-action/pull-request-review@v1
```

See [action.yml](action.yml)

## Inputs

### `version`

**Optional**: The version. Defaults to `1.2.3`:

```yaml
- uses: ai-action/pull-request-review@v1
  with:
    version: 1.2.3
```

## License

[MIT](LICENSE)
