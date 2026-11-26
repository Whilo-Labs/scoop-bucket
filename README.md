# Whilo Labs Scoop bucket

[![Excavator](https://github.com/Whilo-Labs/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/Whilo-Labs/scoop-bucket/actions/workflows/excavator.yml)

A [Scoop](https://scoop.sh) bucket for the open-source apps of Whilo Labs.

## Install

```pwsh
scoop bucket add whilo-labs https://github.com/Whilo-Labs/scoop-bucket
scoop install whilo-labs/whilo-trace
```

## Apps

| App | What it is | What you get |
|---|---|---|
| [whilo-trace](https://github.com/Whilo-Labs/whilo-trace) | Network path monitor: per-hop packet loss and latency for several hosts at once | The desktop app in the Start menu as "Whilo Trace" and the command line as `whilo-trace-cli` |

The manifest installs the portable zip from the [Whilo Trace releases](https://github.com/Whilo-Labs/whilo-trace/releases) (Windows x64).

## Update and uninstall

```pwsh
scoop update
scoop update whilo-trace
scoop uninstall whilo-trace
```

Whilo Trace keeps its history in `%LOCALAPPDATA%\Whilo Trace`, one file shared by the app and the command line. That folder is not in the Scoop folder, so `scoop uninstall` leaves it in place.

## How the manifest is updated

A scheduled workflow, [Excavator](.github/workflows/excavator.yml), checks for a new Whilo Trace release every 4 hours and updates the manifest.

## Problems

A problem with the app itself: [Whilo Trace issues](https://github.com/Whilo-Labs/whilo-trace/issues). A problem with installing or updating it through Scoop: the issues of this repository.

## License

The manifests in this repository are released under [the Unlicense](LICENSE). Each app keeps its own license.
