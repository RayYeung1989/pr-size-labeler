# PR Size Labeler

A GitHub Action that automatically labels pull requests based on their size.

## Usage

Create a workflow file (e.g., `.github/workflows/pr-size-labeler.yml`):

```yaml
name: PR Size Labeler

on:
  pull_request:
    types: [opened, synchronize, reopened]

jobs:
  label:
    runs-on: ubuntu-latest
    steps:
      - uses: RayYeung1989/pr-size-labeler@v1.0.0
```

## Size Labels

| Label | Lines Changed |
|-------|---------------|
| `size/XS` | < 10 lines |
| `size/S` | 10-49 lines |
| `size/M` | 50-199 lines |
| `size/L` | 200-499 lines |
| `size/XL` | 500+ lines |

## Why Use It?

- Keep your PRs small and reviewable
- Identify large PRs that need extra attention
- Automate labeling workflow

## License

MIT
