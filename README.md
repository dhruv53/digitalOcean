# Local Project

### Install express server on project
```javascript
npm install —save express
```
### Create a server.js in root directory and copy the code below
(outside src or public folder)
```javascript
const express = require('express'); 
const path = require('path'); 
const app = express(); 
app.use(express.static(path.join(__dirname, 'build'))); 
app.get(‘/*’, function (req, res) { 
res.sendFile(path.join(__dirname, 'build', 'index.html')); 
}); 
app.listen(9000);
```
### Create a production build of the project
```javascript
npm run build
```
### To run node server
```javascript
node server.js
```
### Test the app by visiting localhost:9000

### Push the code to github
- Initialise git project using <code>git init</code>
- Adding remote origin using <code> git remote add origin url</code>
- Stage everything using <code>git add .</code>
- Create a commit using <code>git commit -m "Commit Name"</code>
- Push the code using <code>git push -u origin main</code>
# Server Side

### Login to the server using terminal 
```javascript
ssh root@ip_address
```

### To find the username
```javascript
whoami
```
### To update system
```javascript
apt-get update && apt-get upgrade
```
### Install nvm(node package manager)
```javascript
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
```javascript
source ~/.profile
```
### List all available node versions 
```javascript
nvm ls-remote
```
### Install specific node version
```javascript
nvm install v12
```
### Check node version
```javascript
node —version
```
### Clone git project
```javascript
git clone url
npm install --save
```
### To run server
```javascript
node server.js	
```
### To exit running node server
```javascript
ctrl+c
```
### Install nginx
```javascript
apt-get install nginx
```


