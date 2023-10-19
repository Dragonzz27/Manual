#### 添加windows字体

1. 下载Fonts字体到~/Downloads文件夹

2. 创建字体存放目录windows-fonts

```shell
sudo mkdir /usr/share/fonts/truetype/windows-fonts
```

3. 拷贝字体到windows-font目录下

```shell
sudo cp ~/Downloads/Fonts/* /usr/share/fonts/truetype/windows-fonts

```

3. 修改权限，更新字体缓存

```shell
sudo chmod -R 777 /usr/share/fonts/truetype/windows-fonts

cd /usr/share/fonts/truetype/windows-fonts

sudo mkfontscale

sudo mkfontdir

sudo fc-cache -fv
```