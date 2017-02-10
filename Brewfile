##
# Brewfile by Joel Parker Henderson and SixArm.com
#
# CAUTION: THIS IS A WORK IN PROGRESS. USE AT YOUR OWN RISK.
#
# We use this Brewfile for our teams and their developer laptops.
#
# This file installs many apps, including office suites, multimedia suites,
# programming langauges and IDEs, unix utilities, and sysadmin tools.
#
# This file is organized in meaningful sections because we want to
# make it easy for you to pick and choose sections that you want.
#
# ## Taps
#
# We do not use tap in this file; instead, we use full paths.
# This is because we want to be as clear as possible about what
# is being installed, and from what locations.
#
# ## Dupes
#
# We generaly prefer homebrew/dupes to preinstalled Mac software.
# For example, we prefer the GNU `sed` command vs. macOS `sed` command.
# However, we have seen this cause conflicts with macOS software that
# isn't aware of GNU; therefore we install the dupes in parallel.
#
# ## Contents
#
# This file has a bunch of sections:
#
#   * Browsers: firefox, google-chrome, opera, ...
#   * Passwords: keybase, 1password, lastpass, ...
#   * Terminals: iterm2, tmux, screen, ...
#   * Shells: bash, zsh, fish, mosh, ...
#   * Editors: vim, emacs, atom, sublime, ...
#   * Downloaders: curl, wget, cask, carthage, ...
#   * Version control: git, hg, svn, cvs, ...
#   * GNU command line tools
#   * System related: TODO
#   * File compression: zstd, unrar, unzip, ...
#   * File synchronization: rsync, unison, syncthing, ...
#   * Text search: ripgrep, ag, sift, ...
#   * Operating-related
#   * Build tools
#   * Fonts: hundreds of fonts
#   * JetBrains programmer tools
#   * OmniGroup project management tools
#   * Database servers: postgresql, redis, ...
#   * Database searchers: sphinx, TODO
#   * Database managers: TODO
#   * Markup languages: pandoc, TODO
#   * Programming languages: Java, Node, Python, ...
#
# ## See Also
#
# See also:
#
#   * https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/
#
# ## Tracking
#
# * Package: https://github.com/joelparkerhenderson/brewfile
# * Version: 0.2.0
# * Created: 2017-01-01
# * Updated: 2017-02-07
# * License: GPL
# * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
##

##
# Browsers
#
# We prefer Firefox because it's open source.
##

# Firefox web browser
cask 'firefox'

# Google Chrome web browser
cask 'google-chrome'

# Opera web browser
cask 'opera'

##
# Passwords
#
# We use password-manager applications with many of our projects.
# If you don't use these, feel free to delete them.
##

# Keybase.io digital signature manager
brew 'keybase'

# 1password is a password manager
cask '1password'

# LastPass is a password manager
cask 'lastpass'

##
# Terminals
#
# We typically use `tmux`, `tmate`,
# and sometimes fall back on `screen`.
##

# iTerm is our favorite terminal app.
cask 'iterm2'

# Tmux is a newer terminal multiplexer.
#
# TODO:
#
#     brew 'pkg-config' && brew link pkg-config && brew 'tmux'
#
brew 'tmux'

# tmate is a fork of tmux that makes screen sharing friendlier.
brew 'tmate'

# Screen is an older terminal multiplexer.
brew 'homebrew/dupes/screen'

##
# Shells
#
# We typically use bash, zsh, fish, and mosh.
##

# Bash is the Bourne Again SHell. Bash is an sh-compatible shell.
brew 'bash'

# Programmable completion functions for bash
brew 'bash-completion'

# Bashish is a theme enviroment for text terminals.
brew 'bashish'

# Zsh is a shell designed for interactive use.
brew 'zsh'

# Fish shell.
brew 'fish'

# Mobile Shell (MOSH) is like SSH plus roaming and smart echo.
brew 'mobile-shell'

##
# Editors
#
# We typically use command line editors (vim, emacs, etc.)
# and sometimes use GUI editors (atom, sublime, etc.)
##

# Vim editor
brew 'vim'

# MacVIM editor
cask 'macvim'

# Emacs editor
cask 'emacs'

# Emacs editor for Spacemacs
# TODO: brew tap d12frosted/emacs-plus
brew 'emacs-plus'
# brew linkapps emacs-plus

# Atom editor by GitHub
cask 'atom'

# Sublime text editor
cask 'sublime-text'

# GNU Aspell is a free open source spell checker; compare `lspell`.
#brew 'aspell --with-lang=en'

# Enca - detect and convert encoding of text files
brew 'enca'

# MacTex: LaTeX document preparation system with high-quality typesetting.
cask 'mactex'

##
# Downloaders
#
# These items download files and fetch content from the network.
##

# Carthage is a simple, decentralized dependency manager for Cocoa
brew 'carthage'

# Homebrew Cask extends Homebrew to install OS X applications and large binaries.
brew 'cask'

# curl is a command line tool for transferring data with URL syntax
brew 'curl'

# HTTrack is a free and easy-to-use offline browser utility.
brew 'httrack'

# Wget is a free software package for retrieving files using HTTP and FTP.
brew 'wget'

##
# Version control
#
# We prefer `git` version control. We also work on a wide
# range of systems, so we also sometimes use CVS, HG, and SVN.
##

# CVS is a version control system.
brew 'cvs'

# Git is a free and open source distributed version control system.
#
# TODO: why do we need brew 'git' and also cask 'git'?
brew 'git'
cask 'git'

# TODO
brew 'git-cola'

# Git extras: utilities including summary, repl, population, etc.
cask 'git-extras'

# Git extensions to provide high-level operations for Git Flow branching model.
brew 'git-flow'

# TODO
brew 'git-ftp'

# TODO
brew 'git-gerrit'

# TODO
brew 'git-multipush'

# TODO
brew 'git-now'

# TODO
brew 'git-url-sub'

# SourceTree graphic client for git
cask 'sourcetree'

# Mercurial version control system.
brew 'hg'

# Subversion version control system.
#
# TODO: brew 'sqlite' && brew 'subversion'
brew 'subversion'

##
# GNU command line tools
#
# If you are moving onto macOS from GNU/Linux, then you would probably
# find out that the command line tools shipped with macOS are not as
# powerful and easy to use as the tools in Linux. The reason is that
# macOS uses the BSD version command line tools, which are different
# from the Linux version.
#
# Note: if you choose to replace the macOS commands with GNU commands,
# then be aware that you may have some compatibility issues with shell
# scripts written specifically for macOS.
#
# If you like using man pages, then you may also want to add an
# itemto the to the MANPATH environmental variable:
#
#     $HOMEBREW_PREFIX/opt/coreutils/libexec/gnuman
#
# For more about the GNU command line tools and brew, see this:
# https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/
##

# Basic file, shell and text manipulation utilities of the GNU operating system.
brew 'coreutils'

brew 'binutils'
brew 'diffutils'
brew 'ed'
brew 'findutils'
brew 'gawk'
brew 'gnu-indent'
brew 'gnu-sed'
brew 'gnu-tar'
brew 'gnu-which'
brew 'gnutls'
brew 'gzip'
brew 'watch'
brew 'wdiff'

##
# Some GNU command line tools already exist by default on OS X.
# We choose to replace these with newer versions.
##

brew 'gdb'  # gdb requires further actions to make it work. See `brew info gdb`.
brew 'gpatch'
brew 'less'
brew 'm4'
brew 'make'
brew 'nano'

##
# System related
#
# These are fundamental operating system tools that we use often.
##

# Automake is a tool for automatically generating Makefile installation files.
brew 'automake'

# GNU Privacy Guard (GnuPG) provides encryption as a free replacement for PGP.
brew 'gpg'

# OpenSSL is an open-source implementation of the SSL and TLS protocols.
brew 'openssl'

# pkg-config is a helper tool used when compiling applications and libraries.
brew 'pkg-config && brew link pkg-config && brew install tmux'

# Functions for use by applications that allow users to edit command lines while typing.
brew 'readline'

# Parallel SSH
brew 'pssh'

# pkg-config is a helper tool used when compiling applications and libraries.
brew 'pkg-config'

# PCRE: Perl-compatible regular expressions, for better searching.
brew 'pcre'
brew 'pcre++'

##
# File compression/uncompression
#
# We prefer `zstd` because it is the best modern compression.
##

# Zstandard is the best modern compression
brew 'zstd'

# WinRAR provides compression/decompression for RAR and ZIP files.
brew 'unrar'

# unzip is the classic command.
brew 'homebrew/dupes/unzip'

##
# File synchronization
#
# We use `rsync` for our systems administration,
# and a variety of web-based services for file sharing.
##

# rsync is the classic unix file synchronizer.
brew 'homebrew/dupes/rsync'

# Unison is a high-level file synchronization utility.
brew 'unison'

# Syncthing is open source file sharing.
brew 'syncthing'

# Dropbox file sharing.
cask 'dropbox'

# Transmission bittorrent client.
cask 'transmission'

# Box.com sync
cask 'box-sync'

##
# Text search
#
# We prefer ripgrep because it is very fast and very safe.#
##

# ripgrep is text search; we prefer it over grep, ag, git grep, ucg, pt, sift.
brew 'https://raw.githubusercontent.com/BurntSushi/ripgrep/master/pkg/brew/ripgrep.rb'

# grep is the classic searcher
brew 'grep'

# ag is "the silver searcher" search tool; retired by ripgrep.
brew 'ag'

# sift is like grep, plus faster and with more features; retired by ripgrep.
brew install sift

# jq is a lightweight and flexible command-line JSON processor.
brew 'jq'

##
# Google software
#
# We use Chrome, Drive, Earth, Music, etc.
##

# Google Chrome web browser
cask 'google-chrome'

# Google Drive cloud file storage
cask 'google-drive'

# Google Earth viewer for satellite imagery and maps.
cask 'google-earth'

# Google Music plays songs, especially with a subscription service.
cask 'google-music'

# TDB
cask 'google-notifier'

# TDB
cask 'google-quick-search-box'

# TDB
cask 'google-refine'

# TDB
cask 'google-web-designer'


##################### TODO ####################################

# GraphicsMagick is the swiss army knife of image processing.
brew 'graphicsmagick'

# TODO
brew 'graphviz'

# Gnuplot is a portable command-line driven graphing utility.
brew 'gnuplot'

# TODO
brew 'html-xml-utils'

# TODO
brew 'lynx'

# Most is a powerful paging program; compare `less` and `more`.
brew 'most'

# Mutt is a small powerful text-based mail client.
brew 'mutt'

# Netcat is a networking utility for the TCP/IP protocol.
brew 'netcat'

# TODO
brew 'ncdu'

# TODO
brew 'randomize-lines'

# TODO
brew 'rename'

# TODO
brew 'salt'

# Tree is a directory lister that shows a tree outline
brew 'tree'

# xclip is a command line interface to the X11 clipboard.
brew 'xclip'

## Server-Related

# Docker software containers to help distribute applications.
brew 'docker'
brew 'boot2docker'

# Monit is for managing and monitoring Unix systems.
brew 'monit'

# Nagios IT infrastructure monitoring.
brew 'nagios'

# TODO
brew 'nginx'

# Varnish reverse-proxy web application accelerator.
brew 'varnish'

## Media-Related

brew 'exif'
brew 'exiftags'
brew 'exiftool'
brew 'flac'
brew 'ffmpeg'
brew 'ffmpeg2theora'
brew 'ffmpegthumbnailer'
brew 'imagemagick'
brew 'kindle'
brew 'theora'

##
# Font-Related
##

# Fontconfig is a library for configuring and customizing font access.
brew 'fontconfig'

# FreeType is a freely available software library to render fonts.
brew 'freetype'

##
# Image-Related
##

brew 'libgphoto2'
brew 'libpng'
brew 'libtiff'

# Jasper command line transcoder between JPEG2000 and other formats.
brew 'jasper'

## Uncategorized

brew 'abook'
brew 'ack'
brew 'apachetop'
brew 'apple-gcc42'
brew 'ascii'
brew 'asciidoc'
brew 'asciitex'
brew 'autobench'
brew 'autoconf'
brew 'autoenv'
brew 'autogen'
brew 'autojump'
brew 'base64'
brew 'bcrypt'
brew 'bind'
brew 'bison'
brew 'bogofilter'
brew 'colordiff'
brew 'ctags'
brew 'docbook'
brew 'dovecot'
brew 'doxygen'
brew 'dpkg'
brew 'fakeroot'
brew 'findutils'
brew 'geoip'
brew 'gnu-barcode'
brew 'gnu-getopt'
brew 'gnu-indent'
brew 'gnu-prolog'
brew 'gnu-sed --default-names'
brew 'gnu-smalltalk'
brew 'gnu-tar'
brew 'gnu-time'
brew 'gnu-typist'
brew 'gnu-units'
brew 'gnu-which'
brew 'google-app-engine'
brew 'google-js-test'
brew 'google-perftools'
brew 'google-sparsehash'
brew 'google-sql-tool'
brew 'html2text'
brew 'htop'
brew 'httperf'
brew 'ical-buddy'
brew 'jmeter'
brew 'jpeg'
brew isntall libdnet
brew 'lzo'
brew 'rarian'
brew 'pixman'

# libMemcached is a client library and tools for the memcached server.
brew 'libmemcached'
brew 'memcached'

brew 'scrypt'
brew 'qt5'

# Tarsnap is a secure online backup service for Unix.
brew 'tarsnap'

# Valkyrie is a Qt4-based GUI for the Memcheck and Helgrind tools in Valgrind.
# Commented-out because it's currently incompatible with macOS 10.12.
#brew 'valkyrie'

# WINE runs Windows applications on other operating systems.
brew 'wine'

# Xapian is an open-source search engine library.
brew 'xapian'

##
# Dupes
#
# These formulas duplicate software provided by OS X,
# though may provide more recent or bugfix versions.
#
# We prefer to keep these explicitly listed in `/dupes`
# because these are potentially shadowing system tools,
# and we want to show that these are unusual and special.
#
# If you prefer to type less, then you can tap, like this:
#
#     brew tap homebrew/dupes
#
# Then you can install any forumla, such as:
#
#     brew 'awk'
#
##

brew 'homebrew/dupes/awk'
brew 'homebrew/dupes/diffstat'
brew 'homebrew/dupes/diffutils'
brew 'homebrew/dupes/ed'
brew 'homebrew/dupes/expect'
brew 'homebrew/dupes/fetchmail'
brew 'homebrew/dupes/file-formula'
brew 'homebrew/dupes/gdb'
brew 'homebrew/dupes/gpatch'
brew 'homebrew/dupes/gperf'
brew 'homebrew/dupes/grep'
brew 'homebrew/dupes/groff'
brew 'homebrew/dupes/gzip'
brew 'homebrew/dupes/heimdal'
brew 'homebrew/dupes/lapack'
brew 'homebrew/dupes/less'
brew 'homebrew/dupes/libedit'
brew 'homebrew/dupes/libiconv'
brew 'homebrew/dupes/libpcap'
brew 'homebrew/dupes/lsof'
brew 'homebrew/dupes/m4'
brew 'homebrew/dupes/make'
brew 'homebrew/dupes/nano'
brew 'homebrew/dupes/ncurses'
brew 'homebrew/dupes/openldap'
brew 'homebrew/dupes/openssh'
brew 'homebrew/dupes/screen'
brew 'homebrew/dupes/tcl-tk'
brew 'homebrew/dupes/tcpdump'
brew 'homebrew/dupes/tidy'
brew 'homebrew/dupes/units'
brew 'homebrew/dupes/whois'
brew 'homebrew/dupes/zlib'

