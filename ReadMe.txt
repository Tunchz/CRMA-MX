// to run project

// 1: generate all needed files and start current project
go generate ./...
go run *.go

// 2: build go project
go generate ./...
CGO_ENABLED=0 go build






// to install golang on ubuntu 22.04

// 1: update the packages and repositories
sudo apt update && sudo apt upgrade

// 2: install go **** do not use >>> sudo apt install golang-go >>> DO NOT WORK
// --- load packages >>> check available version from >>> https://go.dev/dl/
wget https://go.dev/dl/go1.23.12.linux-amd64.tar.gz -O go.tar.gz
// --- extract go to /usr/local
sudo tar -xzvf go.tar.gz -C /usr/local
// --- set PATH variable
echo export PATH=$HOME/go/bin:/usr/local/go/bin:$PATH >> ~/.profile
source ~/.profile

// 3: Verify GO installation
// --- check version
go version


// Note for config
I am able to call the /v3/paths/list from another machine.
Please also check that you're not using the legacy readUser, readPass, publishUser, publishPass inside any path, since these trigger a legacy mode in which the API can be accessed by localhost only.