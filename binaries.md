# Downloadable binaries for Semantic Diff Tool

---
title: Executable binaries fo SDT and support utilities
date: November 30, 2022
---

For each of these tools, simply download each one to your PATH, as
appropriate to your operating system and CPU architecture.

For example, on a Linux x86-64 system, you might do this:

```
% sudo curl https://sdt.dev/linux/amd64/sdt > /usr/local/bin/sdt
% sudo chmod a+x /usr/local/bin/sdt
```

See the main documentation for discussion of the additional capabilities
provided by the supporting executables.  Note that this archive simply
maintains the latest(ish) version of each executable.  To build a specific
older version for your platform, clone the appropriate release branch of 

<pre>
├── aix
│   └── ppc64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/treesit)
├── android
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/treesit)
│   └── arm64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/treesit)
├── darwin
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/treesit)
│   └── arm64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/treesit)
├── dragonfly
│   └── amd64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/treesit)
├── freebsd
│   ├── 386
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/treesit)
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/treesit)
│   ├── arm
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/treesit)
│   └── arm64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/treesit)
├── illumos
│   └── amd64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/treesit)
├── js
│   └── wasm
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/treesit)
├── linux
│   ├── 386
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/treesit)
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/treesit)
│   ├── arm
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/treesit)
│   ├── arm64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/treesit)
│   ├── mips
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/treesit)
│   ├── mips64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/treesit)
│   ├── mips64le
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/treesit)
│   ├── mipsle
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/treesit)
│   ├── ppc64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/treesit)
│   ├── ppc64le
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/treesit)
│   ├── riscv64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/treesit)
│   └── s390x
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/treesit)
├── netbsd
│   ├── 386
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/treesit)
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/treesit)
│   ├── arm
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/treesit)
│   └── arm64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/treesit)
├── openbsd
│   ├── 386
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/treesit)
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/treesit)
│   ├── arm
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/treesit)
│   ├── arm64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/treesit)
│   └── mips64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/treesit)
├── plan9
│   ├── 386
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/treesit)
│   ├── amd64
│   │   ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/gotree)
│   │   ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/jsonformat)
│   │   ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/sdt)
│   │   └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/treesit)
│   └── arm
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/treesit)
├── solaris
│   └── amd64
│       ├── [gotree](https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/gotree)
│       ├── [jsonformat](https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/jsonformat)
│       ├── [sdt](https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/sdt)
│       └── [treesit](https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/treesit)
└── windows
    ├── 386
    │   ├── [gotree.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/gotree.exe)
    │   ├── [jsonformat.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/jsonformat.exe)
    │   ├── [sdt.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/sdt.exe)
    │   └── [treesit.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/treesit.exe)
    ├── amd64
    │   ├── [gotree.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/gotree.exe)
    │   ├── [jsonformat.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/jsonformat.exe)
    │   ├── [sdt.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/sdt.exe)
    │   └── [treesit.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/treesit.exe)
    ├── arm
    │   ├── [gotree.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/gotree.exe)
    │   ├── [jsonformat.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/jsonformat.exe)
    │   ├── [sdt.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/sdt.exe)
    │   └── [treesit.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/treesit.exe)
    └── arm64
        ├── [gotree.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/gotree.exe)
        ├── [jsonformat.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/jsonformat.exe)
        ├── [sdt.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/sdt.exe)
        └── [treesit.exe](https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/treesit.exe)
</pre>
