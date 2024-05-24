# installation

### 如何安裝 php
```sh
# 更新
sudo apt update

# 安裝 php
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt install php8.2 php8.2-cli php8.2-fpm php8.2-mysql php8.2-xml php8.2-mbstring php8.2-curl php8.2-zip php8.2-gd php8.2-sqlite3

# 檢查 php 版本
php -v
```

### 如何安裝 composer
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

### Laravel 如何建立新專案
```sh
# 建立新專案
composer create-project laravel/laravel chirper

# 執行測試環境
cd chirper
php artisan serve
```

---

### 如何安裝 node & npm
```sh
# 安裝
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs

# 檢查 npm 版本
npm -v
```

### 安裝 Laravel Breeze 會員模組
備註：需要先安裝 node & npm

```sh
# 安裝模組
composer require laravel/breeze --dev
php artisan breeze:install blade

# 編譯 Vite
npm run dev
```
