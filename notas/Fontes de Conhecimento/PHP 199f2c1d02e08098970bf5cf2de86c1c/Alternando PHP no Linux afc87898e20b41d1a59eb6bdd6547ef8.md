# Alternando PHP no Linux

Instalação do Espelho

```bash
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt update
```

Instalação do PHP

```bash
sudo apt install php7.4
```

Instalação das extensões PHP

```bash
sudo apt install php7.4-common php7.4-mysql php7.4-xml php7.4-xmlrpc php7.4-curl php7.4-gd php7.4-imagick php7.4-cli php7.4-dev php7.4-imap php7.4-mbstring php7.4-opcache php7.4-soap php7.4-zip php7.4-intl -y
```

Alternando a versão 

```bash
update-alternatives --set php /usr/bin/php7.4
```