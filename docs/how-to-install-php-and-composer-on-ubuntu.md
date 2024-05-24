# webdev draft

- 如何安裝 php
```sh
# 更新
sudo apt update

# 安裝 php
sudo apt install php php-cli php-mbstring php-xml php-zip php-curl

# 檢查 php 版本
php -v
```

- 如何安裝 composer
```sh
# 下載安裝檔
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer

# 驗證安裝檔
HASH="$(wget -q -O - https://composer.github.io/installer.sig)"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

# 執行安裝檔
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer

# 檢查 composer 版本
composer --version
```
