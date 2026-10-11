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
"github:dawiddutoit/gg-releases" = { version = "latest", prerelease = true, minimum_release_age = "0s" }
```

Run `mise install` to install and `mise upgrade` to follow later alphas. The
tool-specific release age option allows immediate updates; mise otherwise holds
new GitHub releases for 24 hours. Pin
`version = "0.1.0-alpha.2"` when a project needs a fixed build.

The first release targets Apple Silicon and Intel Macs, Linux arm64 and x64
with glibc 2.35 or newer, and Windows x64. Native Windows currently runs
without gg's private local action journal. `gg --version` prints the exact
version and source commit used for the build.

`alpha.2` asks for a new review when the selected worktree or its observed
removal risk changes after a confirmation opens. As with Git itself, avoid
changing a worktree concurrently with its removal.
