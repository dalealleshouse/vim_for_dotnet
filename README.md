# Prerequisites:

- [dotnet](https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu)
    ``` bash
    wget https://packages.microsoft.com/config/ubuntu/21.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
    sudo dpkg -i packages-microsoft-prod.deb
    rm packages-microsoft-prod.deb

    sudo apt-get update; \
      sudo apt-get install -y apt-transport-https && \
      sudo apt-get update && \
      sudo apt-get install -y dotnet-sdk-5.0
    ```
- Python 3 with development headers
    ```bash
    sudo apt-get install python3-dev cmake build-essential
    ```
- Build tools (required for _You Complete Me_)
    ```bash
    sudo apt-get install cmake build-essential
    ```

# Vim Plugin Manager
My preference is [pathogen](https://github.com/tpope/vim-pathogen), but any will
work

``` bash
mkdir -p ~/.vim/autoload ~/.vim/bundle && \
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
```

Update/create `~/.vimrc`

```
call pathogen#infect()
syntax on
filetype plugin indent on
```

# Project Explorer
My preference is [Nerd Tree](https://github.com/preservim/nerdtree)

``` bash
git clone https://github.com/preservim/nerdtree.git ~/.vim/bundle/nerdtree
```

# dotnet Language Server
[OmniSharp](https://github.com/OmniSharp/omnisharp-vim)

``` bash
git clone git://github.com/OmniSharp/omnisharp-vim ~/.vim/bundle/OmniSharp
```

# Some Nice Shortcuts
[Sharpen Up!](https://github.com/nickspoons/vim-sharpenup)

``` bash
git clone git://github.com/nickspoons/vim-sharpenup.git ~/.vim/bundle/vim-sharpenup
```

# Lint Server
My preference is [ALE](https://github.com/dense-analysis/ale)

``` bash
git clone git://github.com/dense-analysis/ale.git ~/.vim/bundle/ale
```

# Intellisense
My preference is [You Complete Me](https://github.com/ycm-core/YouCompleteMe)

``` bash
git clone git://github.com/Valloric/YouCompleteMe.git ~/.vim/bundle/YouCompleteMe
cd ~/.vim/bundle/YouCompleteMe
git submodule update --init --recursive
./install.py
```
