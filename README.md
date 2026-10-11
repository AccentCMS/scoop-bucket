# Accent CMS Scoop bucket

[![Tests](https://github.com/AccentCMS/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/AccentCMS/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/AccentCMS/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/AccentCMS/scoop-bucket/actions/workflows/excavator.yml)

The [Scoop](https://scoop.sh) bucket for [Accent CMS](https://accentcms.dev),
the single-binary markdown CMS and static site generator. It installs the
release binaries from
[AccentCMS/accent](https://github.com/AccentCMS/accent/releases) on Windows
x64 and ARM64.

## Install

```pwsh
scoop bucket add accent https://github.com/AccentCMS/scoop-bucket
scoop install accent
accent --version
```

## Update

```pwsh
scoop update accent
```

Use one installer. If Accent CMS is also installed with WinGet or the install
script, one copy shadows the other on `PATH`.

## How the manifest stays current

`bucket/accent.json` takes each archive's SHA-256 from the release's
`checksums-vX.Y.Z.txt`, the file that is signed with the Accent CMS release
key. After each release, this bucket's Excavator workflow updates the version
and the hashes the same way.

Report a problem with the package in
[AccentCMS/accent](https://github.com/AccentCMS/accent/issues).
