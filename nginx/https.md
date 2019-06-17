#Steps to enable SSL encryption in `Nginx` with `letsencrypt` 
This post is summarised from this (post)[https://certbot.eff.org/lets-encrypt/arch-nginx.html]

1) install crertbot then run this command `sudo certbot --nginx`
2) `sudo certbot --nginx certonly`
3) done !

## For wildcaed

`sudo certbot -a dns-plugin -i nginx -d "*.example.com" -d example.com --server https://acme-v02.api.letsencrypt.org/directory`

## Automating renewal
1) `sudo certbot renew --dry-run`
2) `certbot renew`
