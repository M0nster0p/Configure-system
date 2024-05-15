# Configure-system

# Installing platform tools
```
wget https://dl.google.com/android/repository/platform-tools-latest-linux.zip
```

```
unzip platform-tools-latest-linux.zip -d ~
```

```
nano ~/.profile 
```

# copy paste the below code into ~/.profile
```
# add Android SDK platform tools to path
if [ -d "$HOME/platform-tools" ] ; then
    PATH="$HOME/platform-tools:$PATH"
fi
```


# now Installing varios tools requried for compiling a rom

```
cd ~/
git clone https://github.com/akhilnarang/scripts
cd scripts
./setup/android_build_env.sh
```



# repo initating // basically android from google (my perception)
```
sudo apt install git
```
```
mkdir -p ~/bin
```
```
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
```

# add this bin to ~/.profile
```
nano ~/.profile
```

# only add if not already present there, if its already there leave it as it is
```
# set PATH so it includes user's private bin if it exists
if [ -d "$HOME/bin" ] ; then
    PATH="$HOME/bin:$PATH"
fi
```

# lastly configure your git
```
git config --global user.email "your@gmail.com"
git config --global user.name "your name"
```

