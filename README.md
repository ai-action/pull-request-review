# pull-request-review

[![version](https://badgen.net/github/release/ai-action/pull-request-review)](https://github.com/ai-action/pull-request-review/releases)
[![test](https://github.com/ai-action/pull-request-review/actions/workflows/test.yml/badge.svg)](https://github.com/ai-action/pull-request-review/actions/workflows/test.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

👀 Review pull request code with AI.

## Quick Start

```yaml
# .github/workflows/pr-review.yml
on: pull_request
jobs:
  pr-review:
    runs-on: ubuntu-latest
    steps:
      - name: PR review
        uses: ai-action/pull-request-review@v1
```

## Usage

Add an AI code review comment to the pull request:

```yaml
- uses: ai-action/pull-request-review@v1
```

See [action.yml](action.yml)

## Inputs

### `model`

**Optional**: The language [model](https://ollama.com/library) to use. Defaults to [codellama](https://ollama.com/library/codellama):

```yaml
- uses: ai-action/pull-request-review@v1
  with:
    model: codellama
```

### `prompt`

**Optional**: The input prompt that comes before the PR diff. Defaults to:

```yaml
- uses: ai-action/pull-request-review@v1
  with:
    prompt: 'Code review the diff:'
```

### `comment-header`

**Optional**: The PR comment title in Markdown. Defaults to:

```yaml
- uses: ai-action/pull-request-review@v1
  with:
    comment-header: '# Pull Request Review'
```

### `token`

**Optional**: The GitHub token. Defaults to `GITHUB_TOKEN`:

```yaml
- uses: ai-action/pull-request-review@v1
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```

## License

[MIT](LICENSE)
