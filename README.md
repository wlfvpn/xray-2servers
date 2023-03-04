# xray-2servers
Connect two servers using xray-VLESS-XTLS-VISION-with-NGINX-FALLBACK to bypass filtering. This is an alternative approach to port forwarding.

### Definitions
internal: server inside IRAN
external: server outside IRAN

### STEPS (Do for internal and external folder)
1. install docker, docker-compsoe, nginx
2. Get your wildcart certificate and place it in `cert/example.com/`
3. Modify the `config.json` and point your certificates.
4. Go to the website you wanna copy and save it as `index.html` and copy files into `/var/www/html/`
5. `cp nginx.conf /etc/nginx/conf.d/nginx.conf && rm /etc/nginx/conf.d/default.conf`
9. `rm /dev/shm/h* && service nginx restart`

### LINKS:

```
vless://e547d090-e309-4067-91d6-90e313701692@int.example.com:443?encryption=none&flow=xtls-rprx-vision&security=tls&sni=int.example.com&alpn=h2&type=tcp&headerType=none#vless-xtls-vison-1
vless://7e0a39a8-17e1-41c5-ad68-1e7e564866ca@int.example.com:443?encryption=none&flow=xtls-rprx-vision&security=tls&sni=int.example.com&alpn=h2&type=tcp&headerType=none#vless-xtls-vison-2`
 ```

