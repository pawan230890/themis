# Setup

Make install for themis core lib
```
git clone https://github.com/cossacklabs/themis.git
cd themis
sudo make install
```


Make intstall for phpthemis

```
cd tests/phpthemis
sudo make phpthemis_install
```

# Unit tests


You can use shell scripts  for convenience
```
composer_setup.sh # to setup PHP Composer

#  for PHP 5.6
init_env-php5.6.sh

# for PHP 7.0+
init_env-php7.sh

```

Or proceed manually.

Install Composer locally

```console
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

```

Check you current php version
```console
# to see current state
update-alternatives --display php
# to list all options
update-alternatives --list php
# to set the very one
sudo update-alternatives --set php <path_to_php>
```

Link version specific composer config
```console
ln -s composer-php<version>.json composer.json
```

Update environment
```console
php composer.phar update
```
