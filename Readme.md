# Multiple Apps in the same server

This Docker-compose.yml join multiple apps in the same Server:

* Proxy
* Mariadb
* php
* phpmyadmin
* wordpress x2
* Laravel
* Vuejs ( Producction /dist folder)
* Html files

## Run

``` 
mkdir Server
cd Server
git clone https://github.com/p3drojimenez/docker-multiple-apps.git .

docker-compose up -d

 ```


 ## Vuejs App

 You must to create your app in your folder, usint vue-cli (https://cli.vuejs.org/)

 ``
 cd Server
 cd vue
 vue create myapp
 
```

### Developent mode:

`` cd myapp & npm run serve ``

### Produccion mode:

#### 1: Update docker-compose.yml

```
volumes:
      - ./vue/myapp/dist:/usr/share/nginx/html/
```
#### 2: Run Build Vue App


```
npm run build
```

## Todo

 [] Fix multi Laravel apps
 [] Add Reactjs App