##
# Brew cask enables installing typical Mac OS X applications.
# For example, these formulas may download a `*.dmg` file,
# then unpack it into the correct `/Applications` directory,
# and possibly configure the app with typical settings.
##

# Adium is an open source multi-protocol instant messaging client.
cask 'adium'

# TDB
cask 'adventure'

# TDB
cask 'alfred'

# TDB
cask 'amazon-cloud-drive'

# TDB
cask 'amazon-music'

# TDB
cask 'android-file-transfer'

# TDB
cask 'anki'

# AppCleaner thoroughly uninstalls unwanted apps.
cask 'appcleaner'

# TDB
cask 'arq'

# TDB
cask 'atext'

# TDB
cask 'backblaze-downloader'

# TDB
cask 'backuploupe'

# TDB
cask 'balsamiq-mockups'

# TDB
cask 'bartender'

# TDB
cask 'basecamp'

# TDB
cask 'beacon-scanner'

# TDB
cask 'blender'

# TDB
cask 'brain-workshop'

# TDB
cask 'cactus'

# TDB
cask 'caffeine'

# TDB
cask 'calibre'

# TDB
cask 'ccleaner'

# TDB
cask 'cheatsheet'

# TDB
cask 'chromecast'

# TDB
cask 'coconutbattery'

# TDB
cask 'codekit'

# TDB
cask 'commandq'

# TDB
cask 'dash'

# TDB
cask 'doxygen'

# TDB
cask 'duet'

# TDB
cask 'easysimbl'

# TDB
cask 'evernote'

# FileZilla FTP client
cask 'filezilla'

# TDB
cask 'fluid'

# Flux dims the screen colors for better nighttime visibility.
cask 'flux'

# TDB
cask 'freeplane'

# TDB
cask 'ganttproject'

# TDB
cask 'gfxcardstatus'

# GitHub source code social sharing
cask 'github'

# TDB
cask 'gitx'

###################

# TDB
cask 'grooveshark'

# TDB
cask 'harvest'

# TDB
cask 'hockey'

# TDB
cask 'hipchat'

# TDB
cask 'iterm2'

# TDB
cask 'joinme'

# TDB
cask 'jumpcut'

# Kindle book reader by Amazon
cask 'kindle'

# TDB
cask 'krita'

# TDB
cask 'launchy'

# TDB
cask 'little-snitch'

# LibreOffice is a large editor for text, spreadsheets, diagrams.
cask 'libreoffice'

# TODO
cask 'mysqlworkbench'

# TODO
cask 'p4merge'

# Pandora music player
cask 'pandora-one'

# TODO
cask 'paparazzi'

# Prezi slide show presentation.
cask 'prezi'

# TODO
cask 'pupil'

# TODO
cask 'quicksilver'

# Rdio music player.
cask 'rdio'

# TODO
cask 'rescuetime'

# Screenhero screen sharing by Slack.
cask 'screenhero'

# TODO
cask 'sequential'

# TODO
cask 'shortcat'

# Silverlight video player by Microsoft.
cask 'silverlight'

# TODO
cask 'skitch'

# Skype calling with video and phone calls.
cask 'skype'

# Discord chat
cask 'discord'

# Slack chat client
cask 'slack'

# TODO
cask 'sleep-monitor'

# Sophos anti virus
cask 'sophos-anti-virus-home-edition'

# TODO
cask 'sourcetree'

# Spotify music player
cask 'spotify'

# TODO
cask 'superduper'

# Synergy screen sharing utility
cask 'synergy'

# TODO
cask 'thisservice'

# Thunderbird email client by Mozilla.
cask 'thunderbird'

# TODO
cask 'transmit'

# TODO
cask 'todoist'

# TODO
cask 'todos'

# Unison file synchronizer.
cask 'unison'

# VLC media player
cask 'vlc'

##
# Extras
#
# These are packages that we may want.
#
# If you want any of these, please let us know,
# or create a pull request for this repository.
#
# Applications that we want that are not on brew:
#
#   * Kiwix
#   * SoapUI
#
# Applications that we want that we need to find:
#
#   * Automator
#   * Battery Health
#   * Cloud
#   * Coffitivity
#   * Disk Diag
#   * Docs for Xcode
#   * DxO Perspective
#   * Facebook
#   * Font Book
#   * Fotor
#   * Garmin
#   * Gmail
#   * Image Capture
#   * MailTab for Gmail
#   * Memory Clean
#   * MenuBar Stats
#   * Microsoft Remote Desktop
#   * Mint QuickView
#   * Prepo
#   * Screen Recorder Robot Lite
#   * Stickies
#   * Tab for Reddit
#   * The Unarchiver
#   * Time Machine
#   * Twitter
#   * VirtualDJ
#   * Wunderlist
#   * Xcode
#   * xScan
#
# Apple built-in apps:
#
#   * App Store
#   * Apple Configurator
#   * Calculator
#   * Calendar
#   * Chess
#   * Contacts
#   * DVD Player
#   * Dashboard
#   * Dictionary
#   * FaceTime
#   * Game Center
#   * GarageBand
#   * iBooks
#   * iCloud
#   * iMovie
#   * iPhoto
#   * iTunes
#   * iWork
#   * Keynote
#   * Launchpad
#   * Mail
#   * Maps
#   * Messages
#   * Mission Control
#   * Notes
#   * Numbers
#   * Pages
#   * Photo Booth
#   * Preview
#   * QuickTime Player
#   * Reminders
#   * Safari
#   * System Preferences
#   * TextEdit
##

