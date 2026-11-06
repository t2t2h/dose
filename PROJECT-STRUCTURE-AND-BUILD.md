# Unified project structure

This repository contains one Theos target: `AflatoonMubdi.dylib`. All source modules, headers, the embedded background image, Makefile, and GitHub Actions workflow are included in the same project root.

The former VPN / WireGuard / Packet Tunnel components and their menu controls have been removed. The only subdirectory required for automation is `.github/workflows/`.

`Makefile` explicitly includes every compiled source, including `Image.c` for the embedded menu background. The workflow checks the Makefile source list and required headers before compiling.
