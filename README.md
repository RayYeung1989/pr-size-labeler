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
      - uses: your-username/pr-size-labeler@v1
```

## Size Labels

- `size/XS` - Less than 10 lines changed
- `size/S` - 10-49 lines changed
- `size/M` - 50-199 lines changed
- `size/L` - 200-499 lines changed
- `size/XL` - 500+ lines changed
