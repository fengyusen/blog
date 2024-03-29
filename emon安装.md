## ssh 配置

基本用法 ssh user@remote -p port

ssh-keygen 生成ssh密钥，公钥： ~/.ssh/id_rsa.pub，私钥： ~/.ssh/id_rsa

设置免密连接：ssh-copy-id user@remote -p port

Mac ： brew install ssh-copy-id

一句话搞定：ssh user@remote -p port 'mkdir -p .ssh && cat >> .ssh/authorized_keys' < ~/.ssh/id_rsa.pub

配置别名 vim .ssh/config

```
Host host_name
		HostName host_ip
		User user_name
		Port port
```



## Oh my zsh 配置教程

- **Oh My Zsh** 是一款社区驱动的命令行工具，正如它的主页上说的，**Oh My Zsh** 是一种生活方式。它基于 **zsh** 命令行，提供了主题配置，插件机制，已经内置的便捷操作。给我们一种全新的方式使用命令行。
- **Oh My Zsh** 是基于 **zsh** 命令行的一个扩展工具集，提供了丰富的扩展功能。
- 安装 **Oh My Zsh** 前提条件：必须已安装 **zsh**

1. 安装 zsh

​		Mac 直接用

​		Ubuntu ： sudo apt-get install zsh

​		fedora :  sudo dnf install -y zsh

2. 安装oh my zsh

```powershell
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
wget https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh

sh install.sh
```

3. 配置插件

   1. autojump

      Mac: brew install autojump

      linux: 

   ```powershell
   sudo apt install autojump
   
   git clone git://github.com/wting/autojump.git
   
   cd autojump
   ./install.py or ./uninstall.py
   ```

   2. zsh-autosuggestions

   ```powershell
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
   
   brew install zsh-autosuggestions
   ```

   3. zsh-syntax-highlighting

   ```powershell
   git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
   ```

 4. 编辑.zshrc

    ```powershell
    vim .zshrc
    
    ZSH_THEME="ys"
    
    plugins=( git autojump zsh-autosuggestions zsh-syntax-highlighting)
    ```



## python conda 配置

Linux 下载miniconda

``` powershell
wget https://mirrors.tuna.tsinghua.edu.cn/anaconda/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
ls
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes 
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

# 设置默认进入base
conda config --set auto_activate_base false

cat /etc/issue #查看cuda
nvidia-smi #查看显卡型号
cat /proc/driver/nvidia/version # 查看显卡驱动版本

conda env list # 展示环节列表
conda create --name myenv python==版本号 # 创建环境
conda activate myenv # 进入环境
conda deactivate # 退出环境
conda remove -n myenv --all # 删除环境

```

















我对这个项目充满兴趣，并且很愿意投入其中努力做出点贡献。而且如果能够参与进去并有所产出，会对毕业成果有很大帮助。这个问题您上周就提过，如何将CPU算力归一化，并不是一个容易解决的问题，我很愿意深入学习来进行尝试。在此基础上的应用容量规划也是一个很关键的问题，我对类似调度优化问题也很有兴趣。

I am very interested in this project and am eager to invest effort to make a meaningful contribution. Furthermore, if I can participate and produce results, it will greatly benefit my graduation outcomes. You raised the issue of normalizing CPU compute power this week, and it's not an easy problem to solve. I'm very willing to dive deep into studying it and attempting to address it. Capacity planning based on this normalization is also a critical issue, and I have a strong interest in similar scheduling optimization problems.
