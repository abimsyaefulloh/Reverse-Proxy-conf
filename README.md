# Reverse-Proxy-conf
```bash
server {
    listen 80;
    server_name your_domain.com; # Replace with your domain or IP address

    location / {
        proxy_pass http://localhost:8080; # Replace with the address and port of your backend application
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```
