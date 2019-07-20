# vim编译安装
1. [这里是详细步骤](https://github.com/Valloric/YouCompleteMe/wiki/Building-Vim-from-source)
2. 注意适配自己的场景
```sh
./configure --with-features=huge \
            --enable-multibyte \
	    --enable-rubyinterp=yes \
	    --enable-python3interp=yes \
	    --with-python3-config-dir=/usr/lib/python3.7/config-3.7m-x86_64-linux-gnu \
	    --with-python3-command=python3.7 \
	    --enable-perlinterp=yes \
	    --enable-luainterp=yes \
            --enable-gui=gtk2 \
            --enable-cscope
make -j32 VIMRUNTIMEDIR=/usr/local/share/vim/vim81
```
3. 使用checkinstall安装，可方便卸载，卸载使用`dpkg -r vim`
4. 使用`sudo apt-mark hold vim`，来设置不自动升级vim软件包
    - vim-runtime也可以加上（未知行为，自用）
# 使用vim配置文件
1. $HOME目录下克隆本仓库，`git clone https://github.com/shzxd/.vim.git ~/.vim`
2. 安装Vundle(Vim bundle)`git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
3. 先安装YouCompleteMe
    1. 在Vundle插件目录（~/.vim/bundle/）运行`git clone https://github.com/Valloric/YouCompleteMe.git`
    2. 进入YouCompleteMe仓库目录，运行`git submodule update --init --recursive`
    3. 运行`python3 install.py`（不支持C系语言的安装）
4. 启动Vim并运行`:PluginInstall`
## 其它问题

## TODO
- [ ] airline配置
