# Dev Setup

Ideally I would be using a gist, but I'm maintaining the notes here as it would be easier to manage links to source material and organize topics in a markdown file.

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
