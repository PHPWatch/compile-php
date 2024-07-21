# Compile PHP - GitHub Actions

This GitHub action downloads the latest PHP source (php/php-src),
configures it to enable all extensions, compiles it, and installs it.

## Usage

```yaml
name: Tests
permissions: read-all
on:
  pull_request:
  push:

jobs:
  run:
    runs-on: ubuntu-latest
    name: Compile and install PHP - Test
    steps:
      - name: Setup PHP
        uses: PHPWatch/compile-php

      - name: Display versions and env
        run: |
          php -v
          php -m


```
