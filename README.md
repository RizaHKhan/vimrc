# The Ultimate vimrc

### Install for your own user only

The awesome version includes a lot of great plugins, configurations and color schemes that make Vim a lot better. To install it simply do following from your terminal:

    git clone --depth=1 https://github.com/RizaHKhan/vimrc.git ~/.vim_runtime
    sh ~/.vim_runtime/install_awesome_vimrc.sh

# Presentation

Thanks for attending todays talk on VIM. A few things I'd like to get out of the way. First of all, I'm going to make an assumption that you don't have any or very limited experience with VIM.

You found yourself stuck in it once and had to google how to close it. Which, funny enough, is my first experience with VIM.

Secondly, there will be demonstrations of the various features and plugins of VIM, but no technical discussion on how to do certain things. I want to keep this talk relatively light because we will be covering a few topics about VIM so it might be too much to take in.

## Pros and Cons of VIM

Although I personally think VIM is the greatest text editing ever, and has increased my producitivy as a developer along with making the whole development process more enjoyable, I do think that its a tool you should use only if you think it will bring value to your life.

I think there are plenty of valid alternatives to VIM and they do their jobs quite well. IDE's like VSCode and PHPStorm being examples.

Pros:

1. VIM will help you eleminate the mouse
2. Features will make you write out code faster
3. Customizable with many plugins
4. Can customize every aspect of it with your own keybinds and functions

Cons:

1. Steep learning curve. The first week of learning will be a wash.
2. Setup can take a while and forces you to dig into things that might not be relevant.

## Demonstration

You probably thing of VIM as really awful looking editor with no real syntax highlighting for coders. Despite the ke

## Popular Plugins

### Color Themes and Syntax Highlighting

Like with many other

### Code Formatting

### Linting

### Git with Vim Fugitive

### File Explorer

### Language Servers

## Installation

# Coc

## Dependencies

Plug:

```
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

:CocInstall coc-prettier
:CocInstall coc-tsserver
:CocInstall coc-phpls
:CocInstall @yaegassy/coc-volar
:CocInstall coc-eslint
:CocInstall coc-json
:CocInstall coc-snippets

```

FZF:
```

sudo apt-get install fzf

```

RIPGREP:
```

sudo apt-get install ripgrep

```

## Config

```

{
"coc.preferences.formatOnSaveFiletypes": [
"*"
],
"eslint.autoFixOnSave": true,
"eslint.format.enable": false,
"eslint.alwaysShowStatus": true,
"eslint.options": { "extensions": [".html", ".js", ".vue", ".jsx"] },
"eslint.validate": [
"javascript",
"javascriptreact",
{
"language": "vue",
"autoFix": true
}
],
"diagnostic.refreshOnInsertMode": true,
"diagnostic.messageDelay": 500,
"diagnostic-languageserver.filetypes": {
"javascript": "eslint"
},
"diagnostic-languageserver.linters": {
"eslint": {
"command": "./node_modules/.bin/eslint",
"rootPatterns": [".git", "package.json"],
"debounce": 100,
"args": ["--stdin", "--stdin-filename", "%filepath", "--format", "json"],
"sourceName": "eslint",
"parseJson": {
"errorsRoot": "[0].messages",
"line": "line",
"column": "column",
"endLine”: “endLine",
"endColumn": "endColumn",
"message": "${message} [${ruleId}]",
"security": "severity"
},
"securities": {
"2": "error",
"1": "warning"
}
}
},
"volar.enable": true,
"volar.formatting.enable": true,
"vetur.format.defaultFormatter.pug": "prettier",
"vetur.ignoreProjectWarning": true,
"typescript.suggestionActions.enabled": false,
"bladeFormatter.enable": true,
"bladeLinter.enable": true,
"bladeLinter.lintOnSave": true
}

```

# FAQ

## Merginal Not Working
```
