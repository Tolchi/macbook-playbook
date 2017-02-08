# macbook-playbook

Automatically prepare a Macbook for development and desktop tasks using Ansible.

## Warning

At the current state this project is not usable by people other than me out of
the box.

## Tested on

- MacBookPro11,1 with OS X 10.9 (13A2093)

## Assumptions

- You have a clean installation of OS X
- You have a Dropbox account
- There is a directory named "ssh" under your Dropbox root directory.
- Your public and private SSH keys are inside the aforementioned "ssh"
  directory.
- There is a git repository for your dotfiles and it installs itself with `rake
  install`.
- There is a git repository for your Vim configuration files.

## Configuring machine

### Prepare machine to run the Ansible playbooks

    $ ./scripts/bootstrap

### Configure machine

    $ ansible-playbook main.yml -i hosts

## Installs

### Desktop applications

- Cantata
- Dash
- Divvy
- Dropbox
- Firefox
- Google Chrome
- Google Photos
- LICEcap
- LightTable
- OpenOffice
- Prey
- Skitch
- Skype
- Steam
- Theremin
- Unity
- VLC
- XQuartz
- YNAB

### Text editors
- Emacs 25
- MacVim
- Neovim 1.5
- Vim 8.0

### Command line applications

- ffmpeg
- irssi (with IrssiNotifier)
- mpc
- shpotify
- mpd
- mpdscribble
- mplayer
- s3cmd
- vault
- vimpc
- wkhtmltopdf

### Browser Plugins

- Adblock Plus
- Hangouts
- JRE
- Pentadactyl
- Silverlight

### Programming Languages

- GNU Octave
- Haskell Platform
- Java (JDK)
- Lua
- Node.js
- PureScript
- Python 3
- R

### Virtualization

- Docker
- Vagrant (with vagrant-vbguest plugin)
- VirtualBox

### Shell

- fish
- iTerm
- oh-my-zsh
- Powerline
- tmux
- Zsh

### Haskell Utilities

- ghc-mod
- hlint
- hoogle
- pointfree

### Utilities

- chef
- knife
- bundler
- ctags
- fontforge
- Hadoop
- heroku
- Homebrew
- htop
- jmeter
- jsxhint
- leiningen
- LuaJIT
- MacPorts
- MacTeX
- p7zip
- pgsanity
- PostgreSQL 9.4
- pulp
- reattach-to-user-namespace
- terminal-notifier
- the-silver-searcher
- tmuxinator
- tree
- wget

### Git repositories

- dotfiles
- vimfiles

## Configures

- Remaps Caps-Lock to Control
- Puts SSH keys in place
- Patches Monaco font for Powerline

## TODO

- Add user in the sudoers list in `script/bootstrap`.
- Add notes regarding encrypting and storing SSH keys on Dropbox.
- Key mappings for controlling volume, mpd, etc.
- Make WiFi not be disabled when the machine sleeps and is charging.
- Disable annoying bell sound.
- Integrate https://github.com/mathiasbynens/dotfiles/blob/master/.osx?
- Leverage some of this: https://gist.github.com/brandonb927/3195465
- Configure iTerm to use Monaco For Powerline.
- Move hard coded values to configurable variables.
- Make it more portable, so that it can be useful to more people.
- Abstract repeated installation tasks.
- Extract roles to a different project?
- Improve README with rationale, useful prose, etc.

## Author

[Murilo Pereira](http://murilopereira.com)

## License

[MIT](http://opensource.org/licenses/MIT)