# brew 'aws-cfn-tools'
# brew 'aws-cloudsearch'
# brew 'aws-elasticache'
# brew 'aws-iam-tools'
# brew 'aws-sns-cli'
# brew 'dart'
# brew 'json-c'
# brew 'json-glib'
# brew 'json_spirit'
# brew 'jsonpp'
# brew 'jstalk'
# brew 'jsvc'
# brew 'judy'
# brew 'justniffer'
# brew 'jython'
# brew 'kawa'
# brew 'kbtin'
# brew 'kdiff3'
# brew 'kelbt'
# brew 'kes'
# brew 'keychain'
# brew 'kismet'
# brew 'kite'
# brew 'kiwi'
# brew 'knife-completion'
# brew 'knock'
# brew 'konoha'
# brew 'ktoblzcheck'
# brew 'kumofs'
# brew 'kyoto-cabinet'
# brew 'kyoto-tycoon'
# brew 'kytea'
# brew 'lablgtk'
# brew 'lame'
# brew 'languagetool'
# brew 'lapack'
# brew 'lasi'
# brew 'lastfm_fplib'
# brew 'lastfmfpclient'
# brew 'lastfmlib'
# brew 'latex2html'
# brew 'latex2rtf'
# brew 'launch'
# brew 'lbdb'
# brew 'lcdf-typetools'
# brew 'lcov'
# brew 'lcrack'
# brew 'ldapvi'
# brew 'ldid'
# brew 'ldns'
# brew 'le'
# brew 'leafnode'
# brew 'ledger'
# brew 'ledit'
# brew 'legit'
# brew 'lemon'
# brew 'leptonica'
# brew 'less'
# brew 'lesspipe'
# brew 'lesstif'
# brew 'leveldb'
# brew 'lft'
# brew 'lftp'
# brew 'lha'
# brew 'libagg'
# brew 'libao'
# brew 'libarchive'
# brew 'libart'
# brew 'libass'
# brew 'libassuan'
# brew 'libbinio'
# brew 'libbs2b'
# brew 'libcaca'
# brew 'libcddb'
# brew 'libcdio'
# brew 'libcmph'
# brew 'libconfig'
# brew 'libcouchbase'
# brew 'libcroco'
# brew 'libcsv'
# brew 'libcue'
# brew 'libcuefile'
# brew 'libdaemon'
# brew 'libdap'
# brew 'libdbusmenu-qt'
# brew 'libdc1394'
# brew 'libdca'
# brew 'libdlna'
# brew 'libdmtx'
# brew 'libdnet'
# brew 'libdrizzle'
# brew 'libdshconfig'
# brew 'libdsk'
# brew 'libdv'
# brew 'libdvbpsi'
# brew 'libdvdcss'
# brew 'libdvdnav'
# brew 'libdvdread'
# brew 'libebml'
# brew 'libechonest'
# brew 'libelf'
# brew 'libemu'
# brew 'libev'
# brew 'libevent'
# brew 'libewf'
# brew 'libexif'
# brew 'libexosip'
# brew 'libextractor'
# brew 'libffi'
# brew 'libfishsound'
# brew 'libfixbuf'
# brew 'libflowmanager'
# brew 'libftdi'
# brew 'libgadu'
# brew 'libgaiagraphics'
# brew 'libgarmin'
# brew 'libgcrypt'
# brew 'libgda'
# brew 'libgee'
# brew 'libgeotiff'
# brew 'libgit2'
# brew 'libglade'
# brew 'libglademm'
# brew 'libgnomecanvas'
# brew 'libgpg-error'
# brew 'libgphoto2'
# brew 'libgsasl'
# brew 'libgsf'
# brew 'libgtextutils'
# brew 'libgtop'
# brew 'libharu'
# brew 'libhid'
# brew 'libical'
# brew 'libicns'
# brew 'libiconv'
# brew 'libid3tag'
# brew 'libident'
# brew 'libidl'
# brew 'libidn'
# brew 'libimobiledevice'
# brew 'libinfinity'
# brew 'libiptcdata'
# brew 'libkate'
# brew 'libkml'
# brew 'libksba'
# brew 'liblas'
# brew 'liblastfm'
# brew 'liblinear'
# brew 'liblo'
# brew 'liblockfile'
# brew 'liblqr'
# brew 'liblunar'
# brew 'libmagic'
# brew 'libmatroska'
# brew 'libmemcached'
# brew 'libmicrohttpd'
# brew 'libmikmod'
# brew 'libming'
# brew 'libmms'
# brew 'libmp3splt'
# brew 'libmpc'
# brew 'libmpd'
# brew 'libmpdclient'
# brew 'libmpeg2'
# brew 'libmtp'
# brew 'libmusicbrainz'
# brew 'libmxml'
# brew 'libnet'
# brew 'libnfc'
# brew 'libnids'
# brew 'libogg'
# brew 'liboil'
# brew 'libopennet'
# brew 'liboping'
# brew 'libosip'
# brew 'libotr'
# brew 'libpano'
# brew 'libpar2'
# brew 'libpcap'
# brew 'libplist'
# brew 'libpst'
# brew 'libpurple'
# brew 'libpuzzle'
# brew 'libqalculate'
# brew 'libqglviewer'
# brew 'libquicktime'
# brew 'librasterlite'
# brew 'libraw'
# brew 'libreplaygain'
# brew 'librets'
# brew 'librsvg'
# brew 'libsamplerate'
# brew 'libsgml'
# brew 'libshout'
# brew 'libsigc++'
# brew 'libsigsegv'
# brew 'libsmi'
# brew 'libsndfile'
# brew 'libspatialite'
# brew 'libspiro'
# brew 'libspotify'
# brew 'libssh'
# brew 'libssh2'
# brew 'libstfl'
# brew 'libstxxl'
# brew 'libsvg'
# brew 'libsvg-cairo'
# brew 'libsvm'
# brew 'libtasn1'
# brew 'libtecla'
# brew 'libtermkey'
# brew 'libtiff'
# brew 'libtommath'
# brew 'libtool'
# brew 'libtorrent'
# brew 'libtorrent-rasterbar'
# brew 'libtrace'
# brew 'libunique'
# brew 'libunistring'
# brew 'libupnp'
# brew 'libusb'
# brew 'libusb-compat'
# brew 'libutf'
# brew 'libvbucket'
# brew 'libvirt'
# brew 'libvo-aacenc'
# brew 'libvorbis'
# brew 'libvpx'
# brew 'libwbxml'
# brew 'libwmf'
# brew 'libwpd'
# brew 'libwpg'
# brew 'libwps'
# brew 'libxdiff'
# brew 'libxmi'
# brew 'libxml++'
# brew 'libxml2'
# brew 'libxmlsec1'
# brew 'libxslt'
# brew 'libxspf'
# brew 'libyaml'
# brew 'libyubikey'
# brew 'libzdb'
# brew 'libzip'
# brew 'libzzip'
# brew 'lifelines'
# brew 'lightning'
# brew 'lighttpd'
# brew 'lilypond'
# brew 'link-grammar'
# brew 'linklint'
# brew 'links'
# brew 'liquibase'
# brew 'litmus'
# brew 'little-cms'
# brew 'little-cms2'
# brew 'llvm'
# brew 'lmutil'
# brew 'lockrun'
# brew 'log4cplus'
# brew 'log4cpp'
# brew 'log4cxx'
# brew 'log4shib'
# brew 'logcheck'
# brew 'logentries'
# brew 'logrotate'
# brew 'logstalgia'
# brew 'logtalk'
# brew 'lolcode'
# brew 'lorem'
# brew 'loudmouth'
# brew 'lout'
# brew 'lpc21isp'
# brew 'lrzip'
# brew 'lrzsz'
# brew 'lsdvd'
# brew 'lsof'
# brew 'lua'
# brew 'luajit'
# brew 'luarocks'
# brew 'luciddb'
# brew 'lv'
# brew 'lxsplit'
# brew 'lynx'
# brew 'lysp'
# brew 'lzip'
# brew 'lzlib'
# brew 'lzo'
# brew 'lzop'
# brew 'm4'
# brew 'mac-robber'
# brew 'macvim'
# brew 'mad'
# brew 'madplay'
# brew 'mafft'
# brew 'magit'
# brew 'mailcheck'
# brew 'mairix'
# brew 'make'
# brew 'makeicns'
# brew 'makensis'
# brew 'malbolge'
# brew 'mame'
# brew 'man2html'
# brew 'mapnik'
# brew 'mapserver'
# brew 'mariadb'
# brew 'markdown'
# brew 'mathgl'
# brew 'mathomatic'
# brew 'maven-shell'
# brew 'mawk'
# brew 'maxima'
# brew 'mcabber'
# brew 'mcl'
# brew 'mcpp'
# brew 'mcrypt'
# brew 'md'
# brew 'md5deep'
# brew 'md5sha1sum'
# brew 'mdbtools'
# brew 'mdf2iso'
# brew 'mdxmini'
# brew 'mecab'
# brew 'mecab-ipadic'
# brew 'media-info'
# brew 'mediatomb'
# brew 'memcache-top'
# brew 'memcached'
# brew 'memcacheq'
# brew 'memtester'
# brew 'mercurial'
# brew 'mesalib-glw'
# brew 'mess'
# brew 'metalua'
# brew 'metapixel'
# brew 'metaproxy'
# brew 'metasploit'
# brew 'metis'
# brew 'mftrace'
# brew 'mg'
# brew 'mhash'
# brew 'midgard2'
# brew 'midnight-commander'
# brew 'mikmod'
# brew 'minbif'
# brew 'minc'
# brew 'minicom'
# brew 'minisat'
# brew 'minised'
# brew 'miniupnpc'
# brew 'minuit2'
# brew 'mira'
# brew 'mit-scheme'
# brew 'mjpegtools'
# brew 'mkclean'
# brew 'mkcue'
# brew 'mksh'
# brew 'mktorrent'
# brew 'mkvalidator'
# brew 'mkvtoolnix'
# brew 'mldonkey'
# brew 'mlton'
# brew 'mmv'
# brew 'mobile-shell'
# brew 'mod_python'
# brew 'mod_wsgi'
# brew 'mogenerator'
# brew 'monetdb'
# brew 'mongoose'
# brew 'mongrel2'
# brew 'monotone'
# brew 'montage'
# brew 'moreutils'
# brew 'mosh'
# brew 'mosml'
# brew 'mosquitto'
# brew 'movgrab'
# brew 'mp3cat'
# brew 'mp3check'
# brew 'mp3gain'
# brew 'mp3info'
# brew 'mp3splt'
# brew 'mp3val'
# brew 'mp3wrap'
# brew 'mp4v2'
# brew 'mpack'
# brew 'mpc'
# brew 'mpd'
# brew 'mpdas'
# brew 'mpdscribble'
# brew 'mpfr'
# brew 'mpg123'
# brew 'mpg321'
# brew 'mpgtx'
# brew 'mpich2'
# brew 'mpio'
# brew 'mplayer'
# brew 'mpop'
# brew 'mpsolve'
# brew 'mr'
# brew 'mrfast'
# brew 'mrtg'
# brew 'mscgen'
# brew 'msgpack'
# brew 'msgpack-rpc'
# brew 'msmtp'
# brew 'mt-daapd'
# brew 'mtools'
# brew 'mtr'
# brew 'mu'
# brew 'multimarkdown'
# brew 'multitail'
# brew 'muparser'
# brew 'mupdf'
# brew 'muscle'
# brew 'musepack'
# brew 'mydumper'
# brew 'mytop'
# brew 'n2n'
# brew 'nacl'
# brew 'nagios'
# brew 'nagios-plugins'
# brew 'nailgun'
# brew 'nano'
# brew 'narwhal'
# brew 'nasm'
# brew 'naturaldocs'
# brew 'nauty'
# brew 'ncdu'
# brew 'ncftp'
# brew 'ncmpc'
# brew 'ncmpcpp'
# brew 'ncrack'
# brew 'ncurses'
# brew 'ncview'
# brew 'ndiff'
# brew 'neko'
# brew 'neo4j'
# brew 'neon'
# brew 'nesc'
# brew 'net-nuclear'
# brew 'net-snmp'
# brew 'net6'
# brew 'netcat'
# brew 'netcdf'
# brew 'netpbm'
# brew 'netsed'
# brew 'nettle'
# brew 'newick-utils'
# brew 'newlisp'
# brew 'ngircd'
# brew 'ngrep'
# brew 'ngspice'
# brew 'nickle'
# brew 'nimrod'
# brew 'nkf'
# brew 'nload'
# brew 'nlopt'
# brew 'nmap'
# brew 'node'
# brew 'notmuch'
# brew 'noweb'
# brew 'nrg2iso'
# brew 'nrpe'
# brew 'nspr'
# brew 'nss'
# brew 'ntfs-3g'
# brew 'ntl'
# brew 'nu'
# brew 'num-utils'
# brew 'nuttcp'
# brew 'nvi'
# brew 'nylon'
# brew 'nzbget'
# brew 'o-make'
# brew 'oath-toolkit'
# brew 'obby'
# brew 'objective-caml'
# brew 'ocp'
# brew 'ocrad'
# brew 'octave'
# brew 'ode'
# brew 'odt2txt'
# brew 'offline-imap'
# brew 'oggz'
# brew 'ogmtools'
# brew 'ohcount'
# brew 'omega'
# brew 'oniguruma'
# brew 'oorexx'
# brew 'open-babel'
# brew 'open-cobol'
# brew 'open-mesh'
# brew 'open-mpi'
# brew 'open-ocd'
# brew 'open-scene-graph'
# brew 'open-sg'
# brew 'open-sp'
# brew 'open-vcdiff'
# brew 'opencc'
# brew 'opencolorio'
# brew 'openconnect'
# brew 'opencore-amr'
# brew 'opencv'
# brew 'openexr'
# brew 'openfst'
# brew 'openimageio'
# brew 'openjpeg'
# brew 'openldap'
# brew 'openmeeg'
# brew 'opensaml'
# brew 'openslp'
# brew 'opentracker'
# brew 'openttd'
# brew 'openvpn'
# brew 'ophcrack'
# brew 'optipng'
# brew 'opus'
# brew 'opus-tools'
# brew 'orbit'
# brew 'orc'
# brew 'orpie'
# brew 'ortp'
# brew 'osm-pbf'
# brew 'osm2pgsql'
# brew 'osmosis'
# brew 'osslsigncode'
# brew 'ossp-uuid'
# brew 'otx'
# brew 'owfs'
# brew 'p0f'
# brew 'p11-kit'
# brew 'p7zip'
# brew 'pam_yubico'
# brew 'paml'
# brew 'pango'
# brew 'pangomm'
# brew 'paperkey'
# brew 'par'
# brew 'par2'
# brew 'par2tbb'
# brew 'parallel'
# brew 'pari'
# brew 'parmetis'
# brew 'parrot'
# brew 'patchutils'
# brew 'pathfinder'
# brew 'pax-construct'
# brew 'pax-runner'
# brew 'pbc'
# brew 'pbc-sig'
# brew 'pbzip2'
# brew 'pcal'
# brew 'pcb'
# brew 'pdal'
# brew 'pdf2image'
# brew 'pdf2json'
# brew 'pdf2svg'
# brew 'pdfcrack'
# brew 'pdfgrep'
# brew 'pdfjam'
# brew 'pdflib-lite'
# brew 'pdftohtml'
# brew 'pdksh'
# brew 'pdnsd'
# brew 'pdsh'
# brew 'peg'
# brew 'peg-markdown'
# brew 'perceptualdiff'
# brew 'percona-server'
# brew 'percona-toolkit'
# brew 'perforce'
# brew 'perforce-proxy'
# brew 'perforce-server'
# brew 'perl'
# brew 'pg_top'
# brew 'pgbouncer'
# brew 'pgdbf'
# brew 'pgpool-ii'
# brew 'pgtap'
# brew 'phantomjs'
# brew 'phash'
# brew 'phoronix-test-suite'
# brew 'phyml'
# brew 'physfs'
# brew 'pianobar'
# brew 'picoc'
# brew 'picocom'
# brew 'pidof'
# brew 'pig'
# brew 'pigz'
# brew 'pil'
# brew 'pincaster'
# brew 'pinentry'
# brew 'pipebench'
# brew 'pipemeter'
# brew 'pit'
# brew 'pixie'
# brew 'pixman'
# brew 'pkg-config'
# brew 'play'
# brew 'playdar'
# brew 'plink'
# brew 'plod'
# brew 'plotutils'
# brew 'plowshare'
# brew 'plt-racket'
# brew 'plustache'
# brew 'plzip'
# brew 'pmdmini'
# brew 'pms'
# brew 'png2ico'
# brew 'pngcheck'
# brew 'pngcrush'
# brew 'pngnq'
# brew 'pngrewrite'
# brew 'poco'
# brew 'podofo'
# brew 'points2grid'
# brew 'polipo'
# brew 'polyml'
# brew 'poppler'
# brew 'popt'
# brew 'portaudio'
# brew 'portmidi'
# brew 'pos'
# brew 'poster'
# brew 'postgis'
# brew 'postgresql'
# brew 'postmark'
# brew 'potrace'
# brew 'pound'
# brew 'povray'
# brew 'pow'
# brew 'ppl'
# brew 'ppss'
# brew 'premake'
# brew 'primer3'
# brew 'primesieve'
# brew 'privoxy'
# brew 'proctools'
# brew 'prodigal'
# brew 'proguard'
# brew 'proj'
# brew 'proxytunnel'
# brew 'psftools'
# brew 'psgrep'
# brew 'pstoedit'
# brew 'pstree'
# brew 'pth'
# brew 'ptunnel'
# brew 'puf'
# brew 'pulledpork'
# brew 'pure'
# brew 'pure-ftpd'
# brew 'putmail'
# brew 'putmail-queue'
# brew 'putty'
# brew 'pv'
# brew 'pwgen'
# brew 'pwnat'
# brew 'pwsafe'
# brew 'py2cairo'
# brew 'pygobject'
# brew 'pygtk'
# brew 'pygtkglext'
# brew 'pypy'
# brew 'pyqt'
# brew 'pyqwt'
# brew 'pyside'
# brew 'pyside-tools'
# brew 'qca'
# brew 'qcachegrind'
# brew 'qd'
# brew 'qdbm'
# brew 'qemu'
# brew 'qfits'
# brew 'qhull'
# brew 'qi'
# brew 'qjson'
# brew 'qpdf'
# brew 'qprint'
# brew 'qrencode'
# brew 'qrupdate'
# brew 'qscintilla2'
# brew 'qstat'
# brew 'qt-mobility'
# brew 'quantlib'
# brew 'quassel'
# brew 'quex'
# brew 'quickfix'
# brew 'quicktree'
# brew 'quilt'
# brew 'quvi'
# brew 'qwt'
# brew 'qxmpp'
# brew 'radare2'
# brew 'ragel'
# brew 'rails-completion'
# brew 'rakudo-star'
# brew 'ranger'
# brew 'raptor'
# brew 'rarian'
# brew 'rasqal'
# brew 'rats'
# brew 'rbenv'
# brew 'rbenv-gemset'
# brew 'rbenv-vars'
# brew 'rc'
# brew 'rdesktop'
# brew 'rdiff-backup'
# brew 'rds-command-line-tools'
# brew 're2'
# brew 're2c'
# brew 'readline'
# brew 'readosm'
# brew 'readpst'
# brew 'reattach-to-user-namespace'
# brew 'rebar'
# brew 'recode'
# brew 'recutils'
# brew 'redis'
# brew 'redis-tools'
# brew 'redland'
# brew 'redo'
# brew 'redsocks'
# brew 'regina-rexx'
# brew 'remind'
# brew 'ren'
# brew 'rename'
# brew 'renameutils'
# brew 'repl'
# brew 'repo'
# brew 'reposurgeon'
# brew 'resty'
# brew 'rfcdiff'
# brew 'rfcmarkup'
# brew 'rfcstrip'
# brew 'rhino'
# brew 'riak'
# brew 'riak-search'
# brew 'riemann'
# brew 'rinetd'
# brew 'ringojs'
# brew 'ripmime'
# brew 'rlog'
# brew 'rlwrap'
# brew 'rmcast'
# brew 'rmtrash'
# brew 'rnv'
# brew 'robodoc'
# brew 'rock'
# brew 'rogue'
# brew 'rom-tools'
# brew 'roundup'
# brew 'rpg'
# brew 'rpl'
# brew 'rpm2cpio'
# brew 'rrdtool'
# brew 'rsense'
# brew 'rsnapshot'
# brew 'rsyslog'
# brew 'rt-audio'
# brew 'rtmpdump'
# brew 'rtorrent'
# brew 'rtpbreak'
# brew 'rubber'
# brew 'rubinius'
# brew 'ruby'
# brew 'ruby-build'
# brew 'ruby-enterprise-edition'
# brew 'ruby-odbc'
# brew 'runcocoa'
# brew 'runit'
# brew 'rush'
# brew 'rust'
# brew 'rxvt-unicode'
# brew 'rzip'
# brew 's-lang'
# brew 's3-backer'
# brew 's3cmd'
# brew 's3fs'
# brew 's3sync'
# brew 'saga-core'
# brew 'salt'
# brew 'sam2p'
# brew 'samba'
# brew 'samtools'
# brew 'sane-backends'
# brew 'sary'
# brew 'savana'
# brew 'saxon'
# brew 'saxon-b'
# brew 'sbcl'
# brew 'sbt'
# brew 'sc68'
# brew 'scalate'
# brew 'scalpel'
# brew 'scamperema'
# brew 'scantailor'
# brew 'scheme48'
# brew 'schroedinger'
# brew 'scm-manager'
# brew 'scons'
# brew 'scotch'
# brew 'screen'
# brew 'scrollkeeper'
# brew 'scrotwm'
# brew 'scrub'
# brew 'scrypt'
# brew 'scsh'
# brew 'scummvm'
# brew 'sdcc'
# brew 'sdelta3'
# brew 'sdf'
# brew 'sdl'
# brew 'sdl_gfx'
# brew 'sdl_image'
# brew 'sdl_mixer'
# brew 'sdl_net'
# brew 'sdl_rtf'
# brew 'sdl_sound'
# brew 'sdl_ttf'
# brew 'sedna'
# brew 'selenium-server-standalone'
# brew 'ser2net'
# brew 'serf'
# brew 'sersniff'
# brew 'sgrep'
# brew 'shakespeare'
# brew 'shapelib'
# brew 'shaper-probe'
# brew 'shared-mime-info'
# brew 'shark'
# brew 'shell.fm'
# brew 'shen'
# brew 'shiboken'
# brew 'shmux'
# brew 'shntool'
# brew 'shocco'
# brew 'shorten'
# brew 'shtool'
# brew 'sic'
# brew 'sickbeard'
# brew 'sigar'
# brew 'signing-party'
# brew 'silk'
# brew 'simgrid'
# brew 'simh'
# brew 'since'
# brew 'sip'
# brew 'sipcalc'
# brew 'sipp'
# brew 'sipsak'
# brew 'sisc-scheme'
# brew 'sispmctl'
# brew 'sitecopy'
# brew 'ski'
# brew 'skipfish'
# brew 'skktools'
# brew 'skytools'
# brew 'sl'
# brew 'sleepwatcher'
# brew 'sleuthkit'
# brew 'sloccount'
# brew 'slrn'
# brew 'smake'
# brew 'smartmontools'
# brew 'smartypants'
# brew 'smlnj'
# brew 'smpeg'
# brew 'snappy'
# brew 'snobol4'
# brew 'snort'
# brew 'sntop'
# brew 'socat'
# brew 'sofia-sip'
# brew 'solid'
# brew 'solr'
# brew 'sonar'
# brew 'sound-touch'
# brew 'source-highlight'
# brew 'sox'
# brew 'spark'
# brew 'spatialindex'
# brew 'spatialite-tools'
# brew 'spawn-fcgi'
# brew 'speex'
# brew 'sphinx'
# brew 'spidermonkey'
# brew 'spim'
# brew 'spin'
# brew 'spiped'
# brew 'splint'
# brew 'spring-roo'
# brew 'sproxy'
# brew 'sqsh'
# brew 'squashfs'
# brew 'squid'
# brew 'squirrel'
# brew 'srecord'
# brew 'ssdeep'
# brew 'ssed'
# brew 'ssh-copy-id'
# brew 'sshfs'
# brew 'sshguard'
# brew 'sshuttle'
# brew 'ssldump'
# brew 'sslscan'
# brew 'ssss'
# brew 'stanford-parser'
# brew 'star'
# brew 'staticrouted'
# brew 'stgit'
# brew 'stklos'
# brew 'storm'
# brew 'stormfs'
# brew 'stow'
# brew 'stp'
# brew 'strategoxt'
# brew 'streamripper'
# brew 'stress'
# brew 'stunnel'
# brew 'style-check'
# brew 'sub2srt'
# brew 'subversion'
# brew 'suite-sparse'
# brew 'sundials'
# brew 'surfraw'
# brew 'svdlibc'
# brew 'svg2pdf'
# brew 'svg2png'
# brew 'swaks'
# brew 'swfmill'
# brew 'swftools'
# brew 'swi-prolog'
# brew 'swig'
# brew 'swish-e'
# brew 'syck'
# brew 'symphony'
# brew 'synergy'
# brew 'synfig'
# brew 'synfigstudio'
# brew 'syslog-ng'
# brew 'szip'
# brew 'szl'
# brew 't1utils'
# brew 'ta-lib'
# brew 'tabbed'
# brew 'tabix'
# brew 'taglib'
# brew 'tal'
# brew 'talk-filters'
# brew 'talloc'
# brew 'tarsnap'
# brew 'task'
# brew 'tbb'
# brew 'tcl'
# brew 'tclap'
# brew 'tcpdump'
# brew 'tcpflow'
# brew 'tcping'
# brew 'tcpreplay'
# brew 'tcpstat'
# brew 'tcptrace'
# brew 'tcptraceroute'
# brew 'tcptrack'
# brew 'tcpurify'
# brew 'teapot'
# brew 'teem'
# brew 'term'
# brew 'tesseract'
# brew 'testdisk'
# brew 'tetgen'
# brew 'texinfo'
# brew 'thc-pptp-bruter'
# brew 'the_silver_searcher'
# brew 'theora'
# brew 'thrift'
# brew 'thrulay'
# brew 'tidy'
# brew 'tidyp'
# brew 'tiff2png'
# brew 'tig'
# brew 'tiger-vnc'
# brew 'timbl'
# brew 'timedog'
# brew 'tin'
# brew 'tinc'
# brew 'tintin'
# brew 'tiny-fugue'
# brew 'tinyproxy'
# brew 'tinysvm'
# brew 'titlecase'
# brew 'tivodecode'
# brew 'tk'
# brew 'tkdiff'
# brew 'tmap'
# brew 'tmpreaper'
# brew 'tmux'
# brew 'tn5250'
# brew 'tnef'
# brew 'todo-txt'
# brew 'tofrodos'
# brew 'toilet'
# brew 'tokyo-cabinet'
# brew 'tokyo-dystopia'
# brew 'tokyo-tyrant'
# brew 'tomcat'
# brew 'topgit'
# brew 'tophat'
# brew 'tor'
# brew 'torsocks'
# brew 'trafficserver'
# brew 'trafshow'
# brew 'trang'
# brew 'transcode'
# brew 'transmission'
# brew 'tre'
# brew 'tree'
# brew 'treecc'
# brew 'treeline'
# brew 'triangle'
# brew 'tsung'
# brew 'ttf2eot'
# brew 'ttf2pt1'
# brew 'tth'
# brew 'ttyrec'
# brew 'ttytter'
# brew 'tup'
# brew 'two-lame'
# brew 'txt2man'
# brew 'txt2tags'
# brew 'typespeed'
# brew 'uade'
# brew 'uchardet'
# brew 'ucl'
# brew 'udis86'
# brew 'udns'
# brew 'udunits'
# brew 'ufraw'
# brew 'uif2iso'
# brew 'uim'
# brew 'unafold'
# brew 'unbound'
# brew 'uncrustify'
# brew 'unfs3'
# brew 'ungif'
# brew 'unifdef'
# brew 'unison'
# brew 'unittest'
# brew 'unixodbc'
# brew 'unp'
# brew 'unpaper'
# brew 'unrtf'
# brew 'unshield'
# brew 'unyaffs'
# brew 'uptimed'
# brew 'upx'
# brew 'uriparser'
# brew 'urlview'
# brew 'urweb'
# brew 'usbmuxd'
# brew 'ushare'
# brew 'utimer'
# brew 'uudeview'
# brew 'uwsgi'
# brew 'v8'
# brew 'v8cgi'
# brew 'vala'
# brew 'valkyrie'
# brew 'vbindiff'
# brew 'vcdimager'
# brew 'vcftools'
# brew 'vcodex'
# brew 'vcprompt'
# brew 'vde'
# brew 'velvet'
# brew 'verilator'
# brew 'vf'
# brew 'vgmstream'
# brew 'vice'
# brew 'vifm'
# brew 'vilistextum'
# brew 'vimeo-downloader'
# brew 'vimpager'
# brew 'vimpc'
# brew 'vip'
# brew 'vips'
# brew 'virtualhost.sh'
# brew 'virtuoso'
# brew 'visitors'
# brew 'visualnetkit'
# brew 'vmalloc'
# brew 'vnstat'
# brew 'vobcopy'
# brew 'voldemort'
# brew 'vorbis-tools'
# brew 'vorbisgain'
# brew 'vpnc'
# brew 'vrpn'
# brew 'vsftpd'
# brew 'vte'
# brew 'vtk'
# brew 'w3m'
# brew 'wait_on'
# brew 'wakeonlan'
# brew 'watch'
# brew 'wavpack'
# brew 'wbox'
# brew 'wdfs'
# brew 'wdiff'
# brew 'web100clt'
# brew 'webalizer'
# brew 'webfs'
# brew 'webkit2png'
# brew 'webp'
# brew 'weechat'
# brew 'wemux'
# brew 'whatmask'
# brew 'when'
# brew 'whirr'
# brew 'whohas'
# brew 'wiggle'
# brew 'willgit'
# brew 'wine'
# brew 'winetricks'
# brew 'winexe'
# brew 'wkhtmltopdf'
# brew 'wla-dx'
# brew 'wmctrl'
# brew 'wol'
# brew 'wopr'
# brew 'wordnet'
# brew 'wp-cli'
# brew 'wps2odt'
# brew 'wput'
# brew 'wrangler'
# brew 'writerperfect'
# brew 'wrk'
# brew 'wtf'
# brew 'wv'
# brew 'wv2'
# brew 'wwwoffle'
# brew 'wxmac'
# brew 'wyrd'
# brew 'x264'
# brew 'x3270'
# brew 'xa'
# brew 'xapian'
# brew 'xar'
# brew 'xaric'
# brew 'xastir'
# brew 'xaw3d'
# brew 'xchat'
# brew 'xclip'
# brew 'xdelta'
# brew 'xdotool'
# brew 'xerces-c'
# brew 'xml-coreutils'
# brew 'xml-security-c'
# brew 'xml-tooling-c'
# brew 'xml2rfc'
# brew 'xmlformat'
# brew 'xmlrpc-c'
# brew 'xmlto'
# brew 'xmltoman'
# brew 'xmoto'
# brew 'xmp'
# brew 'xpa'
# brew 'xpdf'
# brew 'xplanet'
# brew 'xqilla'
# brew 'xrootd'
# brew 'xspin'
# brew 'xspringies'
# brew 'xsw'
# brew 'xvid'
# brew 'xz'
# brew 'yaf'
# brew 'yajl'
# brew 'yamdi'
# brew 'yaml-cpp'
# brew 'yara'
# brew 'yarp'
# brew 'yasm'
# brew 'yaws'
# brew 'yaz'
# brew 'yazpp'
# brew 'yconalyzer'
# brew 'yeti'
# brew 'ykclient'
# brew 'ykpers'
# brew 'youtube-dl'
# brew 'yuicompressor'
# brew 'yydecode'
# brew 'z'
# brew 'zbar'
# brew 'zdelta'
# brew 'zebra'
# brew 'zeromq'
# brew 'zile'
# brew 'zint'
# brew 'zlib'
# brew 'znc'
# brew 'zookeeper'
# brew 'zsh'
# brew 'zsh-completions'
# brew 'zsh-lovers'
# brew 'zssh'
# brew 'zsync'
# brew 'zzuf'

