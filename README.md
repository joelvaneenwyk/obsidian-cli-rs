# Obsidian Launcher

> ⚠️ This is a fork of [obs](https://github.com/kootsZhin/obs) by [kootsZhin](https://github.com/kootsZhin). There are no additional changes or benefits from using this forked repository yet as this is only here to evaluate what work remains and if this is maintainable enough to rely on.

<!-- markdownlint-disable MD033 -->

<h1 id="readme-title" align="center">
    <div>
      <img alt="Obsidian logo" src="./assets/obsidian.png" width="200"/>
      <br/>
      <code>obs</code> - the Obsidian CLI
    </div>
    <div id="readme-description" style="font-size: 70%; padding-top:10px">⚡️ Connecting your second brain to the terminal ⚡️</div>
</h1>

> 📢 Please note that `obs` is under active development and currently only support MacOS, please report any issue while using!

## Features

- Fast & easy access to vaults from terminal in seconds
- Backup your vault to remote git effortlessly
- Flat learning curve without the need to memorize complicated commands
- Automatically fetch vault list from Obsidian, no extra config needed

<p align="center">
  <img src="assets/demo-1.gif" alt="animated" />
</p>

## Usage

- `obs` : open up a menu for choosing actions and vault to interact with
  - `goto` : goto vault
  - `open` : open vault
  - `backup` : backup vault
- `obs --goto <GOTO>` : `cd` to the directory of vault `<GOTO>`
- `obs --open <OPEN>` : open the vault `<OPEN>` in Obsidian
- `obs --help` : show help

<p align="center">
  <img src="assets/demo-2.gif" alt="animated" />
</p>

## Getting Started

1. Install `obs`

    ```bash
    cargo install obs
    ```

2. Put this in your `.zshrc` (or equivalent)

    ```bash
    obs() {
        local result=$(command obs "$@")
        [ -n "$result" ] && cd -- "$result"
    }
    ```

3. Start using: `obs`!

## License

[MIT @ 2023](LICENSE): Distributed under the MIT License.
