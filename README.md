# Vimlander 3

This is near copy of [Vimlander-2-The-Quickening](https://github.com/spicycode/Vimlander-2-The-Quickening). However, Vimlander causes editor bugs whenever I install it so I have modified it to reduce editor glitches.

## Setting up Vimlander 3

1. Clone this repository wherever you want. I put mine in a projects directory:
```
cd /Users/robskrob/code/projects/

git clone git@github.com:robskrob/Vimlander-3.git
```

2. In your user root directory /Users/your-user-name, make sure that `.vim`, `.vimrc` and `.gvimrc` do not exist.

3. Provided that they are not there, create the following symbolic links:

```bash
$ ln -s /Users/yourusername/path/to/project/Vimlander-3 /Users/yourusername/.vim
$ ln -s /Users/yourusername/path/to/project/Vimlander-3/vimrc /Users/yourusername/.vimrc
$ ln -s /Users/yourusername/path/to/project/Vimlander-3/gvimrc /Users/yourusername/.gvimrc
```

4. Run `$ ls -al` in your user root directory to make sure that your symbolic links have been created. They should look like the following:

```bash
.gvimrc -> /Users/yourusername/path/to/project/Vimlander-3/gvimrc
.vim -> /Users/yourusername/path/to/project/Vimlander-3/
.vimrc -> /Users/yourusername/path/to/projet/Vimlander-3/vimrc
```

5. Set up `Vundle`:
```bash
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

6. Install the plugins. Note when you first install the packages you will see errors, but they are harmless. Vim is complaining about the plugins not being there, which makes sense because, indeed, the do not exist. However, they will exist once you run:
```bash
vim +PluginInstall +qall
```
