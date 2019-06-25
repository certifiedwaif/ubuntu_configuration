Install git

	sudo apt install -y git
	git config --global user.email "certifiedwaif@gmail.com"
	git config --global user.name "Mark Greenaway"
	mkdir ~/github.com

Create an ssh keypair and install on GitHub

	ssh-keygen

Install curl

	sudo apt install -y curl

Install zsh and Oh My Zsh

	sudo apt install -y zsh
	chsh markg -s /usr/bin/zsh
	sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
	git clone git@github.com:certifiedwaif/zshrc.git

Install vim, and vim configuration

	sudo apt install -y vim-gnome
	cd ~/github.com && git clone https://github.com/certifiedwaif/vimrc.git
	cp ~/github.com/vimrc/vimrc ~/.vimrc
	mkdir -p ~/.vim/bundle/
	git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
	vim +PluginInstall +qall

Create an ssh keypair and install on GitHub

	ssh-keygen

Swap Capslock and Escape

	setxkbmap -option caps:swapescape

Install docker.io

	sudo apt install -y docker.io
	sudo usermod -aG docker ${USER}

Install Google Cloud SDK and initialise the SDK

	# Create environment variable for correct distribution
	CLOUD_SDK_REPO="cloud-sdk-$(grep VERSION_CODENAME /etc/os-release | cut -d '=' -f 2)"

	# Add the Cloud SDK distribution URI as a package source
	echo "deb http://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

	# Import the Google Cloud Platform public key
	curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

	# Update the package list and install the Cloud SDK
	sudo apt update && sudo apt install -y google-cloud-sdk

	gcloud init

Install Synergy

  https://symless.com/synergy/downloads/list/s1

Install htop, iotop, iftop

  sudo apt install -y htop iotop iftop

Install net-tools

  sudo apt install -y net-tools

Install the Hack font

  https://sourcefoundry.org/hack/
  In Edit -> Preferences, set Custom font to Hack Regular 12

Install Anaconda Python distribution

  https://www.anaconda.com/distribution/
  Add $HOME/anaconda3/bin to PATH

Install Android Studio

  https://developer.android.com/studio/?gclid=Cj0KCQjwitPnBRCQARIsAA5n84lJMnj6aa3tHJEhtUbDsM9jZPNGmx_733MH4imSXRVUraOENnwDF3UaApnMEALw_wcB

Install Dart and Flutter

  sudo apt-get update
  sudo apt-get install apt-transport-https
  sudo sh -c 'curl https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add -'
  sudo sh -c 'curl https://storage.googleapis.com/download.dartlang.org/linux/debian/dart_stable.list > /etc/apt/sources.list.d/dart_stable.list'
  sudo apt-get update
  sudo apt-get install dart

  https://flutter.dev/docs/get-started/install/linux
  Run `flutter doctor`
  Add $HOME/flutter/bin to PATH
  sudo apt-get install lib32stdc++6
  flutter doctor --android-licenses
  export PATH="$PATH":"$HOME/flutter/.pub-cache/bin"

Install R and RStudio

  sudo apt install -y r-base
  R -e "install.packages('devtools')"
  https://www.rstudio.com/products/rstudio/download/

Install LaTeX

  sudo apt install -y texlive-full

Install R kernel for Jupyter notebooks

  conda install -c r r-irkernel
  Install libreadline6
    wget  http://mirrors.kernel.org/ubuntu/pool/main/r/readline6/libreadline6_6.3-8ubuntu2_amd64.deb
    sudo dpkg -i 

Install Discord

  https://discordapp.com/download

Install Kubernetes

  https://www.digitalocean.com/community/tutorials/how-to-create-a-kubernetes-cluster-using-kubeadm-on-ubuntu-16-04    

Install lm_sensors, psensor and s-tui

  sudo apt install -y lm-sensors hddtemp
  sudo sensors-detect
  sudo /etc/init.d/kmod start

Install pip, stress

  sudo apt install -y python-pip python3-pip stress
  sudo pip3 install s-tui
  sudo s-tui

Install ansible

  sudo apt install -y ansible

Install tmux

  sudo apt install -y tmux

Install Google Drive Ocamlfuse

  sudo add-apt-repository ppa:alessandro-strada/ppa
  sudo apt update && sudo apt install google-drive-ocamlfuse
  mkdir ~/google-drive
  google-drive-ocamlfuse ~/google-drive

Install latest version of R on Ubuntu Linux

	echo "deb http://cran.stat.ucla.edu/bin/linux/ubuntu bionic-cran35/" | sudo tee -a /etc/apt/sources.list.d/cran.list
	sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E084DAB9

  sudo apt-get update
  sudo apt-get install -y r-base r-base-dev
  #
  # To update any R libraries installed via APT.
  #
  sudo apt-get upgrade

  sudo apt-get remove -y 'r-cran-*'

  Rscript -e "update.packages(ask = FALSE)"

Install ack

  sudo apt install -y ack

Install tree

  sudo apt install -y tree
  
Install gcc-9

  sudo add-apt-repository ppa:jonathonf/gcc-9.0
  sudo apt-get install -y gcc-9

Program NVidia GPUs with OpenMP

  http://on-demand.gputechconf.com/gtc/2016/presentation/s6510-jeff-larkin-targeting-gpus-openmp.pdf

Install npm and Purescript

  curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
## You may also need development tools to build native addons:
     sudo apt-get install gcc g++ make
## To install the Yarn package manager, run:
     curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
     echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
     sudo apt-get update && sudo apt-get install yarn
  sudo apt-get install -y nodejs
  sudo apt install -y npm
  mkdir ~/.npm-global
  npm config set prefix '~/.npm-global'
  echo 'export PATH=~/.npm-global/bin:$PATH' » ~/.zshrc
  npm install -g purescript
  npm install -g pulp
  npm install -g bower
  npm install -g parcel-bundler
