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
sudo apt install php7.1-cli php7.1-common php7.1-curl php7.1-mbstring php7.1-mysql php7.1-xml


wget --no-check-certificate -O shadowsocks-libev-debian.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev-debian.sh
chmod +x shadowsocks-libev-debian.sh

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





