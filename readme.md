# Debian OS config example

changing ssh port, note it is `sshd_config`, not `ssh_config`

```
vi /etc/ssh/sshd_config
```

check ssh key

```
cat ~/.ssh/id_rsa.pub
```

generating ssh-key

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
cat ~/.ssh/id_rsa.pub
```

```bash
apt update
apt install wget curl git htop zsh
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

apt install nginx

mysql
wget https://repo.mysql.com//mysql-apt-config_0.8.12-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.12-1_all.deb
apt update


cat /etc/os-release

# https://tecadmin.net/install-php-debian-9-stretch/
sudo apt install ca-certificates apt-transport-https
wget -q https://packages.sury.org/php/apt.gpg -O- | sudo apt-key add -
echo "deb https://packages.sury.org/php/ stretch main" | sudo tee /etc/apt/sources.list.d/php.list
apt install php7.1-cli php7.1-common php7.1-curl php7.1-mbstring php7.1-mysql php7.1-xml php7.1-fpm

missing extension when composer install in laravel 5.5 project
apt install php7.1-bcmath
```

for laravel 5.5

```

apt install php7.1-mysqlnd
apt install php7.1-opcache
apt install php7.1-pdo
apt install php7.1-xml
apt install php7.1-calendar
apt install php7.1-ctype
apt install php7.1-curl
apt install php7.1-dom
apt install php7.1-exif
apt install php7.1-fileinfo
apt install php7.1-ftp
apt install php7.1-gettext
apt install php7.1-iconv
apt install php7.1-json
apt install php7.1-mbstring
apt install php7.1-mysqli
apt install php7.1-pdo_mysql
apt install php7.1-tokenizer
apt install php7.1-wddx
apt install php7.1-xmlreader
apt install php7.1-xmlwriter
apt install php7.1-xsl

```

bbr config

https://www.mf8.biz/debian9-bbr/

修改系统变量：

```
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
```

保存生效

```
sysctl -p
```

执行

```
sysctl net.ipv4.tcp_available_congestion_control
```

如果结果是这样

```
"rootMF8-BIZ sysctl net.ipv4.tcp_available_congestion_control
net.ipv4.tcp_available_congestion_control = bbr cubic reno
```

就开启了。

执行 lsmod | grep bbr ，以检测 BBR 是否开启。

get shadowsocks

```

wget --no-check-certificate -O shadowsocks-libev-debian.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev-debian.sh
chmod +x shadowsocks-libev-debian.sh
./shadowsocks-libev-debian.sh

```

shadowsocks
cat /etc/shadowsocks-libev/config.json
example config

```

{
"server":"0.0.0.0",
"server_port":12345,
"password":"12345",
"timeout":300,
"user":"nobody",
"method":"aes-256-gcm",
"fast_open":false,
"nameserver":"8.8.8.8",
"mode":"tcp_and_udp"
}

```

nodejs 11

# Using Debian, as root

```

curl -sL https://deb.nodesource.com/setup_11.x | bash -
apt-get install -y nodejs

```

nvm

removed 295 packages in 14.895s
➜ ~ npm -v
6.5.0
➜ ~ node -v
v11.9.0

composer install memory error

```

/bin/dd if=/dev/zero of=/var/swap.1 bs=1M count=1024
/sbin/mkswap /var/swap.1
/sbin/swapon /var/swap.1

```

```

```
