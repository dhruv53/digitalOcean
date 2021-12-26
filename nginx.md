# Setting up nginx

### Configure nginx

1. Navigate to root directory <code>cd /</code><br/>
2. Use <code>ls</code> to check folder etc
3. Navigate to nginx sites available config
```javascript
cd /etc/nginx/sites-available/
```
4. List available sites 
```javacript
ls
```
 5. Edit the available site(default in case of single website)
 To Edit File: i
 
 ```javascript
 vi default
 ```
6. Configuration
- Add a domain name(optional)
Replace _ with domain name. <br/><code> server_name _</code> -> <code>server_name example.com</code>
- Proxy to redirect users from ip address to http://localhost:9000<br/>
<b>Comment location code block</b> and add the below code.
```javascript
location / {
        proxy_pass http://localhost:9000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
```

7. Quit vi using<br/>
- Press <code>Esc</code><br/>
- Press <code>:</code>(colon)<br/>
To exit without saving anything
- Enter <code>q!</code><br/>
To exit while saving changes
- Enter <code>wq</code>

8. Check the saved file syntax
```javascript
nginx -t
```
9. Reload nginx to update proxy settings
```javascript
systemctl reload nginx
```
10. Now navigate to the project folder & run server to test proxy config
```javascript
cd ~
cd projectName
node server.js
```
11. Visit the ip address without port number to check if nginx is running the website or not.
