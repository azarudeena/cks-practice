Vim configurations 

```shell
vi ~/.vimrc 

set ts=2 sw=2 expandtab ruler cursorline paste
set backspace=intent,eol,start

                # OR  use the below command 

echo 'set nu ts=2 sw=2 expandtab ruler cursorline' > ~/.vimrc
echo 'set backspace=indent,eol,start' >> ~/.vimrc
echo 'set paste'  >> ~/.vimrc
echo 'set pastetoggle=<F10>'  >> ~/.vimrc

```

set the above settings for better visibility and editing. 

kubectl config

    https://kubernetes.io/docs/reference/kubectl/cheatsheet/

Use the cheat sheet configure the auto complete for bash. Below block will help you with auto completion and a 
shorthand to `kubectl` as k

```shell

source <(kubectl completion bash) # setup autocomplete in bash into the current shell, bash-completion package should be installed first.
echo "source <(kubectl completion bash)" >> ~/.bashrc # add autocomplete permanently to your bash shell.

alias k=kubectl
complete -F __start_kubectl k
```


also for dry-run, use the below block

```shell
export dy="--dry-run=client -oyaml"
export now="--grace-period=0 --force"

#user the above variable dy to append to commands run. Below example. 

k run nginx --image=nginx $dy 
k delete pod nginx $now 

```

```shell
echo 'set nu ts=2 sw=2 expandtab ruler cursorline' > ~/.vimrc
echo 'set backspace=indent,eol,start' >> ~/.vimrc
echo 'set paste'  >> ~/.vimrc
echo 'set pastetoggle=<F10>'  >> ~/.vimrc

source <(kubectl completion bash) # setup autocomplete in bash into the current shell, bash-completion package should be installed first.
echo "source <(kubectl completion bash)" >> ~/.bashrc # add autocomplete permanently to your bash shell.

alias k=kubectl
complete -F __start_kubectl k

export dy="--dry-run=client -oyaml"
export now="--grace-period=0 --force"
```