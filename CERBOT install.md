
# Cerbot Installation




## Installation
```bash
    sudo snap install core; sudo snap refresh core
```
```bash
    sudo apt remove certbot
```
```bash
    sudo snap install --classic certbot
```
```bash
    sudo ln -s /snap/bin/certbot /usr/bin/certbot
```
```bash
    sudo certbot --nginx -d example.com -d www.example.com
```


Certbot Auto-Renewal

```bash
    sudo systemctl status snap.certbot.renew.service
```
Output >
```bash
    ○ snap.certbot.renew.service - Service for snap application certbot.renew
        Loaded: loaded (/etc/systemd/system/snap.certbot.renew.service; static)
        Active: inactive (dead)
    TriggeredBy: ● snap.certbot.renew.timer
```
```bash
    sudo certbot renew --dry-run
```