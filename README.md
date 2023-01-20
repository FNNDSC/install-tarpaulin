# Install Tarpaulin in Github Actions

Downloads `cargo-tarpaulin` from
[quickinstall](https://github.com/cargo-bins/cargo-quickinstall).

## Example

```yaml
name: CI

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup rust toolchain
        uses: actions-rs/toolchain@v1
        with:
          toolchain: stable
          profile: minimal
      - name: Install tarpaulin
        uses: FNNDSC/quickinstall-tarpaulin@master
        with:
          version: "0.23.1"
```
