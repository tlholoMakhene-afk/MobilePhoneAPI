# MobilePhoneAPI
Restful API on Mobile Phones


# Contents for .htacess file

# Turn rewrite engine on
Options +FollowSymlinks
RewriteEngine on

# map neat URL to internal URL
RewriteRule ^mobile/list/$   RestController.php?page_key=list [nc,qsa]
RewriteRule ^mobile/list$   RestController.php?page_key=list [nc,qsa]

RewriteRule ^mobile/create/$   RestController.php?page_key=create [L]
RewriteRule ^mobile/create$   mobile/create/ [L,R=301]

RewriteRule ^mobile/delete/([0-9]+)/$   RestController.php?page_key=delete&id=$1 [L]
RewriteRule ^mobile/delete([0-9]+)$   mobile/delete/$1 [L,R=301]

RewriteRule ^mobile/update/([0-9]+)/$   RestController.php?page_key=update&id=$1 [L]
RewriteRule ^mobile/update([0-9]+)$   mobile/update/$1/ [L,R=301]
