<div align="center">

# snolc-modules

official native modules for [snolc](https://github.com/owenewans/snolc).

[![ci](https://github.com/owenewans/snolc-modules/actions/workflows/ci.yml/badge.svg?branch=dev)](https://github.com/owenewans/snolc-modules/actions/workflows/ci.yml)
[![scorecard](https://api.securityscorecards.dev/projects/github.com/owenewans/snolc-modules/badge)](https://securityscorecards.dev/viewer/?uri=github.com/owenewans/snolc-modules)
[![last commit](https://img.shields.io/github/last-commit/owenewans/snolc-modules?logo=github)](https://github.com/owenewans/snolc-modules/commits/dev)
[![license](https://img.shields.io/github/license/owenewans/snolc-modules)](LICENSE)

<a href="https://count.owenewans.org/owenewans/snolc-modules?theme=moebooru-h&notitle"><img src="https://count.owenewans.org/owenewans/snolc-modules?theme=moebooru-h&notitle" alt="repository views"></a>

`rust` `networking` `plugins`

</div>

## modules

| package | class | role |
| --- | --- | --- |
| `adapter-socks5` | adapter | client |
| `adapter-http-connect` | adapter | client |
| `adapter-tun` | adapter | client |
| `adapter-direct` | adapter | server |
| `protection-noise` | protection | client, server |
| `protection-dummy` | protection | client, server |
| `carrier-tcp` | carrier | client, server |
| `carrier-ssh` | carrier | client, server |
| `policy-local` | policy | client, server |
| `policy-dummy` | policy | client, server |

## build

Rust 1.98.1 and `Cargo.lock` define the build.

```sh
cargo build --workspace --locked
cargo test --workspace --locked
cargo clippy --workspace --all-targets --locked -- -D warnings
```

The workspace pins `snolc-sdk` and the test engine to one `snolc` commit. Native
E2E tests load all ten libraries and exercise TCP, UDP, Noise, SSH, policy-local
and TUN packet paths.

## packages

`config/templates/modules` contains strict role templates. `snolpkg` contains
signed publication manifests for release artifacts from this repository.

## changes

Push changes to a branch and open a pull request. The protected `master` branch
rejects direct pushes.

## license

[Unlicense](LICENSE)