##
# brew-install-our-base-packages-manually.sh
#
# Use Homebrew to install our favorite typical-user packages
# that may need to be installed manually because of passwords,
# or moving files, or more-complex issues that need a human.
##

## Environment-related

# DisplayLink enables adding monitors
cask 'displaylink'

# Java language for running many applications
cask 'java'

# Karabiner remaps keyboard keys
cask 'karabiner'

## Media-related

# Adobe Air player for multimedia content
cask 'adobe-air'

# Adobe Reader for PDF files
cask 'adobe-reader'


## Misc

cask 'flip4mac'
cask 'google-hangouts'
cask 'inky'
cask 'obs'
cask 'pandoc'
cask 'prey'
cask 'seil'
cask 'teamviewer'
cask 'unity-web-player'
cask 'unity3d'
cask 'zoomus'


## Mac App Store

mas 'Numbers', id: 409203825
mas 'Pages', id: 409201541
mas 'Slack', id: 803453959
mas 'Sip', id: 507257563
mas 'Simplenote', id: 692867256
mas 'Todoist', id: 585829637

##
# brew-install-our-stacks-automatically.sh
#
# Use Homebrew to install our favorite tech-related packages
# that can be installed fully automatically i.e. unattended;
# these packages do not ask for passwords, do not have any
# prompts, and do not have any issues that need a human.
#
# If you're using this file and you find any packages that
# do not install automatically, please let us know by opening
# an issue, or emailing us, or creating a pull request. Thanks!
#
# ## Link
#
# Some of the brew packages need to link to others.
#
#   * `brew link cmake` before mysql
#   * `brew link cmake` before wireshark can be installed
#   * `brew link cmake` before homebrew/science/opencv
#   * `brew link pandoc` before shellcheck can be installed
#
##

##
# System
##

# XQuartz provides X.Org X Window System that runs on OS X.
cask 'xquartz'

##
# Environment
##

# Code Climate Platform for all static analysic
brew tap codeclimate/formulas && brew 'codeclimate'

# Command-line programs for manipulating fonts
brew 'lcdf-typetools'

##
# Shell
##

# GUI for rsync
brew 'grsync'

# Shell script syntax check linter
brew link pandoc; brew 'shellcheck'

# BATS: Bash Automated Testing System
cask 'bats'

##
# Clients
##

# Shuttle: simple SSH shortcut menu
cask 'shuttle'

# Fugu: a graphical shell for SSH and FTP.
cask 'fugu'

# Charles: enables a developer to view HTTP traffic.
cask 'charles'


##
# Languages
##

# Apache Maven is a software project management and comprehension tool.
brew 'maven'

##
# Mac programming
##

# Dash documentation browser and code snippet manager
cask 'dash'

# Realm browser for the Realm embedded database
cask 'realm-browser'

# Tunnelblick remote access VPN
cask 'tunnelblick'

##
# Networking
##

# Wireshark network monitoring, with the QT GUI.
brew link cmake; cask 'wireshark --with-qt'

# Wireshark-chmodbft enables regular users to capture network packets.
cask 'wireshark-chmodbpf'

# Charles web debugging proxy
cask 'charles'

# Siege is an http load testing and benchmarking utility.
brew 'siege'

##
# Virtual environments
##

# Docker assembles applications from components.
cask 'docker'

# Vagrant creates and configures portable development environments.
cask 'vagrant'

# VirtualBox creates and configures portable development environments, by Oracle.
cask 'virtualbox'

# Terraform common configuration to launch infrastructure.
brew 'terraform'

# Kubernetes Solo cluster for macOS
cask 'kube-solo'

##
# IDE
##

# Eclipse is a large programming IDE built on Java
cask 'eclipse-ide'
cask 'eclipse-platform'

##
# Databases
#
# This section installs many databases and database tooling:
# Cassandra, CouchDB, Hadoop, MariaDB, MongoDB, PostgreSQL,
# RabbitMQ, Redis, Riak, Sphinx, SQLite. Notably *not* MySQL.
##

##
# Databases
#
# We like PostgreSQL and a bunch of others.
##

# Cassandra database.
brew 'cassandra'

# CouchDB database, esp. for document-oriented storage.
brew 'couchdb'

# Hadoop database.
brew 'hadoop'

# MariaDB database; prefer this over MySQL.
brew 'mariadb'

# MongoDB database.
brew 'mongodb'

# PostgreSQL database.
brew 'postgres'

# PostgreSQL database.
brew 'postgresql'

# Postgres App provides a Mac-friendly database.
cask 'postgres'

# Postgres admin GUI
brew 'pgadmin3'

# RabbitMQ enterprise message queue based on the emerging AMQP standard.
brew 'rabbitmq'

# Redis database, esp. for key-value cache and store, and data structures.
brew 'redis'

# Riak open-source distributed database.
brew 'riak'

# SQLite database: self-contained, serverless, zero-configuration, transactional engine.
brew 'sqlite && brew link sqlite'

# ZeroMQ message queue
brew 'zeromq'

##
# Database searchers
#
# TODO: add more here
##

# Sphinx search engine.
brew link cmake; brew 'mysql; brew install postgresql; brew install sphinx'

##
# Database managers
#
# TODO: add pgadmin etc.
##

# MySQL Workbench database editor.
brew link cmake; cask 'mysqlworkbench'

# Realm browser mobile database editor.
cask 'realm-browser'

# Sequel Pro database management application.
cask 'sequel-pro'

# Toad database manager by Dell.
cask 'toad'

# Valentina Studio database manager.
cask 'valentina-studio'

##
# Markup languages
#
# For example this section is a good place for HTML tools,
# Markdown tools, UML tools, XML tools, and similar.
##

# Pandoc converts among various formats, such as Markdown and HTML
brew 'pandoc'

## Markdown

# MacDown simple markdown editor
cask 'macdown'

## UML

# StarUML modeling tool
cask 'staruml'

## XML

# XML converter
brew 'xmlstarlet'

# Libxml2 is the XML C parser and toolkit.
brew 'libxml2'

# Libxslt is the XSLT C library for the XML EXtensible Stylesheet Language.
brew 'libxslt'

##
# Programming languages
#
# This section installs many programming languages:
# Clojure, Elixir, Erlang, Go, Haskell, Java, JavaScript,
# Perl, Python, R, Ruby, Scala, Swift, and tooling.
##

## Clojure

# Clojure programming language compiler.
brew 'clojure-compiler'

# Leiningen automates Clojure projects.
brew 'leiningen'

## Elixir

# Elixir programming language built on top of the Erlang VM.
brew 'elixir'

## Erlang

# Erlang programming language for scalable high-availability systems.
brew 'erlang'

## Go

# Go programming language by Google; compare `C`.
brew 'go'

## Haskell

# Cabal is a package manager for Haskell
brew 'ghc'
brew 'cabal-install'

## Java

# Java programming language
cask 'java'

# Gradle is a Java build tool
brew 'gradle'

# Maven is a Java build tool
brew 'maven'

# Spring Tool Suite is an Eclipse IDE for developing apps
cask 'sts'

# Jetty provides a Java web server and javax.servlet container
brew 'jetty'

# Apache Tomcat implements Java Servlet and JavaServer Pages technologies.
brew 'tomcat'

# Glassfish application server.
brew 'glassfish'

## JavaScript

# Node.js is a JavaScript platform for building fast, scalable network app.
brew 'node'

# PhantomJS is a headless WebKit scriptable with a JavaScript API.
brew 'phantomjs'

# V8 JavaScript Engine.
brew 'v8'

# JSON output using the shell
brew 'jo'

# JID JSON explorer
brew tap simeji/jid && brew 'jid'

## Perl

# Perl programming language, esp. for systems administration.
brew 'perl'

# Perl-Compatible Regular Expressions pattern matching tools.
brew 'pcre'

# CPAN search for perl modules
brew 'cpansearch'

## Python

# Python programming language, esp. for systems scripting.
brew 'python'
brew 'python3'

## R

# R programming language, esp. for statistics.
brew 'r'

## Ruby

# chruby changes the current Ruby.
brew 'chruby'

# JRuby is a high performance, stable, fully threaded Java implementation of Ruby.
brew 'jruby'

# Ruby programming language; compare `perl`, `python`.
brew 'ruby'

# Tool to install various implementations of Ruby.
brew 'ruby-install'

## Rust

# Rust programming language
brew 'rust'

## Scala

# Scala programming language, that runs on top of the JVM.
brew 'scala'

## iOS, Objective-C, Swift

# Alcatraz Xcode plugin manager
cask 'alcatraz'

# Appium test automation framework
cask 'appium'

# Carthage Xcode project dependency manager.
brew 'carthage'

# Command-line application launcher for the iOS Simulator
brew 'ios-sim'

# Tool to help with Swift style and conventions.
brew 'swiftlint'

# SourceKitten attaches to SourceKit AST.
brew 'sourcekitten'

