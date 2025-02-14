<h1 align="center">DidYouMean</h1>

<p align="center">
    <a href="LICENSE"> <img src="https://img.shields.io/aur/license/didyoumean-git?style=for-the-badge" /></a>
    <a href="https://aur.archlinux.org/packages/didyoumean-git/"> <img src="https://img.shields.io/aur/version/didyoumean-git?color=1793d1&label=didyoumean-git&logo=arch-linux&style=for-the-badge" /></a>
    <a href="https://github.com/hisbaan/homebrew-tap"><img src="https://img.shields.io/badge/NixOS-v1.1.0-5277c3?style=for-the-badge&logo=NixOS" /></a>
    <a href="https://github.com/hisbaan/homebrew-tap"><img src="https://img.shields.io/badge/Homebrew-v1.1.0-fbb040?style=for-the-badge&logo=Homebrew" /></a>
    <a href="https://lib.rs/crates/didyoumean"> <img src="https://img.shields.io/crates/v/didyoumean?color=red&label=crates.io/lib.rs&logo=Rust&style=for-the-badge" /></a>
</p>

DidYouMean (or `dym`) is a command-line spelling corrector written in rust utilizing [Levenshtein distance](https://en.wikipedia.org/wiki/Levenshtein_distance). DidYouMean is for those moments when you know what a word sounds like, but you're not quite sure how it's spelled.

<p align="center">
    <!-- <img src="img/meningitis.png" height="250" style="border-radius: 10px; margin: 0.5em;"/> -->
    <img src="img/cyclophosphamide.png" height="250" style="border-radius: 10px; margin: 0.5em;"/>
</p>

## Installation

### Arch Linux (and derivatives)

DidYouMean is available on the AUR as [`didyoumean-git`](https://aur.archlinux.org/packages/didyoumean-git). You can install it using any AUR helper. Using `paru`, the command would be as follows:

```sh
paru -S didyoumean-git
```

### NixOS

[evanjs](https://github.com/evanjs) very kindly packaged `didyoumean` for NixOS. The command to install is as follows:

```sh
nix-env install -iA nixpkgs.didyoumean
```

### Homebrew (macOS)

Homebrew is a package manager for macOS. Currently, I have only packaged an x86\_64 binary. The command to install it is as follows:

```sh
brew tap hisbaan/tap
brew install didyoumean
```

### Build from source

Run the following command to build `dym` from source and install it in your home directory. Ensure that you have `$CARGO_HOME/bin/` in your path.

```sh
cargo install didyoumean
```

## Developer Installation

The build dependencies for this project are `git`, `rust`, `rustc`, and `cargo`. First, clone this repository, then run

```sh
cargo run -- <args>
```

where `<args>` are the command-line arguments you would pass the DidYouMean binary. Note that this is an unoptimized build contianing debug information so it runs much, much slower.
