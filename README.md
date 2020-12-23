# Dev Setup

Ideally I would be using a gist, but I'm maintaining the notes here as it would be easier to manage links to source material and organize topics in a markdown file.

## Setup VM

Current set up is running a Ubuntu 20.4 LTS as a VM on a Windows machine. Follow standard procedure for set up and install. Install the Guest additions after setup.

### Improve performance

- Make sure [3D acceleration is enabled](https://blogs.oracle.com/scoter/oracle-vm-virtualbox-6-3d-acceleration-for-ubuntu-1804-guest) else make the necessary changes.
- Set base memory 4-8 GB
- Set display memory to max 128 MB
- Monitor count to 2 for dual monitor set up
- Enable 3D Acceleration
- If graphics card is used, go its program and make sure that graphics card is enabled for the VM program
- Allocate more cores to processor - currently 4 cores assigned

## Software

- VSCode
- Firefox (Stable or Developer)
- Chrome
- [Hyper](https://hyper.is/)

## CLI

### Git

Use [Project Odin Git Guide](https://www.theodinproject.com/courses/foundations/lessons/setting-up-git) to set up Git and SSH key with Github. The commands to do so are as follows:

#### Setup Git

`git config --global user.name "Your Name"`
`git config --global user.email "yourname@example.com"`

`git config --global init.defaultBranch main`
`git config --global color.ui auto`

#### Set up account

`git config --get user.name`
`git config --get user.email`

#### Set up SSH key

Check if SSH key is already installed
`ls ~/.ssh/id_rsa.pub`

If not, set it up using `ssh-keygen -C <youremail>`

Set up key on the Github settings page. Get key using `cat ~/.ssh/id_rsa.pub`

### Oh My ZSH

- First install `zsh` with `sudo apt install zsh`
- Make sure you have cURL and wget installed `sudo apt install curl wget`
- Install Oh My ZSH with curl `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
- Or with wget `$ sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"`
- Or Clone the repository `git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh`
- backup your existing ~/.zshrc file `cp ~/.zshrc ~/.zshrc.orig`
- Create a new zsh configuration file `cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc`
- Change your default shell `chsh -s $(which zsh)`
- Log out from your user session and log back in to see this change.

#### powerlevel10K Theme

View the documentation on the [Github page](https://github.com/romkatv/powerlevel10k).

#### Plugins

- Clone [Z.sh](https://github.com/rupa/z) to your home directory and set up on config file
- [zsh-autosuggestions](https://www.sitepoint.com/zsh-tips-tricks/)
  - `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
  - Then add the plugin `zsh-autosuggestions` to list in `~/zshrc`
- [command-not-found](https://github.com/ohmyzsh/ohmyzsh/wiki/plugins#command-not-found) looks up for any spelling mistakes in typed command
- [sudo](https://github.com/ohmyzsh/ohmyzsh/wiki/plugins#sudo) used double `Esc` presses to add sudo in front of current command or if prompt is empty it will populate the previous command with sudo.
