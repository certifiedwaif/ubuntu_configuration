Install git

	sudo apt install -y git
	git config --global user.email "certifiedwaif@gmail.com"
	git config --global user.name "Mark Greenaway"
	mkdir ~/github.com


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
	sudo usermod -aG ${USER} docker

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

  https://flutter.dev/docs/get-started/install/linux
  Run `flutter doctor`
  Add $HOME/flutter/bin to PATH
  sudo apt-get install lib32stdc++6
  flutter doctor --android-licenses

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

Install SSH server

  sudo apt install -y openssh-server

Install Kubernetes

    

