# Dynamic Virtual Hosting
Please read notes.

## Preparation
The Apache 2 directory structure must consist of following settings. Following such structure you can add any all your domains with any necessary web-sub domains.

### Default IP address access
```
/var/www/255.255.255.255/public/
```

### User's domain with sub-domains
```
# root domain's directory - example: domain.com and www.domain.com
/var/www/domain.com/www/public/

# other sub-domains for example: blog.domain.com
/var/www/domain.com/blog/public/

# and other sub-domains for example: test.domain.com
/var/www/domain.com/test/public/
```

### Apache 2 mods
```
a2enmod rewrite
a2enmod vhost_alias
a2enmod ssl
```

### Installation
```
sudo cp apache2/sites-available/dynamic-virtual-hosts.conf /etc/apache2/sites-available/dynamic-virtual-hosts.conf
sudo cp apache2/sites-available/default-virtual-hosts.conf /etc/apache2/sites-available/default-virtual-hosts.conf
sudo apachectl restart apache2
```

## Good luck.
Please ask questions.