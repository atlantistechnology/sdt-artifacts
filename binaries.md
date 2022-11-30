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

<ul>
<li>aix
<ul>
<li>ppc64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/aix/ppc64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>android   * amd64     * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/gotree">gotree</a>    * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/jsonformat">jsonformat</a>
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/amd64/treesit">treesit</a></li>
<li>arm64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/android/arm64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>darwin   * amd64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/amd64/treesit">treesit</a></li>
<li>arm64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/darwin/arm64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>dragonfly
<ul>
<li>amd64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/dragonfly/amd64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>freebsd   * 386
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/386/treesit">treesit</a>   * amd64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/amd64/treesit">treesit</a>   * arm</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm/treesit">treesit</a></li>
<li>arm64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/freebsd/arm64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>illumos
<ul>
<li>amd64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/illumos/amd64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>js
<ul>
<li>wasm
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/js/wasm/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>linux   * 386
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/386/treesit">treesit</a>   * amd64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/amd64/treesit">treesit</a>   * arm</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm/treesit">treesit</a>   * arm64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/arm64/treesit">treesit</a>   * mips</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips/treesit">treesit</a>   * mips64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64/treesit">treesit</a>   * mips64le</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mips64le/treesit">treesit</a>   * mipsle</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/mipsle/treesit">treesit</a>   * ppc64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64/treesit">treesit</a>   * ppc64le</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/ppc64le/treesit">treesit</a>   * riscv64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/riscv64/treesit">treesit</a></li>
<li>s390x
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/linux/s390x/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>netbsd   * 386
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/386/treesit">treesit</a>   * amd64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/amd64/treesit">treesit</a>   * arm</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm/treesit">treesit</a></li>
<li>arm64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/netbsd/arm64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>openbsd   * 386
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/386/treesit">treesit</a>   * amd64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/amd64/treesit">treesit</a>   * arm</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm/treesit">treesit</a>   * arm64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/arm64/treesit">treesit</a></li>
<li>mips64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/openbsd/mips64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>plan9   * 386
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/386/treesit">treesit</a>   * amd64</li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/sdt">sdt</a>   * <a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/amd64/treesit">treesit</a></li>
<li>arm
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/plan9/arm/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>solaris
<ul>
<li>amd64
<ul>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/gotree">gotree</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/jsonformat">jsonformat</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/sdt">sdt</a></li>
<li><a href="https://github.com/atlantistechnology/sdt-artifacts/blob/main/solaris/amd64/treesit">treesit</a></li>
</ul></li>
</ul></li>
<li>windows
<ul>
<li>386
<ul>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/gotree.exe">gotree.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/jsonformat.exe">jsonformat.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/sdt.exe">sdt.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/386/treesit.exe">treesit.exe</a></li>
</ul></li>
<li>amd64
<ul>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/gotree.exe">gotree.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/jsonformat.exe">jsonformat.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/sdt.exe">sdt.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/amd64/treesit.exe">treesit.exe</a></li>
</ul></li>
<li>arm
<ul>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/gotree.exe">gotree.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/jsonformat.exe">jsonformat.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/sdt.exe">sdt.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm/treesit.exe">treesit.exe</a></li>
</ul></li>
<li>arm64
<ul>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/gotree.exe">gotree.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/jsonformat.exe">jsonformat.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/sdt.exe">sdt.exe</a></li>
<li><a href="https:github.com/atlantistechnology/sdt-artifacts/blob/main/windows/arm64/treesit.exe">treesit.exe</a></li>
</ul></li>
</ul></li>
</ul>
