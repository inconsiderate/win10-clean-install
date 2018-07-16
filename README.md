# Windows 10 Clean Install

## Bash On Ubuntu On Windows Subsystem For Linux
---

coming

### Bash Config Stuff

```bash
#alias gitlog to show more detail and pretty colors
echo "alias gitlog=\"git log --graph --decorate --date=relative --format=format:'%C(bold blue)%H%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(red)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all\"" >> ~/.zshrc
```

### Setup Github

```bash
ssh-keygen -t rsa -C "contact@michaelkant.com"

#copy ssh key to clipboard for adding to github.com
pbcopy < ~/.ssh/id_rsa.pub

#test connection
ssh -T git@github.com

#set git config values
git config --global user.name "Michael Kant" && \
git config --global user.email "michaelkant@live.com" && \
git config --global github.user inconsiderate && \
git config --global core.editor "code -w" && \
git config --global color.ui true && \
git config --global push.default simple

#set git global ignore file
touch ~/.gitignore && \
git config --get core.excludesfile '~/.gitignore' && \
echo ".DS_Store" >> ~/.gitignore && \
echo ".gitignore" >> ~/.gitignore && \
echo ".idea" >> ~/.gitignore && \
echo "*.log" >> ~/.gitignore

#tell git to ignore chmod's
git config --global core.filemode false

```

### Visual Studio Code
---

```json
//keybindings.json
[
    {
      "key": "ctrl+shift+up",
      "command": "editor.action.moveLinesUpAction",
      "when": "editorTextFocus"
    },
    {
      "key": "ctrl+shift+down",
      "command": "editor.action.moveLinesDownAction",
      "when": "editorTextFocus"
    },
    {
      "key": "ctrl+D",
      "command": "editor.action.copyLinesDownAction",
      "when": "editorTextFocus"
    }
  ]
```
