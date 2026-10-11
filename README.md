# gg alpha binaries

Prebuilt alpha releases of gg for macOS, Linux, and Windows. The source repository
is private. Each [release](https://github.com/dawiddutoit/gg-releases/releases)
contains native archives and `checksums.txt`.

## Install

On macOS or Linux with Homebrew:

```sh
brew install dawiddutoit/gg/gg
brew update && brew upgrade dawiddutoit/gg/gg
```

With [mise](https://mise.jdx.dev/) on macOS, Linux, or Windows:

```toml
[tools]
"github:dawiddutoit/gg-releases" = { version = "latest", prerelease = true }
```

Run `mise install` to install and `mise upgrade` to follow later alphas. Pin
`version = "0.1.0-alpha.1"` when a project needs a fixed build.

The first release targets Apple Silicon and Intel Macs, Linux arm64 and x64
with glibc 2.35 or newer, and Windows x64. Native Windows currently runs
without gg's private local action journal. `gg --version` prints the exact
version and source commit used for the build.

For this alpha, use Git directly to remove a worktree if its contents may
change while a gg removal confirmation is open. gg has a known race in that
confirmation path, and a fix is planned for a later alpha.