# Taylor is a Swift code quality metrics tool.
brew 'taylor'

# Testflight Apple iOS testing service
cask 'testflight'

##
# Art editors
##

# Xquarts
cask 'xquartz'

# Tap GUI
brew tap homebrew/gui

# Gimp pixel-based image editor, similar to Adobe Photoshop
cask 'gimp'

# Inkscape vector-based image  editor, similar to Adobe Illustrator
cask 'inkscape; brew 'inkscape''

##
# Paid software
#
#   * JetBrains programmer tools
#   * OmniGroup project management tools
#
# This section installs the tools, which are free trial versions.
# We pay for licenses for all these for all our teammates.
#
# You may want to customize this section by deleting any items that
# you don't want to use or purchase, because this will save disk space.
##

## Paw.cloud

# Paw HTTP API testing tool
cask 'paw'

##
# JetBrains
#
# JetBrains is paid software suitable for professional programmers,
# such as Integrated Development Environments (IDEs) for popular
# programming languages, including Java, Python, Ruby, PHP, etc.
##

# AppCode Swift IDE
cask 'appcode'

# CLion C/C++ IDE
cask 'clion'

# DataGrip SQL IDE
cask 'datagrip'

# IntelliJ Java IDE
cask 'intellij-idea'

# PhpStorm PHP IDE
cask 'phpstorm'

# PyCharm Python IDE
cask 'pycharm'

# RubyMine Ruby IDE
cask 'rubymine'

# WebStorm IDE
cask 'webstorm'

##
# OmniGroup
#
# OmniGroup provides paid software suitable for professional users.
##

# To do list task manager
cask 'omnifocus'

# Diagramming
cask 'omnigraffle'

# Project management planning
cask 'omniplan'

# Outliner
cask 'omnioutliner'

##
# Libraries
#
# We do this near the end of this file,
# because we expect these will already be
# installed by a bunch of the software above.
#
# This section here is really just to cover our
# bases to make sure we have the libraries that we
# sometimes need for building other software later on.
##

# THe libevent API provides provides asynchronous event notification and callbacks.
brew 'libevent'

# Magic number recognition library for file types.
brew 'libmagic'

# Audio/Visual converters
brew 'libav'

# Curl web fetcher
brew 'libcurl'

# Foreign Function Interface Library
brew 'libffi'

# Text encoding
brew 'libiconv'

# File magic number recognizer
brew 'libmagic'

# ncurses console nagivation
brew 'libncurses'

# Sodium secure cryptography
brew 'libsodium'

# Readline terminal input
brew 'libreadline'

# GNU libtool is a generic library support script.
brew 'libtool'

# XML handlers
brew 'libxml2'
brew 'libxslt'

# High-level interface to X.509 and CMS (Cryptographic Message Syntax)
brew 'libksba'

# V8 JavaScript
brew 'libv8'

# YAML markup language
brew 'libyaml'

# ZIP file compression
brew 'libzip'

# Images
brew 'libjpg'
brew 'libpng'
brew 'libtiff'
brew 'libwebp'

##
# brew-install-our-tech-packages-manually.sh
#
# Use Homebrew to install our favorite tech-related packages
# that may need to be installed manually because of passwords,
# or moving files, or more-complex issues that need a human.
#
##

# Update - this is always the first step
brew update

