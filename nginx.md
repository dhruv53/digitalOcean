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
6. Add a domain name(optional)
- Replace _ with domain name. <br/><code> server_name _</code> -> <code>server_name example.com</code>

7. Quit File using <code>wq</code>
