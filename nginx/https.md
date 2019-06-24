# Steps to enable SSL encryption in `Nginx` with `letsencrypt` 
This post is summarised from this [post](https://certbot.eff.org/lets-encrypt/arch-nginx.html)

1) install `sudo add-apt-repository ppa:certbot/certbot`
2) `sudo apt-get update`
3) `sudo apt-get install python-certbot-nginx`
4) install crertbot then run this command `sudo certbot --nginx`
5) `sudo certbot --nginx certonly`
6) done !

## For wildcaed

`sudo certbot -a dns-plugin -i nginx -d "*.example.com" -d example.com --server https://acme-v02.api.letsencrypt.org/directory`

## Automating renewal
1) `sudo certbot renew --dry-run`
2) `certbot renew`
