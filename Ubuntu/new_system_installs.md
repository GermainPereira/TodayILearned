# New System Installs

## Ubuntu

#### Increase number of file watchers

```
echo 999999 | sudo tee -a /proc/sys/fs/inotify/max_user_watches && echo 999999 | sudo tee -a /proc/sys/fs/inotify/max_queued_events && echo 999999 | sudo tee -a /proc/sys/fs/inotify/max_user_instances && watchman shutdown-server && sudo sysctl -p
```

#### Useful Installs

https://github.com/GermainPereira/TodayILearned/blob/master/Ubuntu/useful_installs.md

#### Ubuntu Aliases

https://github.com/GermainPereira/TodayILearned/blob/master/Ubuntu/aliases.md

#### Ubuntu Themes

https://github.com/GermainPereira/TodayILearned/blob/master/Ubuntu/theme.md

#### Google Chrome

```
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb
```

#### Hide left-menu docker

Settings -> appearance -> hide docker (left bar)

#### Custom Keyboard Inputs

Settings -> ...

#### Build Essential

`sudo apt-get install build-essential`

#### Git

`sudo apt install git`

#### VSCODE

`sudo snap install code --classic`

#### SSH/RSA

- **RSA**

```
ssh-keygen -t rsa -b 2048 -C "your-email@provider.com"
```

- **SSH**

```
ssh-add ~/.ssh/id_ed25519
ssh-keygen -t ed25519 -C "your-email@provider.com"

```

Copy the keys using:

```
sudo apt install xclip
xclip -sel clip < ~/.ssh/id_ed25519.pub
```

## Infra and Testing

#### Http packages and Docker

```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common


curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-key fingerprint 0EBFCD88
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
sudo apt update
sudo apt-get install docker-ce docker-ce-cli containerd.io
apt-cache policy docker-ce
sudo apt install docker
```

- **Verify**
  `sudo docker run hello-world`

#### Run command without sudo (docker for instance)

https://github.com/GermainPereira/TodayILearned/blob/master/Ubuntu/run_without_sudo.md

#### DBeaver

`sudo snap install dbeaver-ce`

#### MySQL

```
sudo apt install mysql-server
sudo mysql_secure_installation
```

#### Insomnia

```
echo "deb https://dl.bintray.com/getinsomnia/Insomnia /" \
    | sudo tee -a /etc/apt/sources.list.d/insomnia.list

wget --quiet -O - https://insomnia.rest/keys/debian-public.key.asc \
    | sudo apt-key add -

sudo apt-get update
sudo apt-get install insomnia
```

## Git and development environments

#### Git Configs

```
git config --global core.editor "vim"
git config --global user.name "FIRST_NAME LAST_NAME"
git config --global user.email "MY_NAME@example.com"
```

#### Git Commands and Aliases

https://github.com/GermainPereira/TodayILearned/blob/master/Git/git_commands.md

#### Programming languages

- **PHP:**
  https://linuxize.com/post/how-to-install-php-8-on-ubuntu-20-04/

#### Package Managers and Frameworks

```
sudo apt install -y nodejs
sudo apt install -y npm
npm install -g @angular/cli

wget https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh
bash ./Anaconda3-2020.07-Linux-x86_64.sh
conda update --all --yes
```

#### VSCode

`sudo snap install --classic code`

**VSCode - Extensions, Config and Custom Shortcuts**
https://github.com/GermainPereira/TodayILearned/blob/master/Dev_Environments/VisualStudioCode/extensions.md
https://github.com/GermainPereira/TodayILearned/blob/master/Dev_Environments/VisualStudioCode/config.md
https://github.com/GermainPereira/TodayILearned/blob/master/Dev_Environments/VisualStudioCode/vscode_custom_shortcuts.md
