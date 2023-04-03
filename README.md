
setup autocomplete for zsh 


echo "
autoload -Uz compinit
compinit" >> ~/.zshrc


cat >>~/.zshrc<<EOF
if [ $commands[oc] ]; then
  source <(oc completion zsh)
  compdef _oc oc
fi
EOF
