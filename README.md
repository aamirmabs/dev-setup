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
