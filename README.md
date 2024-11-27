<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1 align="center">
        <img src="https://github.com/Nightro-Fx/Ubuntu-Golang-Installation/blob/main/img/Go.png" width="70" alt="Logo"/> 
        Golang Installation Guide
    </h1>
</body>
</html>

###### Removing the previous version of go (if any)
```bash
sudo snap remove go
sudo rm -rf /usr/local/go
```

###### Downloading the latest version of Golang
```bash
sudo snap install go --classic
wget https://go.dev/dl/go1.23.3.linux-amd64.tar.gz
```
###### Extracting the new version to `/usr/local`
```bash
sudo tar -C /usr/local -xzf go1.23.3.linux-amd64.tar.gz
```
###### Opening your shell config
```bash
sudo nano ~/.bashrc
```
###### Updating your `PATH` variable. Go to the very end of the file and add this:
```bash
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
```
###### Reloading your shell config
```bash
source ~/.bashrc
```
###### Check your new version
```bash 
go version
```
