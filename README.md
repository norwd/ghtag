# tagme

GitHub Action to manage tags

## Usage

### Basic Setup

```yaml
---

name: "Tag new beta version on every push to main"
permissions:
  contents: write

on:
  push:
    branches:
      - main

jobs:
  tag:
    runs-on: ubuntu-latest
    steps:
      - uses: norwd/ghtag@main
        with:
          tag: v0.${{ github.run_id }}.0
```
