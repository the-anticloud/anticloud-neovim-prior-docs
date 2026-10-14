# NEOVIM PRIOR DOCS

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-software_development-lightgrey)

> Anticloud-hardened packaging of the upstream project `NEOVIM_PRIOR_DOCS` in category **SOFTWARE DEVELOPMENT**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SOFTWARE DEVELOPMENT · **Upstream:** https://github.com/neovim/neovim · **Upstream pin:** `09e4491a5351e37cea4ed83b163de315fedc2eaa` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<h1 align="center">
  <img src="https://raw.githubusercontent.com/neovim/neovim.github.io/master/static/logos/neovim-logo-300x87.png" alt="Neovim">

  <a href="https://neovim.io/doc/">Documentation</a> |
  <a href="https://app.element.io/#/room/#neovim:matrix.org">Chat</a>
</h1>

[![Coverity Scan analysis](https://scan.coverity.com/projects/2227/badge.svg)](https://scan.coverity.com/projects/2227)
[![Packages](https://repology.org/badge/tiny-projects/neovim.svg)](https://repology.org/metapackage/neovim)
[![Debian CI](https://badges.debian.net/badges/debian/testing/neovim/version.svg)](https://buildd.debian.org/neovim)
[![Downloads](https://img.shields.io/github/downloads/neovim/neovim/total.svg?maxAge=2592001)](https://github.com/neovim/neovim/releases/)

Neovim is a project that seeks to aggressively refactor [Vim](https://www.vim.org/) in order to:

- Simplify maintenance and encourage [contributions](CONTRIBUTING.md)
- Split the work between multiple developers
- Enable [advanced UIs] without modifications to the core
- Maximize [extensibility](https://neovim.io/doc/user/api-ui-events.html#api-ui-events)

See the [Introduction](https://github.com/neovim/neovim/wiki/Introduction) wiki page and [Roadmap]
for more information.

Features
--------

- Modern [GUIs](https://github.com/neovim/neovim/wiki/Related-projects#gui)
- [API access](https://github.com/neovim/neovim/wiki/Related-projects#api-clients)
  from any language including C/C++, C#, Clojure, D, Elixir, Go, Haskell, Java/Kotlin,
  JavaScript/Node.js, Julia, Lisp, Lua, Perl, Python, Racket, Ruby, Rust
- Embedded, scriptable [terminal emulator](https://neovim.io/doc/user/terminal.html)
- Asynchronous [job control](https://github.com/neovim/neovim/pull/2247)
- [Shared data (shada)](https://github.com/neovim/neovim/pull/2506) among multiple editor instances
- [XDG base directories](https://github.com/neovim/neovim/pull/3470) support
- Compatible with most Vim plugins, including Ruby and Python plugins

See [`:help nvim-features`][nvim-features] for the full list, and [`:help news`][nvim-news] for noteworthy changes in the latest version!

Install from package
--------------------

Pre-built packages for Windows, macOS, and Linux are found on the
[Releases](https://github.com/neovim/neovim/releases/) page.

[Managed packages] are in [Homebrew], [Debian], [Ubuntu], [Fedora], [Arch Linux], [Void Linux], [Gentoo], and more!

Install from source
-------------------

See [BUILD.md](./BUILD.md) and [supported platforms](https://neovim.io/doc/user/support.html#supported-platforms) for details.

The build is CMake-based, but a Makefile is provided as a convenience.
After installing the dependencies, run the following command.
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
```

To install to a non-default location:
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo CMAKE_INSTALL_PREFIX=/full/path/
make install
```

CMake hints for inspecting the build:

- `cmake --build build --target help` lists all build targets.
- `build/CMakeCache.txt` (or `cmake -LAH build/`) contains the resolved values of all CMake variables.
- `build/compile_commands.json` shows the full compiler invocations for each translation unit.

Transitioning from Vim
--------------------

See [`:help nvim-from-vim`](https://neovim.io/doc/user/nvim.html#nvim-from-vim) for instructions.

Project layout
--------------

    ├─ cmake/           CMake utils
    ├─ cmake.config/    CMake defines
    ├─ cmake.deps/      subproject to fetch and build dependencies (optional)
    ├─ runtime/         plugins and docs
    ├─ src/nvim/        application source code (see src/nvim/README.md)
    │  ├─ api/          API subsystem
    │  ├─ eval/         Vimscript subsystem
    │  ├─ event/        event-loop subsystem
    │  ├─ generators/   code generation (pre-compilation)
    │  ├─ lib/          generic data structures
    │  ├─ lua/          Lua subsystem
    │  ├─ msgpack_rpc/  RPC subsystem
    │  ├─ os/           low-level platform code
    │  └─ tui/          built-in UI
    └─ test/            tests (see test/README.md)

License
-------

Neovim contributions since [b17d96][license-commit] are licensed under the
Apache 2.0 license, except for contributions copied from Vim (identified by the
`vim-patch` token). See [LICENSE.txt](./LICENSE.txt) for details.

[license-commit]: https://github.com/neovim/neovim/commit/b17d9691a24099c9210289f16afb1a498a89d803
[nvim-features]: https://neovim.io/doc/user/vim_diff.html#nvim-features
[nvim-news]: https://neovim.io/doc/user/news.html
[Roadmap]: https://neovim.io/roadmap/
[advanced UIs]: https://github.com/neovim/neovim/wiki/Related-projects#gui
[Managed packages]: ./INSTALL.md#install-from-package
[Debian]: https://packages.debian.org/testing/neovim
[Ubuntu]: https://packages.ubuntu.com/search?keywords=neovim
[Fedora]: https://packages.fedoraproject.org/pkgs/neovim/neovim/
[Arch Linux]: https://www.archlinux.org/packages/?q=neovim
[Void Linux]: https://voidlinux.org/packages/?arch=x86_64&q=neovim
[Gentoo]: https://packages.gentoo.org/packages/app-editors/neovim
[Homebrew]: https://formulae.brew.sh/formula/neovim

<!-- vim: set tw=80: -->

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **C/C++ / CMake** (manifests: CMakeLists.txt, Makefile; scanned in UPSTREAM_CLONE)
- Top-level source layout: `cmake/`, `cmake.config/`, `cmake.deps/`, `cmake.packaging/`, `contrib/`, `runtime/`, `scripts/`, `src/`, `test/`
- Snapshot size: **3828 files**, **805115 lines of code** (measured; see Benchmarks)
- Primary languages: `.vim` (2035), `.lua` (848), `.h` (304), `.c` (227), `.txt` (178), `(none)` (59)
- Upstream commit pinned for this packaging: `09e4491a5351e37cea4ed83b163de315fedc2eaa`

---

## Installation

[![Downloads](https://img.shields.io/github/downloads/neovim/neovim/total.svg?maxAge=2592001)](https://github.com/neovim/neovim/releases/)

Neovim is a project that seeks to aggressively refactor [Vim](https://www.vim.org/) in order to:

- Simplify maintenance and encourage [contributions](CONTRIBUTING.md)
- Split the work between multiple developers
- Enable [advanced UIs] without modifications to the core
- Maximize [extensibility](https://neovim.io/doc/user/api-ui-events.html#api-ui-events)

See the [Introduction](https://github.com/neovim/neovim/wiki/Introduction) wiki page and [Roadmap]
for more information.

Features
--------

- Modern [GUIs](https://github.com/neovim/neovim/wiki/Related-projects#gui)
- [API access](https://github.com/neovim/neovim/wiki/Related-projects#api-clients)
  from any language including C/C++, C#, Clojure, D, Elixir, Go, Haskell, Java/Kotlin,
  JavaScript/Node.js, Julia, Lisp, Lua, Perl, Python, Racket, Ruby, Rust
- Embedded, scriptable [terminal emulator](https://neovim.io/doc/user/terminal.html)
- Asynchronous [job control](https://github.com/neovim/neovim/pull/2247)
- [Shared data (shada)](https://github.com/neovim/neovim/pull/2506) among multiple editor instances
- [XDG base directories](https://github.com/neovim/neovim/pull/3470) support
- Compatible with most Vim plugins, including Ruby and Python plugins

See [`:help nvim-features`][nvim-features] for the full list, and [`:help news`][nvim-news] for noteworthy changes in the latest version!

Install from package
--------------------

Pre-built packages for Windows, macOS, and Linux are found on the
[Releases](https://github.com/neovim/neovim/releases/) page.

[Managed packages] are in [Homebrew], [Debian], [Ubuntu], [Fedora], [Arch Linux], [Void Linux], [Gentoo], and more!

Install from source
-------------------

See [BUILD.md](./BUILD.md) and [supported platforms](https://neovim.io/doc/user/support.html#supported-platforms) for details.

The build is CMake-based, but a Makefile is provided as a convenience.
After installing the dependencies, run the following command.
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
```

To install to a non-default location:
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo CMAKE_INSTALL_PREFIX=/full/path/
make install
```

CMake hints for inspecting the build:

- `cmake --build build --target help` lists all build targets.
- `build/CMakeCache.txt` (or `cmake -LAH build/`) contains the resolved values of all CMake variables.
- `build/compile_commands.json` shows the full compiler invocations for each translation unit.

Transitioning from Vim
--------------------

See [`:help nvim-from-vim`](https://neovim.io/doc/user/nvim.html#nvim-from-vim) for instructions.

Project layout
--------------

    ├─ cmake/           CMake utils
    ├─ cmake.config/    CMake defines
    ├─ cmake.deps/      subproject to fetch and build dependencies (optional)
    ├─ runtime/         plugins and docs
    ├─ src/nvim/        application source code (see src/nvim/README.md)
    │  ├─ api/          API subsystem
    │  ├─ eval/         Vimscript subsystem
    │  ├─ event/        event-loop subsystem
    │  ├─ generators/   code generation (pre-compilation)
    │  ├─ lib/          generic data structures
    │  ├─ lua/          Lua subsystem
    │  ├─ msgpack_rpc/  RPC subsystem
    │  ├─ os/           low-level platform code
    │  └─ tui/          built-in UI
    └─ test/            tests (see test/README.md)

License
-------

Neovim contributions since [b17d96][license-commit] are licensed under the
Apache 2.0 license, except for contributions copied from Vim (identified by the
`vim-patch` token). See [LICENSE.txt](./LICENSE.txt) for details.

[license-commit]: https://github.com/neovim/neovim/commit/b17d9691a24099c9210289f16afb1a498a89d803
[nvim-features]: https://neovim.io/doc/user/vim_diff.html#nvim-features
[nvim-news]: https://neovim.io/doc/user/news.html
[Roadmap]: https://neovim.io/roadmap/
[advanced UIs]: https://github.com/neovim/neovim/wiki/Related-projects#gui
[Managed packages]: ./INSTALL.md#install-from-package
[Debian]: https://packages.debian.org/testing/neovim
[Ubuntu]: https://packages.ubuntu.com/search?keywords=neovim
[Fedora]: https://packages.fedoraproject.org/pkgs/neovim/neovim/
[Arch Linux]: https://www.archlinux.org/packages/?q=neovim
[Void Linux]: https://voidlinux.org/packages/?arch=x86_64&q=neovim
[Gentoo]: https://packages.gentoo.org/packages/app-editors/neovim
[Homebrew]: https://formulae.brew.sh/formula/neovim

<!-- vim: set tw=80: -->

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

No usage section was found in the upstream readme. Entry points detected in this project directory:

```sh
# build first (see Installation), then run the produced binary from build/
```

Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

<a href="https://app.element.io/#/room/#neovim:matrix.org">Chat</a>
</h1>

[![Coverity Scan analysis](https://scan.coverity.com/projects/2227/badge.svg)](https://scan.coverity.com/projects/2227)
[![Packages](https://repology.org/badge/tiny-projects/neovim.svg)](https://repology.org/metapackage/neovim)
[![Debian CI](https://badges.debian.net/badges/debian/testing/neovim/version.svg)](https://buildd.debian.org/neovim)
[![Downloads](https://img.shields.io/github/downloads/neovim/neovim/total.svg?maxAge=2592001)](https://github.com/neovim/neovim/releases/)

Neovim is a project that seeks to aggressively refactor [Vim](https://www.vim.org/) in order to:

- Simplify maintenance and encourage [contributions](CONTRIBUTING.md)
- Split the work between multiple developers
- Enable [advanced UIs] without modifications to the core
- Maximize [extensibility](https://neovim.io/doc/user/api-ui-events.html#api-ui-events)

See the [Introduction](https://github.com/neovim/neovim/wiki/Introduction) wiki page and [Roadmap]
for more information.

Features
--------

- Modern [GUIs](https://github.com/neovim/neovim/wiki/Related-projects#gui)
- [API access](https://github.com/neovim/neovim/wiki/Related-projects#api-clients)
  from any language including C/C++, C#, Clojure, D, Elixir, Go, Haskell, Java/Kotlin,
  JavaScript/Node.js, Julia, Lisp, Lua, Perl, Python, Racket, Ruby, Rust
- Embedded, scriptable [terminal emulator](https://neovim.io/doc/user/terminal.html)
- Asynchronous [job control](https://github.com/neovim/neovim/pull/2247)
- [Shared data (shada)](https://github.com/neovim/neovim/pull/2506) among multiple editor instances
- [XDG base directories](https://github.com/neovim/neovim/pull/3470) support
- Compatible with most Vim plugins, including Ruby and Python plugins

See [`:help nvim-features`][nvim-features] for the full list, and [`:help news`][nvim-news] for noteworthy changes in the latest version!

Install from package
--------------------

Pre-built packages for Windows, macOS, and Linux are found on the
[Releases](https://github.com/neovim/neovim/releases/) page.

[Managed packages] are in [Homebrew], [Debian], [Ubuntu], [Fedora], [Arch Linux], [Void Linux], [Gentoo], and more!

Install from source
-------------------

See [BUILD.md](./BUILD.md) and [supported platforms](https://neovim.io/doc/user/support.html#supported-platforms) for details.

The build is CMake-based, but a Makefile is provided as a convenience.
After installing the dependencies, run the following command.
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
```

To install to a non-default location:
```bash
make CMAKE_BUILD_TYPE=RelWithDebInfo CMAKE_INSTALL_PREFIX=/full/path/
make install
```

CMake hints for inspecting the build:

- `cmake --build build --target help` lists all build targets.
- `build/CMakeCache.txt` (or `cmake -LAH build/`) contains the resolved values of all CMake variables.
- `build/compile_commands.json` shows the full compiler invocations for each translation unit.

Transitioning from Vim
--------------------

See [`:help nvim-from-vim`](https://neovim.io/doc/user/nvim.html#nvim-from-vim) for instructions.

Project layout
--------------

    ├─ cmake/           CMake utils
    ├─ cmake.config/    CMake defines
    ├─ cmake.deps/      subproject to fetch and build dependencies (optional)
    ├─ runtime/         plugins and docs
    ├─ src/nvim/        application source code (see src/nvim/README.md)
    │  ├─ api/          API subsystem
    │  ├─ eval/         Vimscript subsystem
    │  ├─ event/        event-loop subsystem
    │  ├─ generators/   code generation (pre-compilation)
    │  ├─ lib/          generic data structures
    │  ├─ lua/          Lua subsystem
    │  ├─ msgpack_rpc/  RPC subsystem
    │  ├─ os/           low-level platform code
    │  └─ tui/          built-in UI
    └─ test/            tests (see test/README.md)

License
-------

Neovim contributions since [b17d96][license-commit] are licensed under the
Apache 2.0 license, except for contributions copied from Vim (identified by the
`vim-patch` token). See [LICENSE.txt](./LICENSE.txt) for details.

[license-commit]: https://github.com/neovim/neovim/commit/b17d9691a24099c9210289f16afb1a498a89d803
[nvim-features]: https://neovim.io/doc/user/vim_diff.html#nvim-features
[nvim-news]: https://neovim.io/doc/user/news.html
[Roadmap]: https://neovim.io/roadmap/
[advanced UIs]: https://github.com/neovim/neovim/wiki/Related-projects#gui
[Managed packages]: ./INSTALL.md#install-from-package
[Debian]: https://packages.debian.org/testing/neovim
[Ubuntu]: https://packages.ubuntu.com/search?keywords=neovim
[Fedora]: https://packages.fedoraproject.org/pkgs/neovim/neovim/
[Arch Linux]: https://www.archlinux.org/packages/?q=neovim
[Void Linux]: https://voidlinux.org/packages/?arch=x86_64&q=neovim
[Gentoo]: https://packages.gentoo.org/packages/app-editors/neovim
[Homebrew]: https://formulae.brew.sh/formula/neovim

<!-- vim: set tw=80: -->

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | C/C++ / CMake |
| Manifests detected | CMakeLists.txt, Makefile |
| Files in snapshot | 3828 |
| Lines of code | 805115 |
| Dependency references | 14 |
| Dependencies by ecosystem | native: 14 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| native | Luv | - | src/nvim/CMakeLists.txt |
| native | Iconv | - | src/nvim/CMakeLists.txt |
| native | Libuv | - | src/nvim/CMakeLists.txt |
| native | Treesitter | - | src/nvim/CMakeLists.txt |
| native | UTF8proc | - | src/nvim/CMakeLists.txt |
| native | Libintl | - | src/nvim/CMakeLists.txt |
| native | Unibilium | - | src/nvim/CMakeLists.txt |
| native | Wasmtime | - | src/nvim/CMakeLists.txt |
| native | Lua | - | src/nvim/CMakeLists.txt |
| native | Luajit | - | src/nvim/CMakeLists.txt |
| native | Luajit | - | src/nvim/CMakeLists.txt |
| native | Gettext | - | src/nvim/po/CMakeLists.txt |
| native | Luajit | - | cmake.deps/CMakeLists.txt |
| native | Lua | - | cmake.deps/CMakeLists.txt |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

- `build/compile_commands.json` shows the full compiler invocations for each translation unit.

Transitioning from Vim
--------------------

See [`:help nvim-from-vim`](https://neovim.io/doc/user/nvim.html#nvim-from-vim) for instructions.

Project layout
--------------

    ├─ cmake/           CMake utils
    ├─ cmake.config/    CMake defines
    ├─ cmake.deps/      subproject to fetch and build dependencies (optional)
    ├─ runtime/         plugins and docs
    ├─ src/nvim/        application source code (see src/nvim/README.md)
    │  ├─ api/          API subsystem
    │  ├─ eval/         Vimscript subsystem
    │  ├─ event/        event-loop subsystem
    │  ├─ generators/   code generation (pre-compilation)
    │  ├─ lib/          generic data structures
    │  ├─ lua/          Lua subsystem
    │  ├─ msgpack_rpc/  RPC subsystem
    │  ├─ os/           low-level platform code
    │  └─ tui/          built-in UI
    └─ test/            tests (see test/README.md)

License
-------

Neovim contributions since [b17d96][license-commit] are licensed under the
Apache 2.0 license, except for contributions copied from Vim (identified by the
`vim-patch` token). See [LICENSE.txt](./LICENSE.txt) for details.

[license-commit]: https://github.com/neovim/neovim/commit/b17d9691a24099c9210289f16afb1a498a89d803
[nvim-features]: https://neovim.io/doc/user/vim_diff.html#nvim-features
[nvim-news]: https://neovim.io/doc/user/news.html
[Roadmap]: https://neovim.io/roadmap/
[advanced UIs]: https://github.com/neovim/neovim/wiki/Related-projects#gui
[Managed packages]: ./INSTALL.md#install-from-package
[Debian]: https://packages.debian.org/testing/neovim
[Ubuntu]: https://packages.ubuntu.com/search?keywords=neovim
[Fedora]: https://packages.fedoraproject.org/pkgs/neovim/neovim/
[Arch Linux]: https://www.archlinux.org/packages/?q=neovim
[Void Linux]: https://voidlinux.org/packages/?arch=x86_64&q=neovim
[Gentoo]: https://packages.gentoo.org/packages/app-editors/neovim
[Homebrew]: https://formulae.brew.sh/formula/neovim

<!-- vim: set tw=80: -->

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

Contributing to Neovim
======================

Getting started
---------------

If you are new to the codebase, read [:help dev-quickstart](https://neovim.io/doc/user/dev_tools.html#dev-quickstart)
to see how to run tests and start hacking on the codebase.

If you want to help but don't know where to start, here are some
low-risk/isolated tasks:

- Try a [complexity:low] issue.
- Fix bugs found by [Coverity](#coverity).
- [Merge a Vim patch] (requires strong familiarity with Vim)
  - NOTE: read the above link before sending improvements to "runtime files" (anything in `runtime/`).
    - *Vimscript* files are (mostly) maintained by [Vim], not Nvim.
    - *Lua* files are maintained by *Nvim*.
    - Nvim's [filetype detection](https://github.com/neovim/neovim/blob/master/runtime/lua/vim/filetype.lua) behavior matches Vim, so changes to filetype detection should be submitted to [Vim] first.

Reporting problems
------------------

- [Check the FAQ][wiki-faq].
- [Search existing issues][github-issues] (including closed!)
- Update Neovim to the latest version to see if your problem persists.
- Try to reproduce with `nvim --clean` ("factory defaults").
- If a specific configuration or plugin is necessary to recreate the problem, use the minimal template in `contrib/minimal.lua` with `nvim --clean -u contrib/minimal.lua` after making the necessary changes.
- [Bisect](https://neovim.io/doc/user/starting.html#bisect) your config: disable plugins incrementally, to narrow down the cause of the issue.
- [Bisect][git-bisect] Neovim's source code to find the cause of a regression, if you can. This is _extremely_ helpful.
- When reporting a crash, [include a stacktrace](https://neovim.io/doc/user/dev_tools.html#dev-tools-backtrace).
- Use [ASAN/UBSAN](#sanitizers-asan-and-ubsan) to get detailed errors for segfaults and undefined behavior.
- Check the logs. `:edit $NVIM_LOG_FILE`
- Include `cmake --system-information` for build-related issues.

Developer guidelines
--------------------

- New functionality should generally be implemented in Lua, not C. PRs [#37757](https://github.com/neovim/neovim/pull/37757), [#37831](https://github.com/neovim/neovim/pull/37831)
  are excellent examples of this.
- Read [:help dev-quickstart](https://neovim.io/doc/user/dev_tools.html#dev-quickstart) to see how to run tests and start hacking on the codebase.
- Read [:help dev](https://neovim.io/doc/user/dev.html#dev) and [:help dev-doc][dev-doc-guide] if you are working on Nvim core.
- Read 

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE.txt` in the upstream snapshot).

License file excerpt:

```text
Copyright Neovim contributors. All rights reserved.

Neovim is licensed under the terms of the Apache 2.0 license, except for
parts of Neovim that were contributed under the Vim license (see below).

Neovim's license follows:

====
                                 Apache License
                           Version 2.0, January 2004
                        https://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `NEOVIM_PRIOR_DOCS` (category: SOFTWARE DEVELOPMENT)
- **Upstream URL:** https://github.com/neovim/neovim
- **Pinned commit (SHA):** `09e4491a5351e37cea4ed83b163de315fedc2eaa`
- **Branch:** master
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`81d76bd65e7c3cac98ce72feebf594bdc29890c0656e6a0ce2ed08a9511a2c70`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

