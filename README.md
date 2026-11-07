<div align="center">

# Tokei

**Count lines of code, comments and blank lines by language.**

[![tokei](https://snapcraft.io/tokei/badge.svg)](https://snapcraft.io/tokei)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64, arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Tokei](https://github.com/XAMPPRocky/tokei), a fast code counter that reports files, code, comments and blank lines per language.

</div>

---

## Getting Started

<a href="https://snapcraft.io/tokei"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install tokei
tokei ./my-project
```

Use `tokei --files` for per-file results, `--sort code` to order languages, and `--output json`, `yaml` or `cbor` for machine-readable output.

## Configure

There are no `snap set` options. Tokei reads `tokei.toml` or `.tokeirc` from the project directory, and a global `tokei.toml` from `~/snap/tokei/current/.config`. Exclude paths with a `.tokeignore` file.

For projects on removable storage:

```bash
sudo snap connect tokei:removable-media
```

## Limitations

- Projects must be in a normal folder under your home directory or on connected removable storage. Hidden folders directly under your home directory and system paths are not accessible.
- A global configuration in the host's `~/.config` is not read; place it under `~/snap/tokei/current/.config`.

## Build

```bash
git clone https://github.com/sidalit/tokei-snap.git
cd tokei-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/tokei-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/XAMPPRocky/tokei/issues).

## License

Snap packaging: [MIT](LICENSE).
