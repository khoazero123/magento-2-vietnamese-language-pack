composer config repositories.khoazero123/magento-2-vietnamese-language-pack vcs https://github.com/khoazero123/magento-2-vietnamese-language-pack.git
composer require khoazero123/magento-2-vietnamese-language-pack:dev-master


php bin/magento i18n:collect-phrases -o "app/i18n/mageplaza/vi_VN/vi_VN.csv" -m
php bin/magento i18n:pack -d app/i18n/mageplaza/vi_VN/vi_VN.csv vi_VN

php bin/magento setup:static-content:deploy vi_VN