# Emacs editor.
sudo rm /usr/bin/emacs &&
sudo rm -rf /usr/share/emacs &&
brew 'emacs --cocoa --srgb --use-git-head --HEAD &&'
ls -1 /usr/local/Cellar/emacs/*/bin/emacs |
tail -1 |
xargs -I{} sudo ln -sf "{}" /usr/bin/emacs

## Networking

# nmap network mapper is a security scanner
cask 'nmap'

# Wireshark network protocol analyzer
cask 'wireshark'

## Programming

# Netbeans Java IDE
cask 'netbeans'

# R statistics programming language
cask 'r'

## Deployments

# Vagrant lightweight, reproducible, portable development environments
cask 'vagrant'

# Heroku hosting utilities
cask 'heroku-toolbelt'

##
# Fonts
#
# We like having lots of fonts.
#
# You may prefer to trim this list.
#
# You may prefer to use tap, such as:
#
#      brew tap caskroom/fonts
#      brew cask install font-inconsolata
##

cask 'caskroom/fonts/font-3270'
cask 'caskroom/fonts/font-abeezee'
cask 'caskroom/fonts/font-abel'
cask 'caskroom/fonts/font-aboriginal-sans'
cask 'caskroom/fonts/font-aboriginal-serif'
cask 'caskroom/fonts/font-abril-fatface'
cask 'caskroom/fonts/font-aclonica'
cask 'caskroom/fonts/font-acme'
cask 'caskroom/fonts/font-actor'
cask 'caskroom/fonts/font-adamina'
cask 'caskroom/fonts/font-adinatha-tamil-brahmi'
cask 'caskroom/fonts/font-advent-pro'
cask 'caskroom/fonts/font-african-sans'
cask 'caskroom/fonts/font-african-serif'
cask 'caskroom/fonts/font-aguafina-script'
cask 'caskroom/fonts/font-ahuramzda'
cask 'caskroom/fonts/font-aileron'
cask 'caskroom/fonts/font-akronim'
cask 'caskroom/fonts/font-aladin'
cask 'caskroom/fonts/font-aldrich'
cask 'caskroom/fonts/font-alef'
cask 'caskroom/fonts/font-alegreya-sans-sc'
cask 'caskroom/fonts/font-alegreya-sans'
cask 'caskroom/fonts/font-alegreya-sc'
cask 'caskroom/fonts/font-alegreya'
cask 'caskroom/fonts/font-aleo'
cask 'caskroom/fonts/font-alex-brush'
cask 'caskroom/fonts/font-alfa-slab-one'
cask 'caskroom/fonts/font-alice'
cask 'caskroom/fonts/font-alike-angular'
cask 'caskroom/fonts/font-alike'
cask 'caskroom/fonts/font-allan'
cask 'caskroom/fonts/font-allerta-stencil'
cask 'caskroom/fonts/font-allerta'
cask 'caskroom/fonts/font-allura'
cask 'caskroom/fonts/font-almendra-display'
cask 'caskroom/fonts/font-almendra-sc'
cask 'caskroom/fonts/font-almendra'
cask 'caskroom/fonts/font-amarante'
cask 'caskroom/fonts/font-amaranth'
cask 'caskroom/fonts/font-amatic-sc'
cask 'caskroom/fonts/font-amethysta'
cask 'caskroom/fonts/font-amiri'
cask 'caskroom/fonts/font-anaheim'
cask 'caskroom/fonts/font-andada-sc'
cask 'caskroom/fonts/font-andada'
cask 'caskroom/fonts/font-andagii'
cask 'caskroom/fonts/font-andale-mono'
cask 'caskroom/fonts/font-andika'
cask 'caskroom/fonts/font-angkor'
cask 'caskroom/fonts/font-anka-coder'
cask 'caskroom/fonts/font-annie-use-your-telescope'
cask 'caskroom/fonts/font-anonymice-powerline'
cask 'caskroom/fonts/font-anonymous-pro'
cask 'caskroom/fonts/font-antic-didone'
cask 'caskroom/fonts/font-antic-slab'
cask 'caskroom/fonts/font-antic'
cask 'caskroom/fonts/font-antinoou'
cask 'caskroom/fonts/font-anton'
cask 'caskroom/fonts/font-arapey'
cask 'caskroom/fonts/font-arbutus-slab'
cask 'caskroom/fonts/font-arbutus'
cask 'caskroom/fonts/font-architects-daughter'
cask 'caskroom/fonts/font-archivo-black'
cask 'caskroom/fonts/font-archivo-narrow'
cask 'caskroom/fonts/font-arial-black'
cask 'caskroom/fonts/font-arial'
cask 'caskroom/fonts/font-arimo'
cask 'caskroom/fonts/font-arizonia'
cask 'caskroom/fonts/font-armata'
cask 'caskroom/fonts/font-artifika'
cask 'caskroom/fonts/font-arvo'
cask 'caskroom/fonts/font-asap'
cask 'caskroom/fonts/font-asset'
cask 'caskroom/fonts/font-astloch'
cask 'caskroom/fonts/font-asul'
cask 'caskroom/fonts/font-atomic-age'
cask 'caskroom/fonts/font-aubrey'
cask 'caskroom/fonts/font-audiowide'
cask 'caskroom/fonts/font-autour-one'
cask 'caskroom/fonts/font-average-sans'
cask 'caskroom/fonts/font-average'
cask 'caskroom/fonts/font-averia-gruesa-libre'
cask 'caskroom/fonts/font-averia-libre'
cask 'caskroom/fonts/font-averia-sans-libre'
cask 'caskroom/fonts/font-averia-serif-libre'
cask 'caskroom/fonts/font-awesome-terminal-fonts'
cask 'caskroom/fonts/font-babelstone-han'
cask 'caskroom/fonts/font-babelstone-modern'
cask 'caskroom/fonts/font-bad-script'
cask 'caskroom/fonts/font-baloo'
cask 'caskroom/fonts/font-balthazar'
cask 'caskroom/fonts/font-bangers'
cask 'caskroom/fonts/font-baron'
cask 'caskroom/fonts/font-basic'
cask 'caskroom/fonts/font-battambang'
cask 'caskroom/fonts/font-baumans'
cask 'caskroom/fonts/font-bayon'
cask 'caskroom/fonts/font-bebas-neue'
cask 'caskroom/fonts/font-belgrano'
cask 'caskroom/fonts/font-belleza'
cask 'caskroom/fonts/font-benchnine'
cask 'caskroom/fonts/font-bentham'
cask 'caskroom/fonts/font-berkshire-swash'
cask 'caskroom/fonts/font-bevan'
cask 'caskroom/fonts/font-bf-tiny-hand'
cask 'caskroom/fonts/font-bigelow-rules'
cask 'caskroom/fonts/font-bigshot-one'
cask 'caskroom/fonts/font-bilbo-swash-caps'
cask 'caskroom/fonts/font-bilbo'
cask 'caskroom/fonts/font-bitstream-vera'
cask 'caskroom/fonts/font-bitter'
cask 'caskroom/fonts/font-black-ops-one'
cask 'caskroom/fonts/font-blokk-neue'
cask 'caskroom/fonts/font-bokor'
cask 'caskroom/fonts/font-bonbon'
cask 'caskroom/fonts/font-boogaloo'
cask 'caskroom/fonts/font-bowlby-one-sc'
cask 'caskroom/fonts/font-bowlby-one'
cask 'caskroom/fonts/font-bravura'
cask 'caskroom/fonts/font-brawler'
cask 'caskroom/fonts/font-bree-serif'
cask 'caskroom/fonts/font-bubblegum-sans'
cask 'caskroom/fonts/font-bubbler-one'
cask 'caskroom/fonts/font-buda'
cask 'caskroom/fonts/font-buenard'
cask 'caskroom/fonts/font-bukyvede-bold'
cask 'caskroom/fonts/font-bukyvede-italic'
cask 'caskroom/fonts/font-bukyvede-regular'
cask 'caskroom/fonts/font-bungee'
cask 'caskroom/fonts/font-butcherman'
cask 'caskroom/fonts/font-butler'
cask 'caskroom/fonts/font-butterfly-kids'
cask 'caskroom/fonts/font-cabin-condensed'
cask 'caskroom/fonts/font-cabin-sketch'
cask 'caskroom/fonts/font-cabin'
cask 'caskroom/fonts/font-caesar-dressing'
cask 'caskroom/fonts/font-cagliostro'
cask 'caskroom/fonts/font-calligraffitti'
cask 'caskroom/fonts/font-cambo'
cask 'caskroom/fonts/font-camingocode'
cask 'caskroom/fonts/font-candal'
cask 'caskroom/fonts/font-cantarell'
cask 'caskroom/fonts/font-cantata-one'
cask 'caskroom/fonts/font-canter'
cask 'caskroom/fonts/font-cantora-one'
cask 'caskroom/fonts/font-capriola'
cask 'caskroom/fonts/font-cardo'
cask 'caskroom/fonts/font-carme'
cask 'caskroom/fonts/font-carrois-gothic-sc'
cask 'caskroom/fonts/font-carrois-gothic'
cask 'caskroom/fonts/font-carter-one'
cask 'caskroom/fonts/font-caudex'
cask 'caskroom/fonts/font-cedarville-cursive'
cask 'caskroom/fonts/font-ceviche-one'
cask 'caskroom/fonts/font-changa-one'
cask 'caskroom/fonts/font-chango'
cask 'caskroom/fonts/font-chapbook'
cask 'caskroom/fonts/font-charis-sil'
cask 'caskroom/fonts/font-charter'
cask 'caskroom/fonts/font-chau-philomene-one'
cask 'caskroom/fonts/font-chela-one'
cask 'caskroom/fonts/font-chelsea-market'
cask 'caskroom/fonts/font-chenla'
cask 'caskroom/fonts/font-cherry-cream-soda'
cask 'caskroom/fonts/font-cherry-swash'
cask 'caskroom/fonts/font-chewy'
cask 'caskroom/fonts/font-chicle'
cask 'caskroom/fonts/font-chivo'
cask 'caskroom/fonts/font-cinzel-decorative'
cask 'caskroom/fonts/font-cinzel'
cask 'caskroom/fonts/font-clear-sans'
cask 'caskroom/fonts/font-clicker-script'
cask 'caskroom/fonts/font-coda-caption'
cask 'caskroom/fonts/font-coda'
cask 'caskroom/fonts/font-code'
cask 'caskroom/fonts/font-code2000'
cask 'caskroom/fonts/font-code2001'
cask 'caskroom/fonts/font-code2002'
cask 'caskroom/fonts/font-codystar'
cask 'caskroom/fonts/font-combo'
cask 'caskroom/fonts/font-comfortaa'
cask 'caskroom/fonts/font-comic-neue'
cask 'caskroom/fonts/font-comic-sans-ms'
cask 'caskroom/fonts/font-coming-soon'
cask 'caskroom/fonts/font-computer-modern'
cask 'caskroom/fonts/font-conakry'
cask 'caskroom/fonts/font-concert-one'
cask 'caskroom/fonts/font-condiment'
cask 'caskroom/fonts/font-consolas-for-powerline'
cask 'caskroom/fonts/font-constructium'
cask 'caskroom/fonts/font-content'
cask 'caskroom/fonts/font-contrail-one'
cask 'caskroom/fonts/font-convergence'
cask 'caskroom/fonts/font-cookie'
cask 'caskroom/fonts/font-copse'
cask 'caskroom/fonts/font-corben'
cask 'caskroom/fonts/font-courgette'
cask 'caskroom/fonts/font-courier-new'
cask 'caskroom/fonts/font-courier-prime'
cask 'caskroom/fonts/font-cousine'
cask 'caskroom/fonts/font-coustard'
cask 'caskroom/fonts/font-covered-by-your-grace'
cask 'caskroom/fonts/font-crafty-girls'
cask 'caskroom/fonts/font-creepster'
cask 'caskroom/fonts/font-crete-round'
cask 'caskroom/fonts/font-crimson-text'
cask 'caskroom/fonts/font-croissant-one'
cask 'caskroom/fonts/font-crushed'
cask 'caskroom/fonts/font-cuprum'
cask 'caskroom/fonts/font-cutive-mono'
cask 'caskroom/fonts/font-cutive'
cask 'caskroom/fonts/font-cwtex-q'
cask 'caskroom/fonts/font-d2coding'
cask 'caskroom/fonts/font-damion'
cask 'caskroom/fonts/font-dancing-script'
cask 'caskroom/fonts/font-dangrek'
cask 'caskroom/fonts/font-dashicons'
cask 'caskroom/fonts/font-dawning-of-a-new-day'
cask 'caskroom/fonts/font-days-one'
cask 'caskroom/fonts/font-dejavu-sans-mono-for-powerline'
cask 'caskroom/fonts/font-dejavu-sans'
cask 'caskroom/fonts/font-delius-swash-caps'
cask 'caskroom/fonts/font-delius-unicase'
cask 'caskroom/fonts/font-delius'
cask 'caskroom/fonts/font-della-respira'
cask 'caskroom/fonts/font-denk-one'
cask 'caskroom/fonts/font-devicons'
cask 'caskroom/fonts/font-devonshire'
cask 'caskroom/fonts/font-dhyana'
cask 'caskroom/fonts/font-didact-gothic'
cask 'caskroom/fonts/font-digohweli-old-do'
cask 'caskroom/fonts/font-digohweli'
cask 'caskroom/fonts/font-diplomata-sc'
cask 'caskroom/fonts/font-diplomata'
cask 'caskroom/fonts/font-disclaimer'
cask 'caskroom/fonts/font-domine'
cask 'caskroom/fonts/font-donegal-one'
cask 'caskroom/fonts/font-doppio-one'
cask 'caskroom/fonts/font-dorsa'
cask 'caskroom/fonts/font-dosis'
cask 'caskroom/fonts/font-dr-sugiyama'
cask 'caskroom/fonts/font-droid-arabic-kufi'
cask 'caskroom/fonts/font-droid-arabic-naskh'
cask 'caskroom/fonts/font-droid-sans-ethiopic'
cask 'caskroom/fonts/font-droid-sans-mono-for-powerline'
cask 'caskroom/fonts/font-droid-sans-mono'
cask 'caskroom/fonts/font-droid-sans-tamil'
cask 'caskroom/fonts/font-droid-sans-thai'
cask 'caskroom/fonts/font-droid-sans'
cask 'caskroom/fonts/font-droid-serif-thai'
cask 'caskroom/fonts/font-droid-serif'
cask 'caskroom/fonts/font-dukor'
cask 'caskroom/fonts/font-duru-sans'
cask 'caskroom/fonts/font-dynalight'
cask 'caskroom/fonts/font-eagle-lake'
cask 'caskroom/fonts/font-eater'
cask 'caskroom/fonts/font-eb-garamond'
cask 'caskroom/fonts/font-economica'
cask 'caskroom/fonts/font-edlo'
cask 'caskroom/fonts/font-eeyek-unicode'
cask 'caskroom/fonts/font-electrolize'
cask 'caskroom/fonts/font-elsie-swash-caps'
cask 'caskroom/fonts/font-elsie'
cask 'caskroom/fonts/font-emblema-one'
cask 'caskroom/fonts/font-emilys-candy'
cask 'caskroom/fonts/font-engagement'
cask 'caskroom/fonts/font-englebert'
cask 'caskroom/fonts/font-enriqueta'
cask 'caskroom/fonts/font-erica-one'
cask 'caskroom/fonts/font-esteban'
cask 'caskroom/fonts/font-et-book'
cask 'caskroom/fonts/font-euphoria-script'
cask 'caskroom/fonts/font-everson-mono'
cask 'caskroom/fonts/font-ewert'
cask 'caskroom/fonts/font-exo'
cask 'caskroom/fonts/font-exo2'
cask 'caskroom/fonts/font-expletus-sans'
cask 'caskroom/fonts/font-ezra-sil'
cask 'caskroom/fonts/font-fairfax'
cask 'caskroom/fonts/font-fantasque-sans-mono'
cask 'caskroom/fonts/font-fanwood-text'
cask 'caskroom/fonts/font-fascinate-inline'
cask 'caskroom/fonts/font-fascinate'
cask 'caskroom/fonts/font-faster-one'
cask 'caskroom/fonts/font-fasthand'
cask 'caskroom/fonts/font-fauna-one'
cask 'caskroom/fonts/font-federant'
cask 'caskroom/fonts/font-federo'
cask 'caskroom/fonts/font-felipa'
cask 'caskroom/fonts/font-fenix'
cask 'caskroom/fonts/font-finger-paint'
cask 'caskroom/fonts/font-fira-code'
cask 'caskroom/fonts/font-fira-mono-for-powerline'
cask 'caskroom/fonts/font-fira-mono'
cask 'caskroom/fonts/font-fira-sans'
cask 'caskroom/fonts/font-firacode-nerd-font-mono'
cask 'caskroom/fonts/font-firacode-nerd-font'
cask 'caskroom/fonts/font-fjalla-one'
cask 'caskroom/fonts/font-fjord-one'
cask 'caskroom/fonts/font-flamenco'
cask 'caskroom/fonts/font-flavors'
cask 'caskroom/fonts/font-fondamento'
cask 'caskroom/fonts/font-fontawesome'
cask 'caskroom/fonts/font-fontdiner-swanky'
cask 'caskroom/fonts/font-forum'
cask 'caskroom/fonts/font-foundation-icons'
cask 'caskroom/fonts/font-francois-one'
cask 'caskroom/fonts/font-freckle-face'
cask 'caskroom/fonts/font-fredericka-the-great'
cask 'caskroom/fonts/font-fredoka-one'
cask 'caskroom/fonts/font-free-hk-kai'
cask 'caskroom/fonts/font-freehand'
cask 'caskroom/fonts/font-freesans'
cask 'caskroom/fonts/font-fresca'
cask 'caskroom/fonts/font-frijole'
cask 'caskroom/fonts/font-fruktur'
cask 'caskroom/fonts/font-fugaz-one'
cask 'caskroom/fonts/font-gabriela'
cask 'caskroom/fonts/font-gafata'
cask 'caskroom/fonts/font-galdeano'
cask 'caskroom/fonts/font-galindo'
cask 'caskroom/fonts/font-gandom'
cask 'caskroom/fonts/font-genjyuugothic-l'
cask 'caskroom/fonts/font-genjyuugothic-x'
cask 'caskroom/fonts/font-genjyuugothic'
cask 'caskroom/fonts/font-genshingothic'
cask 'caskroom/fonts/font-gentium-basic'
cask 'caskroom/fonts/font-gentium-book-basic'
cask 'caskroom/fonts/font-gentium-plus'
cask 'caskroom/fonts/font-geo'
cask 'caskroom/fonts/font-georgia'
cask 'caskroom/fonts/font-geostar-fill'
cask 'caskroom/fonts/font-geostar'
cask 'caskroom/fonts/font-germania-one'
cask 'caskroom/fonts/font-gfs-didot'
cask 'caskroom/fonts/font-gfs-neohellenic'
cask 'caskroom/fonts/font-gidole'
cask 'caskroom/fonts/font-gilda-display'
cask 'caskroom/fonts/font-give-you-glory'
cask 'caskroom/fonts/font-glass-antiqua'
cask 'caskroom/fonts/font-glegoo'
cask 'caskroom/fonts/font-glober'
cask 'caskroom/fonts/font-gloria-hallelujah'
cask 'caskroom/fonts/font-gnu-unifont'
cask 'caskroom/fonts/font-go-medium'
cask 'caskroom/fonts/font-go-mono'
cask 'caskroom/fonts/font-go'
cask 'caskroom/fonts/font-goblin-one'
cask 'caskroom/fonts/font-gochi-hand'
cask 'caskroom/fonts/font-gorditas'
cask 'caskroom/fonts/font-goudy-bookletter1911'
cask 'caskroom/fonts/font-graduate'
cask 'caskroom/fonts/font-grand-hotel'
cask 'caskroom/fonts/font-gravitas-one'
cask 'caskroom/fonts/font-great-vibes'
cask 'caskroom/fonts/font-griffy'
cask 'caskroom/fonts/font-gruppo'
cask 'caskroom/fonts/font-gudea'
cask 'caskroom/fonts/font-habibi'
cask 'caskroom/fonts/font-hack-nerd-font'
cask 'caskroom/fonts/font-hack'
cask 'caskroom/fonts/font-halant'
cask 'caskroom/fonts/font-hammersmith-one'
cask 'caskroom/fonts/font-han-nom-a'
cask 'caskroom/fonts/font-hanalei-fill'
cask 'caskroom/fonts/font-hanalei'
cask 'caskroom/fonts/font-hanamina'
cask 'caskroom/fonts/font-handlee'
cask 'caskroom/fonts/font-hanuman'
cask 'caskroom/fonts/font-happy-monkey'
cask 'caskroom/fonts/font-hasklig'
cask 'caskroom/fonts/font-headland-one'
cask 'caskroom/fonts/font-henny-penny'
cask 'caskroom/fonts/font-hermeneus-one'
cask 'caskroom/fonts/font-hermit'
cask 'caskroom/fonts/font-herr-von-muellerhoff'
cask 'caskroom/fonts/font-hind'
cask 'caskroom/fonts/font-holtwood-one-sc'
cask 'caskroom/fonts/font-homemade-apple'
cask 'caskroom/fonts/font-homenaje'
cask 'caskroom/fonts/font-hyppolit'
cask 'caskroom/fonts/font-iceberg'
cask 'caskroom/fonts/font-iceland'
cask 'caskroom/fonts/font-icomoon'
cask 'caskroom/fonts/font-idealist-sans'
cask 'caskroom/fonts/font-im-fell-double-pica-sc'
cask 'caskroom/fonts/font-im-fell-double-pica'
cask 'caskroom/fonts/font-im-fell-dw-pica-sc'
cask 'caskroom/fonts/font-im-fell-dw-pica'
cask 'caskroom/fonts/font-im-fell-english-sc'
cask 'caskroom/fonts/font-im-fell-english'
cask 'caskroom/fonts/font-im-fell-french-canon-sc'
cask 'caskroom/fonts/font-im-fell-french-canon'
cask 'caskroom/fonts/font-im-fell-great-primer-sc'
cask 'caskroom/fonts/font-im-fell-great-primer'
cask 'caskroom/fonts/font-impact'
cask 'caskroom/fonts/font-imprima'
cask 'caskroom/fonts/font-inconsolata-dz-for-powerline'
cask 'caskroom/fonts/font-inconsolata-dz'
cask 'caskroom/fonts/font-inconsolata-for-powerline'
cask 'caskroom/fonts/font-inconsolata-g-for-powerline'
cask 'caskroom/fonts/font-inconsolata-lgc'
cask 'caskroom/fonts/font-inconsolata'
cask 'caskroom/fonts/font-inder'
cask 'caskroom/fonts/font-indie-flower'
cask 'caskroom/fonts/font-inika'
cask 'caskroom/fonts/font-input'
cask 'caskroom/fonts/font-ionicons'
cask 'caskroom/fonts/font-iosevka'
cask 'caskroom/fonts/font-iranian-sans'
cask 'caskroom/fonts/font-iranian-serif'
cask 'caskroom/fonts/font-irish-grover'
cask 'caskroom/fonts/font-istok-web'
cask 'caskroom/fonts/font-italiana'
cask 'caskroom/fonts/font-italianno'
cask 'caskroom/fonts/font-jaapokki'
cask 'caskroom/fonts/font-jacques-francois-shadow'
cask 'caskroom/fonts/font-jacques-francois'
cask 'caskroom/fonts/font-jim-nightshade'
cask 'caskroom/fonts/font-jockey-one'
cask 'caskroom/fonts/font-jolly-lodger'
cask 'caskroom/fonts/font-josefin-sans'
cask 'caskroom/fonts/font-josefin-slab'
cask 'caskroom/fonts/font-joti-one'
cask 'caskroom/fonts/font-jsmath-cmbx10'
cask 'caskroom/fonts/font-judson'
cask 'caskroom/fonts/font-julee'
cask 'caskroom/fonts/font-julius-sans-one'
cask 'caskroom/fonts/font-junge'
cask 'caskroom/fonts/font-junicode'
cask 'caskroom/fonts/font-jura'
cask 'caskroom/fonts/font-just-another-hand'
cask 'caskroom/fonts/font-just-me-again-down-here'
cask 'caskroom/fonts/font-kacstone'
cask 'caskroom/fonts/font-kalam'
cask 'caskroom/fonts/font-kameron'
cask 'caskroom/fonts/font-kantumruy'
cask 'caskroom/fonts/font-karla-tamil-inclined'
cask 'caskroom/fonts/font-karla-tamil-upright'
cask 'caskroom/fonts/font-karla'
cask 'caskroom/fonts/font-karma'
cask 'caskroom/fonts/font-kaushan-script'
cask 'caskroom/fonts/font-kavoon'
cask 'caskroom/fonts/font-kawkab-mono'
cask 'caskroom/fonts/font-kayases'
cask 'caskroom/fonts/font-kdam-thmor'
cask 'caskroom/fonts/font-keania-one'
cask 'caskroom/fonts/font-keep-calm'
cask 'caskroom/fonts/font-kelly-slab'
cask 'caskroom/fonts/font-kenia'
cask 'caskroom/fonts/font-khand'
cask 'caskroom/fonts/font-khmer'
cask 'caskroom/fonts/font-kisiska'
cask 'caskroom/fonts/font-kite-one'
cask 'caskroom/fonts/font-knewave'
cask 'caskroom/fonts/font-koruri'
cask 'caskroom/fonts/font-kotta-one'
cask 'caskroom/fonts/font-koulen'
cask 'caskroom/fonts/font-kranky'
cask 'caskroom/fonts/font-kreon'
cask 'caskroom/fonts/font-kristi'
cask 'caskroom/fonts/font-krona-one'
cask 'caskroom/fonts/font-la-belle-aurore'
cask 'caskroom/fonts/font-laila'
cask 'caskroom/fonts/font-lalezar'
cask 'caskroom/fonts/font-lancelot'
cask 'caskroom/fonts/font-lateef'
cask 'caskroom/fonts/font-latin-modern-math'
cask 'caskroom/fonts/font-latin-modern'
cask 'caskroom/fonts/font-lato'
cask 'caskroom/fonts/font-league-gothic'
cask 'caskroom/fonts/font-league-script'
cask 'caskroom/fonts/font-league-spartan'
cask 'caskroom/fonts/font-leckerli-one'
cask 'caskroom/fonts/font-ledger'
cask 'caskroom/fonts/font-lekton'
cask 'caskroom/fonts/font-lemon'
cask 'caskroom/fonts/font-liberation-mono-for-powerline'
cask 'caskroom/fonts/font-liberation-sans'
cask 'caskroom/fonts/font-libertinus'
cask 'caskroom/fonts/font-libre-baskerville'
cask 'caskroom/fonts/font-libre-caslon-text'
cask 'caskroom/fonts/font-libre-franklin'
cask 'caskroom/fonts/font-life-savers'
cask 'caskroom/fonts/font-ligature-symbols'
cask 'caskroom/fonts/font-lilita-one'
cask 'caskroom/fonts/font-lily-script-one'
cask 'caskroom/fonts/font-limelight'
cask 'caskroom/fonts/font-linden-hill'
cask 'caskroom/fonts/font-linux-biolinum'
cask 'caskroom/fonts/font-linux-libertine'
cask 'caskroom/fonts/font-lisutzimu'
cask 'caskroom/fonts/font-lobster-two'
cask 'caskroom/fonts/font-lobster'
cask 'caskroom/fonts/font-lohit-assamese'
cask 'caskroom/fonts/font-lohit-bengali'
cask 'caskroom/fonts/font-lohit-devanagari'
cask 'caskroom/fonts/font-lohit-gujarati'
cask 'caskroom/fonts/font-lohit-kannada'
cask 'caskroom/fonts/font-lohit-malayalam'
cask 'caskroom/fonts/font-lohit-marathi'
cask 'caskroom/fonts/font-lohit-nepali'
cask 'caskroom/fonts/font-lohit-oriya'
cask 'caskroom/fonts/font-lohit-punjabi'
cask 'caskroom/fonts/font-lohit-tamil-classical'
cask 'caskroom/fonts/font-lohit-tamil'
cask 'caskroom/fonts/font-lohit-telugu'
cask 'caskroom/fonts/font-londrina-outline'
cask 'caskroom/fonts/font-londrina-shadow'
cask 'caskroom/fonts/font-londrina-sketch'
cask 'caskroom/fonts/font-londrina-solid'
cask 'caskroom/fonts/font-lora'
cask 'caskroom/fonts/font-love-ya-like-a-sister'
cask 'caskroom/fonts/font-loved-by-the-king'
cask 'caskroom/fonts/font-lovers-quarrel'
cask 'caskroom/fonts/font-luckiest-guy'
cask 'caskroom/fonts/font-luculent'
cask 'caskroom/fonts/font-lusitana'
cask 'caskroom/fonts/font-lustria'
cask 'caskroom/fonts/font-m-plus'
cask 'caskroom/fonts/font-macondo-swash-caps'
cask 'caskroom/fonts/font-macondo'
cask 'caskroom/fonts/font-magra'
cask 'caskroom/fonts/font-maiden-orange'
cask 'caskroom/fonts/font-mako'
cask 'caskroom/fonts/font-marcellus-sc'
cask 'caskroom/fonts/font-marcellus'
cask 'caskroom/fonts/font-marck-script'
cask 'caskroom/fonts/font-margarine'
cask 'caskroom/fonts/font-marko-one'
cask 'caskroom/fonts/font-marmelad'
cask 'caskroom/fonts/font-marta'
cask 'caskroom/fonts/font-marvel'
cask 'caskroom/fonts/font-masinahikan-dene'
cask 'caskroom/fonts/font-masinahikan'
cask 'caskroom/fonts/font-mate-sc'
cask 'caskroom/fonts/font-mate'
cask 'caskroom/fonts/font-material-icons'
cask 'caskroom/fonts/font-materialdesignicons-webfont'
cask 'caskroom/fonts/font-maven-pro'
cask 'caskroom/fonts/font-mclaren'
cask 'caskroom/fonts/font-meddon'
cask 'caskroom/fonts/font-medievalsharp'
cask 'caskroom/fonts/font-medula-one'
cask 'caskroom/fonts/font-megrim'
cask 'caskroom/fonts/font-meie-script'
cask 'caskroom/fonts/font-menlo-for-powerline'
cask 'caskroom/fonts/font-merienda-one'
cask 'caskroom/fonts/font-merienda'
cask 'caskroom/fonts/font-merriweather-sans'
cask 'caskroom/fonts/font-merriweather'
cask 'caskroom/fonts/font-meslo-lg-for-powerline'
cask 'caskroom/fonts/font-metal-mania'
cask 'caskroom/fonts/font-metal'
cask 'caskroom/fonts/font-metamorphous'
cask 'caskroom/fonts/font-metrophobic'
cask 'caskroom/fonts/font-mfizz'
cask 'caskroom/fonts/font-miao-unicode'
cask 'caskroom/fonts/font-michroma'
cask 'caskroom/fonts/font-migmix-1m'
cask 'caskroom/fonts/font-migmix-1p'
cask 'caskroom/fonts/font-migmix-2m'
cask 'caskroom/fonts/font-migmix-2p'
cask 'caskroom/fonts/font-migu-1c'
cask 'caskroom/fonts/font-migu-1m'
cask 'caskroom/fonts/font-migu-1p'
cask 'caskroom/fonts/font-migu-2m'
cask 'caskroom/fonts/font-milonga'
cask 'caskroom/fonts/font-miltonian-tattoo'
cask 'caskroom/fonts/font-miltonian'
cask 'caskroom/fonts/font-miniver'
cask 'caskroom/fonts/font-miss-fajardose'
cask 'caskroom/fonts/font-modern-antiqua'
cask 'caskroom/fonts/font-molengo'
cask 'caskroom/fonts/font-molle'
cask 'caskroom/fonts/font-monda'
cask 'caskroom/fonts/font-monofett'
cask 'caskroom/fonts/font-monofur-for-powerline'
cask 'caskroom/fonts/font-monofur'
cask 'caskroom/fonts/font-monoid'
cask 'caskroom/fonts/font-monoisome'
cask 'caskroom/fonts/font-mononoki'
cask 'caskroom/fonts/font-monoton'
cask 'caskroom/fonts/font-monsieur-la-doulaise'
cask 'caskroom/fonts/font-montaga'
cask 'caskroom/fonts/font-montez'
cask 'caskroom/fonts/font-montserrat-alternates'
cask 'caskroom/fonts/font-montserrat-subrayada'
cask 'caskroom/fonts/font-montserrat'
cask 'caskroom/fonts/font-moul'
cask 'caskroom/fonts/font-moulpali'
cask 'caskroom/fonts/font-mountains-of-christmas'
cask 'caskroom/fonts/font-mouse-memoirs'
cask 'caskroom/fonts/font-mr-bedfort'
cask 'caskroom/fonts/font-mr-dafoe'
cask 'caskroom/fonts/font-mr-de-haviland'
cask 'caskroom/fonts/font-mrs-saint-delafield'
cask 'caskroom/fonts/font-mrs-sheppards'
cask 'caskroom/fonts/font-mukti-narrow'
cask 'caskroom/fonts/font-muli'
cask 'caskroom/fonts/font-myrica'
cask 'caskroom/fonts/font-myricam'
cask 'caskroom/fonts/font-mystery-quest'
cask 'caskroom/fonts/font-n-gage'
cask 'caskroom/fonts/font-namdhinggo-sil'
cask 'caskroom/fonts/font-nanumgothic'
cask 'caskroom/fonts/font-nanumgothiccoding'
cask 'caskroom/fonts/font-nanummyeongjo'
cask 'caskroom/fonts/font-neucha'
cask 'caskroom/fonts/font-neuton'
cask 'caskroom/fonts/font-new-athena-unicode'
cask 'caskroom/fonts/font-new-rocker'
cask 'caskroom/fonts/font-news-cycle'
cask 'caskroom/fonts/font-nexa'
cask 'caskroom/fonts/font-niconne'
cask 'caskroom/fonts/font-nika'
cask 'caskroom/fonts/font-nixie-one'
cask 'caskroom/fonts/font-nobile'
cask 'caskroom/fonts/font-nokora'
cask 'caskroom/fonts/font-norican'
cask 'caskroom/fonts/font-norwester'
cask 'caskroom/fonts/font-nosifer'
cask 'caskroom/fonts/font-nothing-you-could-do'
cask 'caskroom/fonts/font-noticia-text'
cask 'caskroom/fonts/font-noto-color-emoji'
cask 'caskroom/fonts/font-noto-emoji'
cask 'caskroom/fonts/font-noto-kufi-arabic'
cask 'caskroom/fonts/font-noto-mono'
cask 'caskroom/fonts/font-noto-naskh-arabic'
cask 'caskroom/fonts/font-noto-nastaliq-urdu'
cask 'caskroom/fonts/font-noto-sans-armenian'
cask 'caskroom/fonts/font-noto-sans-avestan'
cask 'caskroom/fonts/font-noto-sans-balinese'
cask 'caskroom/fonts/font-noto-sans-bamum'
cask 'caskroom/fonts/font-noto-sans-batak'
cask 'caskroom/fonts/font-noto-sans-bengali'
cask 'caskroom/fonts/font-noto-sans-brahmi'
cask 'caskroom/fonts/font-noto-sans-buginese'
cask 'caskroom/fonts/font-noto-sans-buhid'
cask 'caskroom/fonts/font-noto-sans-canadian-aboriginal'
cask 'caskroom/fonts/font-noto-sans-carian'
cask 'caskroom/fonts/font-noto-sans-cham'
cask 'caskroom/fonts/font-noto-sans-cherokee'
cask 'caskroom/fonts/font-noto-sans-cjk-jp'
cask 'caskroom/fonts/font-noto-sans-cjk-kr'
cask 'caskroom/fonts/font-noto-sans-cjk-sc'
cask 'caskroom/fonts/font-noto-sans-cjk-tc'
cask 'caskroom/fonts/font-noto-sans-cjk'
cask 'caskroom/fonts/font-noto-sans-coptic'
cask 'caskroom/fonts/font-noto-sans-cuneiform'
cask 'caskroom/fonts/font-noto-sans-cypriot'
cask 'caskroom/fonts/font-noto-sans-deseret'
cask 'caskroom/fonts/font-noto-sans-devanagari'
cask 'caskroom/fonts/font-noto-sans-egyptian-hieroglyphs'
cask 'caskroom/fonts/font-noto-sans-ethiopic'
cask 'caskroom/fonts/font-noto-sans-georgian'
cask 'caskroom/fonts/font-noto-sans-glagolitic'
cask 'caskroom/fonts/font-noto-sans-gothic'
cask 'caskroom/fonts/font-noto-sans-gujarati'
cask 'caskroom/fonts/font-noto-sans-gurmukhi'
cask 'caskroom/fonts/font-noto-sans-hanunoo'
cask 'caskroom/fonts/font-noto-sans-hecask'
cask 'caskroom/fonts/font-noto-sans-imperial-aramaic'
cask 'caskroom/fonts/font-noto-sans-inscriptional-pahlavi'
cask 'caskroom/fonts/font-noto-sans-inscriptional-parthian'
cask 'caskroom/fonts/font-noto-sans-javanese'
cask 'caskroom/fonts/font-noto-sans-kaithi'
cask 'caskroom/fonts/font-noto-sans-kannada'
cask 'caskroom/fonts/font-noto-sans-kayah-li'
cask 'caskroom/fonts/font-noto-sans-kharoshthi'
cask 'caskroom/fonts/font-noto-sans-khmer'
cask 'caskroom/fonts/font-noto-sans-lao'
cask 'caskroom/fonts/font-noto-sans-lepcha'
cask 'caskroom/fonts/font-noto-sans-limbu'
cask 'caskroom/fonts/font-noto-sans-linear-b'
cask 'caskroom/fonts/font-noto-sans-lisu'
cask 'caskroom/fonts/font-noto-sans-lycian'
cask 'caskroom/fonts/font-noto-sans-lydian'
cask 'caskroom/fonts/font-noto-sans-malayalam'
cask 'caskroom/fonts/font-noto-sans-mandaic'
cask 'caskroom/fonts/font-noto-sans-meetei-mayek'
cask 'caskroom/fonts/font-noto-sans-mongolian'
cask 'caskroom/fonts/font-noto-sans-myanmar'
cask 'caskroom/fonts/font-noto-sans-n-ko'
cask 'caskroom/fonts/font-noto-sans-new-tai-lue'
cask 'caskroom/fonts/font-noto-sans-ogham'
cask 'caskroom/fonts/font-noto-sans-ol-chiki'
cask 'caskroom/fonts/font-noto-sans-old-italic'
cask 'caskroom/fonts/font-noto-sans-old-persian'
cask 'caskroom/fonts/font-noto-sans-old-south-arabian'
cask 'caskroom/fonts/font-noto-sans-old-turkic'
cask 'caskroom/fonts/font-noto-sans-oriya'
cask 'caskroom/fonts/font-noto-sans-osmanya'
cask 'caskroom/fonts/font-noto-sans-phags-pa'
cask 'caskroom/fonts/font-noto-sans-phoenician'
cask 'caskroom/fonts/font-noto-sans-rejang'
cask 'caskroom/fonts/font-noto-sans-runic'
cask 'caskroom/fonts/font-noto-sans-samaritan'
cask 'caskroom/fonts/font-noto-sans-saurashtra'
cask 'caskroom/fonts/font-noto-sans-shavian'
cask 'caskroom/fonts/font-noto-sans-sinhala'
cask 'caskroom/fonts/font-noto-sans-sundanese'
cask 'caskroom/fonts/font-noto-sans-syloti-nagri'
cask 'caskroom/fonts/font-noto-sans-symbols'
cask 'caskroom/fonts/font-noto-sans-syriac-eastern'
cask 'caskroom/fonts/font-noto-sans-syriac-estrangela'
cask 'caskroom/fonts/font-noto-sans-syriac-western'
cask 'caskroom/fonts/font-noto-sans-tagalog'
cask 'caskroom/fonts/font-noto-sans-tagbanwa'
cask 'caskroom/fonts/font-noto-sans-tai-le'
cask 'caskroom/fonts/font-noto-sans-tai-tham'
cask 'caskroom/fonts/font-noto-sans-tai-viet'
cask 'caskroom/fonts/font-noto-sans-tamil'
cask 'caskroom/fonts/font-noto-sans-telugu'
cask 'caskroom/fonts/font-noto-sans-thaana'
cask 'caskroom/fonts/font-noto-sans-thai'
cask 'caskroom/fonts/font-noto-sans-tibetan'
cask 'caskroom/fonts/font-noto-sans-tifinagh'
cask 'caskroom/fonts/font-noto-sans-ugaritic'
cask 'caskroom/fonts/font-noto-sans-vai'
cask 'caskroom/fonts/font-noto-sans-yi'
cask 'caskroom/fonts/font-noto-sans'
cask 'caskroom/fonts/font-noto-serif-armenian'
cask 'caskroom/fonts/font-noto-serif-georgian'
cask 'caskroom/fonts/font-noto-serif-khmer'
cask 'caskroom/fonts/font-noto-serif-lao'
cask 'caskroom/fonts/font-noto-serif-thai'
cask 'caskroom/fonts/font-noto-serif'
cask 'caskroom/fonts/font-nova-cut'
cask 'caskroom/fonts/font-nova-flat'
cask 'caskroom/fonts/font-nova-mono'
cask 'caskroom/fonts/font-nova-oval'
cask 'caskroom/fonts/font-nova-round'
cask 'caskroom/fonts/font-nova-script'
cask 'caskroom/fonts/font-nova-slim'
cask 'caskroom/fonts/font-nova-square'
cask 'caskroom/fonts/font-numans'
cask 'caskroom/fonts/font-nunito'
cask 'caskroom/fonts/font-nyashi'
cask 'caskroom/fonts/font-ocra'
cask 'caskroom/fonts/font-octicons'
cask 'caskroom/fonts/font-odor-mean-chey'
cask 'caskroom/fonts/font-office-code-pro'
cask 'caskroom/fonts/font-offside'
cask 'caskroom/fonts/font-old-standard-tt'
cask 'caskroom/fonts/font-oldenburg'
cask 'caskroom/fonts/font-oleo-script-swash-caps'
cask 'caskroom/fonts/font-oleo-script'
cask 'caskroom/fonts/font-open-iconic'
cask 'caskroom/fonts/font-open-sans-condensed'
cask 'caskroom/fonts/font-open-sans-hecask-condensed'
cask 'caskroom/fonts/font-open-sans-hecask'
cask 'caskroom/fonts/font-open-sans'
cask 'caskroom/fonts/font-opendyslexic'
cask 'caskroom/fonts/font-oranienbaum'
cask 'caskroom/fonts/font-orbitron'
cask 'caskroom/fonts/font-oregano'
cask 'caskroom/fonts/font-orienta'
cask 'caskroom/fonts/font-original-surfer'
cask 'caskroom/fonts/font-oskiblackfoot'
cask 'caskroom/fonts/font-oskidakelh'
cask 'caskroom/fonts/font-oskidenea'
cask 'caskroom/fonts/font-oskideneb'
cask 'caskroom/fonts/font-oskidenec'
cask 'caskroom/fonts/font-oskidenes'
cask 'caskroom/fonts/font-oskieast'
cask 'caskroom/fonts/font-oskiwest'
cask 'caskroom/fonts/font-oswald'
cask 'caskroom/fonts/font-over-the-rainbow'
cask 'caskroom/fonts/font-overlock-sc'
cask 'caskroom/fonts/font-overlock'
cask 'caskroom/fonts/font-overpass'
cask 'caskroom/fonts/font-ovo'
cask 'caskroom/fonts/font-oxygen-mono'
cask 'caskroom/fonts/font-oxygen'
cask 'caskroom/fonts/font-pacifico'
cask 'caskroom/fonts/font-padauk'
cask 'caskroom/fonts/font-palemonas'
cask 'caskroom/fonts/font-paprika'
cask 'caskroom/fonts/font-parastoo'
cask 'caskroom/fonts/font-parisienne'
cask 'caskroom/fonts/font-passero-one'
cask 'caskroom/fonts/font-passion-one'
cask 'caskroom/fonts/font-pathway-gothic-one'
cask 'caskroom/fonts/font-patrick-hand-sc'
cask 'caskroom/fonts/font-patrick-hand'
cask 'caskroom/fonts/font-patua-one'
cask 'caskroom/fonts/font-paytone-one'
cask 'caskroom/fonts/font-pecita'
cask 'caskroom/fonts/font-penuturesu'
cask 'caskroom/fonts/font-peralta'
cask 'caskroom/fonts/font-permanent-marker'
cask 'caskroom/fonts/font-petit-formal-script'
cask 'caskroom/fonts/font-petrona'
cask 'caskroom/fonts/font-phetsarath'
cask 'caskroom/fonts/font-philosopher'
cask 'caskroom/fonts/font-piedra'
cask 'caskroom/fonts/font-pinyon-script'
cask 'caskroom/fonts/font-pirata-one'
cask 'caskroom/fonts/font-pitabek'
cask 'caskroom/fonts/font-plaster'
cask 'caskroom/fonts/font-play'
cask 'caskroom/fonts/font-playball'
cask 'caskroom/fonts/font-playfair-display-sc'
cask 'caskroom/fonts/font-playfair-display'
cask 'caskroom/fonts/font-podkova'
cask 'caskroom/fonts/font-poetsenone'
cask 'caskroom/fonts/font-poiret-one'
cask 'caskroom/fonts/font-poller-one'
cask 'caskroom/fonts/font-poly'
cask 'caskroom/fonts/font-pompiere'
cask 'caskroom/fonts/font-pontano-sans'
cask 'caskroom/fonts/font-poppins'
cask 'caskroom/fonts/font-port-lligat-sans'
cask 'caskroom/fonts/font-port-lligat-slab'
cask 'caskroom/fonts/font-prata'
cask 'caskroom/fonts/font-preahvihear'
cask 'caskroom/fonts/font-press-start2p'
cask 'caskroom/fonts/font-prime'
cask 'caskroom/fonts/font-prince-valiant'
cask 'caskroom/fonts/font-princess-sofia'
cask 'caskroom/fonts/font-prociono'
cask 'caskroom/fonts/font-profontx'
cask 'caskroom/fonts/font-prosto-one'
cask 'caskroom/fonts/font-pt-mono'
cask 'caskroom/fonts/font-pt-sans'
cask 'caskroom/fonts/font-pt-serif'
cask 'caskroom/fonts/font-puritan'
cask 'caskroom/fonts/font-purple-purse'
cask 'caskroom/fonts/font-qataban'
cask 'caskroom/fonts/font-quando'
cask 'caskroom/fonts/font-quantico'
cask 'caskroom/fonts/font-quattrocento-sans'
cask 'caskroom/fonts/font-quattrocento'
cask 'caskroom/fonts/font-questrial'
cask 'caskroom/fonts/font-quicksand'
cask 'caskroom/fonts/font-quintessential'
cask 'caskroom/fonts/font-quivira'
cask 'caskroom/fonts/font-qwigley'
cask 'caskroom/fonts/font-racing-sans-one'
cask 'caskroom/fonts/font-radley'
cask 'caskroom/fonts/font-rajdhani'
cask 'caskroom/fonts/font-raleway-dots'
cask 'caskroom/fonts/font-raleway'
cask 'caskroom/fonts/font-rambla'
cask 'caskroom/fonts/font-rammetto-one'
cask 'caskroom/fonts/font-ranchers'
cask 'caskroom/fonts/font-rancho'
cask 'caskroom/fonts/font-rationale'
cask 'caskroom/fonts/font-red-october'
cask 'caskroom/fonts/font-redacted'
cask 'caskroom/fonts/font-redressed'
cask 'caskroom/fonts/font-reenie-beanie'
cask 'caskroom/fonts/font-revalia'
cask 'caskroom/fonts/font-ribeye-marrow'
cask 'caskroom/fonts/font-ribeye'
cask 'caskroom/fonts/font-ricty-diminished'
cask 'caskroom/fonts/font-righteous'
cask 'caskroom/fonts/font-risque'
cask 'caskroom/fonts/font-roboto-condensed'
cask 'caskroom/fonts/font-roboto-mono-for-powerline'
cask 'caskroom/fonts/font-roboto-mono'
cask 'caskroom/fonts/font-roboto-slab'
cask 'caskroom/fonts/font-roboto'
cask 'caskroom/fonts/font-rochester'
cask 'caskroom/fonts/font-rock-salt'
cask 'caskroom/fonts/font-rokkitt'
cask 'caskroom/fonts/font-romanesco'
cask 'caskroom/fonts/font-ropa-sans'
cask 'caskroom/fonts/font-rosario'
cask 'caskroom/fonts/font-rosarivo'
cask 'caskroom/fonts/font-rotinonhsonni-sans'
cask 'caskroom/fonts/font-rotinonhsonni-serif'
cask 'caskroom/fonts/font-rouge-script'
cask 'caskroom/fonts/font-rounded-m-plus'
cask 'caskroom/fonts/font-rozha-one'
cask 'caskroom/fonts/font-ruda'
cask 'caskroom/fonts/font-rufina'
cask 'caskroom/fonts/font-ruge-boogie'
cask 'caskroom/fonts/font-ruluko'
cask 'caskroom/fonts/font-rum-raisin'
cask 'caskroom/fonts/font-rupakara'
cask 'caskroom/fonts/font-ruslan-display'
cask 'caskroom/fonts/font-russo-one'
cask 'caskroom/fonts/font-ruthie'
cask 'caskroom/fonts/font-rye'
cask 'caskroom/fonts/font-sacramento'
cask 'caskroom/fonts/font-sadagolthina'
cask 'caskroom/fonts/font-sail'
cask 'caskroom/fonts/font-salsa'
cask 'caskroom/fonts/font-samim'
cask 'caskroom/fonts/font-sanchez'
cask 'caskroom/fonts/font-sancreek'
cask 'caskroom/fonts/font-sansita-one'
cask 'caskroom/fonts/font-sarina'
cask 'caskroom/fonts/font-sarpanch'
cask 'caskroom/fonts/font-satisfy'
cask 'caskroom/fonts/font-scada'
cask 'caskroom/fonts/font-scheherazade'
cask 'caskroom/fonts/font-schoolbell'
cask 'caskroom/fonts/font-seaweed-script'
cask 'caskroom/fonts/font-seoulhangang'
cask 'caskroom/fonts/font-seoulhangangcondensed'
cask 'caskroom/fonts/font-sevillana'
cask 'caskroom/fonts/font-seymour-one'
cask 'caskroom/fonts/font-shabnam'
cask 'caskroom/fonts/font-shadows-into-light-two'
cask 'caskroom/fonts/font-shadows-into-light'
cask 'caskroom/fonts/font-shanti'
cask 'caskroom/fonts/font-share-tech-mono'
cask 'caskroom/fonts/font-share-tech'
cask 'caskroom/fonts/font-share'
cask 'caskroom/fonts/font-shojumaru'
cask 'caskroom/fonts/font-short-stack'
cask 'caskroom/fonts/font-siemreap'
cask 'caskroom/fonts/font-sigmar-one'
cask 'caskroom/fonts/font-signika-negative'
cask 'caskroom/fonts/font-signika'
cask 'caskroom/fonts/font-silent-lips'
cask 'caskroom/fonts/font-simonetta'
cask 'caskroom/fonts/font-sinkin-sans'
cask 'caskroom/fonts/font-sintony'
cask 'caskroom/fonts/font-sirin-stencil'
cask 'caskroom/fonts/font-six-caps'
cask 'caskroom/fonts/font-skola-sans'
cask 'caskroom/fonts/font-skranji'
cask 'caskroom/fonts/font-slackey'
cask 'caskroom/fonts/font-smokum'
cask 'caskroom/fonts/font-smythe'
cask 'caskroom/fonts/font-sniglet'
cask 'caskroom/fonts/font-snippet'
cask 'caskroom/fonts/font-snowburst-one'
cask 'caskroom/fonts/font-sofadi-one'
cask 'caskroom/fonts/font-sofia'
cask 'caskroom/fonts/font-sonsie-one'
cask 'caskroom/fonts/font-sorts-mill-goudy'
cask 'caskroom/fonts/font-source-code-pro-for-powerline'
cask 'caskroom/fonts/font-source-code-pro'
cask 'caskroom/fonts/font-source-han-code-jp'
cask 'caskroom/fonts/font-source-han-sans'
cask 'caskroom/fonts/font-source-sans-pro'
cask 'caskroom/fonts/font-source-serif-pro'
cask 'caskroom/fonts/font-space-mono'
cask 'caskroom/fonts/font-special-elite'
cask 'caskroom/fonts/font-spicy-rice'
cask 'caskroom/fonts/font-spinnaker'
cask 'caskroom/fonts/font-spirax'
cask 'caskroom/fonts/font-squada-one'
cask 'caskroom/fonts/font-stalemate'
cask 'caskroom/fonts/font-stalinist-one'
cask 'caskroom/fonts/font-stardos-stencil'
cask 'caskroom/fonts/font-stint-ultra-condensed'
cask 'caskroom/fonts/font-stint-ultra-expanded'
cask 'caskroom/fonts/font-stoke'
cask 'caskroom/fonts/font-strait'
cask 'caskroom/fonts/font-stroke'
cask 'caskroom/fonts/font-sue-ellen-francisco'
cask 'caskroom/fonts/font-sunshiney'
cask 'caskroom/fonts/font-supermercado-one'
cask 'caskroom/fonts/font-swanky-and-moo-moo'
cask 'caskroom/fonts/font-symbola'
cask 'caskroom/fonts/font-syncopate'
cask 'caskroom/fonts/font-tai-le-valentinium'
cask 'caskroom/fonts/font-takaoex'
cask 'caskroom/fonts/font-tangerine'
cask 'caskroom/fonts/font-taprom'
cask 'caskroom/fonts/font-tauri'
cask 'caskroom/fonts/font-teko'
cask 'caskroom/fonts/font-telex'
cask 'caskroom/fonts/font-tenor-sans'
cask 'caskroom/fonts/font-terminus'
cask 'caskroom/fonts/font-tex-gyre-adventor'
cask 'caskroom/fonts/font-tex-gyre-bonum'
cask 'caskroom/fonts/font-tex-gyre-chorus'
cask 'caskroom/fonts/font-tex-gyre-cursor'
cask 'caskroom/fonts/font-tex-gyre-heros'
cask 'caskroom/fonts/font-tex-gyre-pagella-math'
cask 'caskroom/fonts/font-tex-gyre-pagella'
cask 'caskroom/fonts/font-tex-gyre-schola'
cask 'caskroom/fonts/font-tex-gyre-termes'
cask 'caskroom/fonts/font-text-me-one'
cask 'caskroom/fonts/font-thabit'
cask 'caskroom/fonts/font-the-girl-next-door'
cask 'caskroom/fonts/font-tibetan-machine-uni'
cask 'caskroom/fonts/font-tienne'
cask 'caskroom/fonts/font-tillana'
cask 'caskroom/fonts/font-times-new-roman'
cask 'caskroom/fonts/font-tinos'
cask 'caskroom/fonts/font-titan-one'
cask 'caskroom/fonts/font-titillium-web'
cask 'caskroom/fonts/font-trade-winds'
cask 'caskroom/fonts/font-trebuchet-ms'
cask 'caskroom/fonts/font-trocchi'
cask 'caskroom/fonts/font-trochut'
cask 'caskroom/fonts/font-trykker'
cask 'caskroom/fonts/font-tuffy'
cask 'caskroom/fonts/font-tulpen-one'
cask 'caskroom/fonts/font-twitter-color-emoji'
cask 'caskroom/fonts/font-ubuntu-mono-derivative-powerline'
cask 'caskroom/fonts/font-ubuntu'
cask 'caskroom/fonts/font-ultra'
cask 'caskroom/fonts/font-uncial-antiqua'
cask 'caskroom/fonts/font-underdog'
cask 'caskroom/fonts/font-unica-one'
cask 'caskroom/fonts/font-unifrakturcook'
cask 'caskroom/fonts/font-unifrakturmaguntia'
cask 'caskroom/fonts/font-unkempt'
cask 'caskroom/fonts/font-unlock'
cask 'caskroom/fonts/font-unna'
cask 'caskroom/fonts/font-vampiro-one'
cask 'caskroom/fonts/font-varela-round'
cask 'caskroom/fonts/font-varela'
cask 'caskroom/fonts/font-vast-shadow'
cask 'caskroom/fonts/font-vazir-code'
cask 'caskroom/fonts/font-vazir'
cask 'caskroom/fonts/font-verdana'
cask 'caskroom/fonts/font-vibur'
cask 'caskroom/fonts/font-vidaloka'
cask 'caskroom/fonts/font-viga'
cask 'caskroom/fonts/font-voces'
cask 'caskroom/fonts/font-volkhov'
cask 'caskroom/fonts/font-vollkorn'
cask 'caskroom/fonts/font-voltaire'
cask 'caskroom/fonts/font-vt323'
cask 'caskroom/fonts/font-waiting-for-the-sunrise'
cask 'caskroom/fonts/font-wakor'
cask 'caskroom/fonts/font-wallpoet'
cask 'caskroom/fonts/font-walter-turncoat'
cask 'caskroom/fonts/font-waltograph'
cask 'caskroom/fonts/font-warnes'
cask 'caskroom/fonts/font-webdings'
cask 'caskroom/fonts/font-wellfleet'
cask 'caskroom/fonts/font-wendy-one'
cask 'caskroom/fonts/font-wenquanyi-micro-hei-lite'
cask 'caskroom/fonts/font-wenquanyi-micro-hei'
cask 'caskroom/fonts/font-wenquanyi-zen-hei'
cask 'caskroom/fonts/font-wire-one'
cask 'caskroom/fonts/font-work-sans'
cask 'caskroom/fonts/font-xits'
cask 'caskroom/fonts/font-yanone-kaffeesatz'
cask 'caskroom/fonts/font-yellowtail'
cask 'caskroom/fonts/font-yeseva-one'
cask 'caskroom/fonts/font-yesteryear'
cask 'caskroom/fonts/font-zeyada'

########################### TODO ############################################

## Utility-Related

# Alfred: boost your efficiency with hotkeys, keywords, text expansion, etc.
brew 'alfred'

## Serializers

# Protocol buffers for serializing structured data; compare thrift.
brew 'protobuf'
brew 'protobuf-c'

# Thrift network serialization protocol; compare protobuf.
brew 'thrift'

## Tools

# Ansible is a simple way to automate apps and IT infrastructure.
brew 'ansible'
