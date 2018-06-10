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