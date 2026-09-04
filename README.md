# homebrew-anarlog

Homebrew tap for the `anarlog` CLI, built from [dave-atx/anarlog](https://github.com/dave-atx/anarlog).

```sh
brew install dave-atx/anarlog/anarlog-cli
```

Supports macOS (arm64 and x86_64) and Linux (arm64 and x86_64).

## What this is

`anarlog` is the command-line interface and MCP server for [Anarlog](https://github.com/fastrepl/anarlog), a local-first meeting notetaker. It reads meetings, notes, and transcripts out of the local SQLite database, and `anarlog mcp` exposes them to coding agents over stdio.

The CLI source is **unmodified upstream MIT code**. This tap exists because upstream ships the CLI only bundled inside the macOS app — there are no standalone binaries, and nothing at all for Linux. These builds fill that gap.

The macOS app already installs its own copy of the CLI, so this tap is mainly useful on Linux or if you want the CLI without the desktop app.

## Notes

- Linux binaries are built on Ubuntu 22.04, giving a glibc 2.35 floor. They run on Ubuntu 22.04+, Debian 12+, and RHEL 9+. Older distributions need to build from source.
- The formula is generated automatically by the `fork-release` workflow in the main repo. Do not edit `Formula/anarlog-cli.rb` by hand; changes will be overwritten on the next release.
- Formula versions track the upstream Anarlog app version they were built from. The formula is only republished when the CLI binary actually changes, so it will lag the app version.

## Related

- [dave-atx/anarlog](https://github.com/dave-atx/anarlog) — the fork these binaries are built from ([FORK.md](https://github.com/dave-atx/anarlog/blob/fork/FORK.md))
- [fastrepl/anarlog](https://github.com/fastrepl/anarlog) — the upstream project
