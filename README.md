
# How to setup a new Mac

The following instructions are for someone who is new to Mac and new to programming.

# Enable Rosetta for Terminal on M1

Note: If you are using M1 device make sure to install all dependencies using rosetta terminal.

Rosetta allows us to use apps built for Mac with intel chip.

- Select the app(Terminal) in the Finder.
- Right click on the app(Terminal) and select `Get Info`.
- In General, Check the `Open using Rosetta` check-box.
- Close the `Terminal Info`.
- Now when you quit the terminal and open it again, you’ll be asked to install Rosetta in order to open the Terminal.
- Click on Install button, then enter your user name and password to allow installation to proceed.
- Close the Terminal and open again.
- Confirm that you are using a Rosetta Terminal by entering the `arch` command, which should return `i386`.

# Setting up VSCode

- Install VSCode from [https://code.visualstudio.com](https://code.visualstudio.com/).

### Enable AutoSave

- Go to VSCode application
- Go to File which is next to VScode at the top left corner.
- Under File there is "Auto Save".
- Click on it so that a check mark appears next to it.
- Click on "File" again and this time there should be a check mark next to "Auto Save".

### Enable code command

- Go to VScode application
- Press "Shift" button,  "Command" button and  "p"
- Type > shell command
- Select "Install 'code' command in PATH
- VScode will give you a prompt. Click "Ok".
- VScode will ask for your laptop password. provide password.

Now let's test if command "code" is working or not.

- Open terminal
- type `code dummy.txt`. A dummy.txt file should open in VScode.

# Opening terminal using spotlight

- Press "Command" and then press "space". This will bring up spotlight.
- Spotlight is like a search for your applications, documents etc.
- In the spotlight type "terminal' and hit enter.

# Setting up homebrew

- Now Visit [https://brew.sh/](https://brew.sh/) and copy the command to "install homebrew"
- Open terminal and paste the command on terminal by hitting "Command" and "v". Hit enter.
- This will take a while.
- You will see screen "Downloading Command Line Tools for Xcode". It will see that the screen has frozen but don't worry. It takes a long time to download so please be patient.

# Installing other required applications using homebrew

- Open terminal and run  following commands one by one.

```
brew update
brew install git
brew install openssl
brew install coreutils
brew install wget
```

# Configure Git

- Now execute following commands.
- If you are new to mac then copy these commands one by one.

```
git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global color.branch auto
git config --global color.diff auto
git config --global color.interactive auto
git config --global color.status auto
git config --global branch.autosetuprebase always
git config --global push.default current
git config --global core.mergeoptions --no-edit

```

- For the following command you need to put in your "name" for the first command and you need to put in your "email" for the second command.

```
git config --global user.name "Your-name-here"
git config --global user.email "your-email-here"
```

# Setting up terminal command prompt

Please check [which shell you using](https://unix.stackexchange.com/questions/9501/how-to-test-what-shell-i-am-using-in-a-terminal).


If you are using "zsh" then [install ohmyzsh](https://ohmyz.sh).


<!-- If you are using "bash then following the instructions given below.
- On terminal type `code ~/.bash_profile`
- Replace the existing content with the content from [https://gist.githubusercontent.com/neerajdotname/db6786b44136daeda82a582b644fe57a/raw/49a4e0d91e55ca8cca4252dd1b3d4abe7386c048/bash_profile](https://gist.githubusercontent.com/neerajdotname/db6786b44136daeda82a582b644fe57a/raw/49a4e0d91e55ca8cca4252dd1b3d4abe7386c048/bash_profile)
- Come back to terminal
- On terminal type `code ~/.bashrc`
- At the bottom of the file add content from [https://gist.githubusercontent.com/neerajdotname/fdd5c76e1d5e06da283e416b71adb4fd/raw/8633b61353d7b6d44d68a4e54b8e3451db79dd42/customize_terminal_prompt](https://gist.githubusercontent.com/neerajdotname/fdd5c76e1d5e06da283e416b71adb4fd/raw/8633b61353d7b6d44d68a4e54b8e3451db79dd42/customize_terminal_prompt)
- quit terminal by using "command q"
- Now start terminal
- run `mkdir code`
- run `cd code` -->
- 

# XCode

- Start terminal and type `xcode-select --install` and hit enter.
- If you get the message that "command line tools are already installed" then you are good and you have nothing to worry about.

# Setting up nvm

- Open terminal and execute `brew install nvm`
- Quit terminal using "command q"
- Start terminal and run `mkdir ~/.nvm`
- In terminal run `code ~/.zshrc` and add the following two lines at the bottom of the file.
- `export NVM_DIR="$HOME/.nvm"`
- `. "/usr/local/opt/nvm/nvm.sh"`
- Quit terminal by using "Command q".

# Install node

- Open terminal and execute the following command

`nvm install lts && nvm use lts && nvm alias default lts`

- On terminal type the command `node -v` . If you see `latest lts version` then it means node is correctly installed.

# Install yarn

- brew install yarn
