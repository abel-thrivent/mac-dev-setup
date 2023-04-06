

## Manual Setup
- [Defaults](#defaults)
- [Tools](#tools)
- [Applications](#applications)
- [Optimizations](#optimizations)

### Defaults

##### Create Dock spacers:

```sh
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}' && \
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}' && \
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}' && \
killall Dock
```

##### Autohide Dock:

```sh
defaults write com.apple.dock autohide -boolean true && \
killall Dock
```

##### Display hidden Finder files/folders:

```sh
defaults write com.apple.finder AppleShowAllFiles -boolean true && \
killall Finder
```

##### Installing xcode-select (CLI tools):

```sh
xcode-select --install
```

##### Installing brew ([Homebrew](https://brew.sh/)):

If: Apple Silicon/ARM Architecture:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" && \
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"'>>$HOME/.zprofile && \
eval "$(/opt/homebrew/bin/brew shellenv)" && \
brew doctor
```

If Intel Architecture:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" && \
brew doctor
```

### Tools

##### Install [watchman](https://facebook.github.io/watchman/):

```sh
brew install watchman
```

##### Install [trash](https://hasseg.org/trash/):

```sh
brew install trash
```

##### Install [git](https://git-scm.com/):

```sh
brew install git
```

##### Install [git-flow](https://github.com/nvie/gitflow/):

```sh
brew install git-flow
```

##### Install [zsh](https://www.zsh.org/):

```sh
brew install zsh
```

##### Install Starship


##### Install [node](https://nodejs.org/)

```sh
not via Homebrew!!
```

##### Install [n](https://github.com/tj/n/) (Node via n):

```sh
brew install n
```

##### Install [nvm](https://github.com/nvm-sh/nvm/) (Node via nvm):

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

##### Install [yarn](https://yarnpkg.com/):

```sh
brew install yarn
```

##### Install [pnpm](https://pnpm.io/):

```sh
brew install pnpm
```

##### Upgrade [npm](https://www.npmjs.com/) (globally via npm):

```sh
npm install -g npm@latest
```

##### Install/Upgrade [serve](https://github.com/zeit/serve/) (globally via npm):

```sh
npm install -g serve@latest
```

### Applications/Casks

```

##### Install DiffMerge:

If Intel Architecture:

```sh
brew install --cask diffmerge
```

##### Install Insomnia:

```sh
brew install --cask insomnia
```

##### Install Warp:

##### Install Rectangle:

```sh
brew install --cask rectangle
```

##### Install Sourcetree:

```sh
brew install --cask sourcetree
```

1. Set the font by going to:
   - "Preferences &rarr; Diff &rarr; Internal Diff Visualization &rarr; Diff View font"
   - Font name: "JetBrainsMono Nerd Font Mono"
2. Restart Sourcetree and resolve any remaining issues.


##### Install Visual Studio Code:

```sh
brew install --cask visual-studio-code
```

1. Install my Extensions:
   ```sh
   code --install-extension alefragnani.project-manager
   code --install-extension atomiks.moonlight
   code --install-extension bradlc.vscode-tailwindcss
   code --install-extension christian-kohler.npm-intellisense
   code --install-extension christian-kohler.path-intellisense
   code --install-extension dbaeumer.vscode-eslint
   code --install-extension dsznajder.es7-react-js-snippets
   code --install-extension eamodio.gitlens
   code --install-extension EditorConfig.EditorConfig
   code --install-extension esbenp.prettier-vscode
   code --install-extension formulahendry.auto-rename-tag
   code --install-extension Gruntfuggly.todo-tree
   code --install-extension L13RARY.l13-diff
   code --install-extension mattpocock.ts-error-translator
   code --install-extension mikestead.dotenv
   code --install-extension ms-vscode.sublime-keybindings
   code --install-extension Orta.vscode-twoslash-queries
   code --install-extension Prisma.prisma
   code --install-extension stylelint.vscode-stylelint
   code --install-extension Tyriar.sort-lines
   code --install-extension unifiedjs.vscode-mdx
   code --install-extension vscode-icons-team.vscode-icons
   code --install-extension WallabyJs.console-ninja
   code --install-extension wix.vscode-import-cost
   code --install-extension zenclabs.previewjs
   code --install-extension Zignd.html-css-class-completion
   ```
2. Copy my Visual Studio Code User settings:
   ```sh
   cp ~/Downloads/mac-dev-setup/Code/* ~/Library/Application\ Support/Code/User
   ```
3. Restart Visual Studio Code and resolve any remaining issues.

