# Terminal Automation

## Rename ONLY file content in directories recursively

```
find . -type f -exec sed -i 's/contentToBeReplaced/newContent/g' {} \;
``` 

## Rename ONLY file AND directory names recursively

```
find directoryToRenameRecursively/ -exec rename 's/team/workflow/g' '{}' \;
```



## Move multiple files in current folder


#### Test first

```
for f in *django*; do echo git mv -v -- "$f" django ; done
```

#### Do
```
for f in *django*; do git mv -v -- "$f" django ; done
```

## Kill Process On Port

#### Write it into `~./bashrc`
```
alias kill-port='
kill_process () {     
    sudo kill -9 $(sudo lsof -t -i:$1); 
}
kill_process '
```

## Confirm (Y/N) Automatically

```
confirm() {

    # call with a prompt string or use a default

    read -r -p "${1:-Are you sure? [y/N]} " response

    case "$response" in

        [yY][eE][sS]|[yY])

            true

            ;;

        *)

            false

            ;;

    esac

}
```

## Always show branch and hide user on CLI `~./bashrc`

```
if [ "$color_prompt" = yes ]; then
    PS1="\[\e[0;36m\]\w\[\e[0m\] \[\e[0;34m\]\$(__git_ps1 '(%s) ')\[\e[0m\]\$ "
else
    PS1="\[\e[0;36m\]\w\[\e[0m\] \[\e[0;34m\]\$(__git_ps1 '(%s) ')\[\e[0m\]\$ "
fi
unset color_prompt force_color_prompt
```
