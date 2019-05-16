# vim编译安装
1. [这里是详细步骤](https://github.com/Valloric/YouCompleteMe/wiki/Building-Vim-from-source)
2. 注意适配自己的场景
    ```  
        --with-python3-config-dir=/usr/lib/python3.5/config-3.5m-x86_64-linux-gnu \
        --with-python3-command=python3.5 \
        --enable-gui=gnome2 \
    ```
# vim配置文件
1. 安装Vundle(Vim bundle)`git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
2. 启动Vim并运行`:PluginInstall`
## 其它问题
* YouCompleteMe安装不成功
    1. 在Vundle插件目录（~/.vim/bundle/）运行`git clone https://github.com/Valloric/YouCompleteMe.git`
    2. 进入YouCompleteMe仓库目录，运行`git submodule update --init --recursive`
    3. 运行`python3 install.py`（不支持C系语言的安装）
## TODO
- [ ] airline配置
