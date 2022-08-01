# Marketplace Template Reposotory

## Expected system versions
- ubuntu18.04
- MySQL5.7
- php7.2
- elasticsearch7.6.2

## How to use it

Deploy source code and setup
```
git clone git@gitlab.com:true-mp/mp-template.git [your_project_name]
cd [your_project_name]
chmod 777 -R ./var
chmod 777 -R ./generated
chmod 777 -R ./app/etc
chmod 777 -R ./pub/media
chmod 777 -R ./pub/static
composer update
```

Imstall Magento2 by using following command with options
*You have to fill options before you execute this command!
```
./bin/magento setup:install
--base-url= \
--db-host= \
--db-name= \
--db-user= \
--db-password= \
--admin-firstname= \
--admin-lastname= \
--admin-email= \
--admin-user= \
--admin-password= \
--language=ja_JP \
--currency=JPY \
--timezone=Asia/Tokyo \
--backend-frontname=
```
or
from browser.
Go to http://your_project_url

## Included extension list

### Magento

- Paypal
Magento/Paypal module modified to use it for JP Yen.

### CommunityEngineering JP Localization
https://github.com/magento/magento2-jp

- Kuromoji
(For elasticsearch kuromoji)

### Webkul

- Marketplace
Marketplace extension.
- Marketplace API
Marketplace API extension.
- MarketPlaceBaseShipping
Extension to enable sellers to set Table Rate Shipping for them.
- MarketPlaceAssignProduct
Extension to enable sellers to sell common products.
- MarketPlaceTimeDelivery
Extension to enable sellers to set Delivery Time for them.
- MarketPlaceShipping
Extension to enable sellers to set Shipping Method for them.


Bạn hãy điều tra công số cần thiết để thay đổi url của privacy policy cho seller bên front page

Lý do
Liên quan tới issue issue 186 #74891 tôi muốn làm cho url của "privacy policy" hiển thị phù hợp với text "display based on the Act on Specified Commercial Transactions"

Url hiện tại
https://mpx.true-inc.jp/index.php/marketplace/seller/policy/shop/[shopurl]
=>
Url sau khi thay đổi
https://mpx.true-inc.jp/index.php/marketplace/seller/tokuteitorihiki/shop/[shopurl]
[shopurl] là variable

Phần "policy" thay thành "tokuteitorihiki"


Đồng thời thay đổi cả link source url


