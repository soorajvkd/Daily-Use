
# AWS Static Web site host




## Installation

Install my-project with npm

```bash
    sudo apt update
    sudo apt install nginx
```
```bash
    sudo ufw app list
```
```bash
    systemctl status nginx
```
```bash
    sudo systemctl start nginx
    sudo systemctl stop nginx
    sudo systemctl enable nginx
    sudo systemctl disable nginx
```

```bash
    sudo systemctl restart nginx
```
```bash
    sudo systemctl reload nginx
```

```bash
    sudo mkdir -p /var/www/your_domain
```
read and execute permissions
```bash
    sudo chmod -R 755 /var/www/your_domain
```
```bash
    sudo nano /etc/nginx/sites-available/your_domain
```
```bash
    server {
    listen 80;
    server_name your_domain www.your_domain;
    root /home/ubuntu/your_file;
    index index.html index.htm;

    location / {
        try_files $uri $uri/ =404;
    }
    # ... other configurations ...
}
```
```bash
    sudo ln -s /etc/nginx/sites-available/your_domain /etc/nginx/sites-enabled/
```
```bash
    sudo nano /etc/nginx/nginx.conf
```

```bash
    sudo nginx -t
```
```bash
    sudo systemctl restart nginx
```

Resolve 404 error
```bash
    sudo find /home/ubuntu/roocabs-static -type f -exec chmod 644 {} \;
```
```bash
    sudo chmod -R 755 /home/ubuntu/your_file
```
Check Error Log
```bash
    sudo tail -n 50 /var/log/nginx/error.log
```
```bash
    sudo chown -R www-data:www-data /home/ubuntu/roocabs-static
```
```bash
    sudo nginx -t
```
```bash
    sudo systemctl restart nginx
```
