#### 安装oh-my-zsh

1. 安装zsh

```shell
sudo apt install zsh
```

2. 使用curl下载oh-my-zsh

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

3. 变更默认的shell

```shell
chsh -s /usr/bin/zsh
```

4. 查看当前使用的shell

```shell
echo $SHELL
```

5. 修改配置文件

```shell
ZSH_THEME="frontcube"
plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
```

6. 安装插件

```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```