## Solana Cluster Installation

## Install cURL and git 

    sudo -i apt install curl 
    sudo -i apt install git

## Install Rust

Install the stable version of Rust

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

    source $HOME/.cargo/env
    rustup component add rustfmt

## Install Python3
In most operating systems, Python3 is installed by default. Verify the version of the Python3 

    python3 --version

In case if python3 is not installed, 

    apt install python3

## Install System Dependencies

 - `libssl-dev` 
 - `libudev-dev` 
 - `pkg-config` 
 - `zlib1g-dev` 
 - `llvm` 
 - `clang` 
 - `make`

  Install these dependencies with package manager

     sudo -i apt update 
     sudo -i apt install libssl-dev libudev-dev pkg-config zlib1g-dev llvm clang make

## Mac M1 (Additional Components)
On Mac M1s, make sure we set up terminal and homebrew to use Rosetta. 

    softwareupdate --install-rosetta

## Download Source Code

    git clone https://github.com/solana-labs/solana.git
    cd solana

## Build

    cargo build

## Run a minimal local cluster

    cd scripts
    chmod a+x run.sh
    ./run.sh
