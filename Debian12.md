# flatpak
```
sudo apt install flatpak -y
echo "Kde plasma版"
sudo apt install plasma-discover-backend-flatpak    #kde
gnome-software-plugin-flatpak   #Gnome
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
sudo flatpak remote-modify flathub --url=https://mirror.sjtu.edu.cn/flathub

apt install flatpak gnome-software-plugin-flatpak

flatpak install flathub com.github.tchx84.Flatseal
flatpak install flathub com.tencent.WeChat
flatpak install flathub com.qq.QQ
flatpak install flathub com.visualstudio.code
flatpak install flathub ai.opencode.opencode
flatpak install flathub com.github.gmg137.netease-cloud-music-gtk


```
# 交换文件
```
    #创建一个 32 GiB 的交换文件:
    echo "创建32G交换文件"
    sudo dd if=/dev/zero of=/swapfile bs=1M count=32k status=progress
    sudo chmod 0600 /swapfile
    sudo mkswap -U clear /swapfile
    sudo swapon /swapfile
    sudo sed -i '$a\/swapfile none swap defaults 0 0' /etc/fstab
    # sleep 5
    # sudo reboot

# Arch wiki
/sbin/mkswap -U clear --size 16G --file /swapfile
/sbin/swapon /swapfile

/etc/fstab
/swapfile none swap defaults 0 0

```



# 生产禁用Nouveau文件后更新
```
sudo update-initramfs -u 
```

# 1
```
#sudo apt install ffmpeg default-jdk git wget nano vim htop locate p7zip p7zip-full unzip fonts-wqy-zenhei build-essential -y
```

# Gnome extension
```

gnome-shell-extension-appindicator gnome-shell-extension-desktop-icons-ng  gnome-shell-extension-gpaste 
gnome-shell-extension-kimpanel #fcitx5的Gnome
gnome-shell-extension-bluetooth-quick-connect #Gnome44不需要

apt install gnome-shell-extension-appindicator gnome-shell-extension-desktop-icons-ng  gnome-shell-extension-gpaste gnome-shell-extension-kimpanel gnome-console
```

#NVIDIA
1.执行安装前操作。

2.当前运行的内核的内核头文件和开发包可以通过以下方式安装：
```
sudo apt-get install linux-headers-$(uname -r)
```
3.启用 contrib 存储库：
```
sudo add-apt-repository contrib
```
4.删除过时的签名密钥：
```
sudo apt-key del 7fa2af80
```
