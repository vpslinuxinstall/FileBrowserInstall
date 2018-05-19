# Manually Install

## 1.Manually Install

### 1.1 Edit [filebrowser.service](https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser.service)

```bash
nano /lib/systemd/system/filebrowser.service
```

```bash
Description=Filebrowser Service  
After=network.target  
Wants=network.target  

[Service]  
Type=simple  
PIDFile=/var/run/filebrowser.pid  
ExecStart=/usr/bin/filebrowser -c /etc/filebrowser/filebrowser.json  
Restart=on-failure  

[Install]  
WantedBy=multi-user.target
```

### 1.2 Edit [filebrowser.json](https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser.json)

```bash
nano /etc/filebrowser/filebrowser.json
```

```bash
{  
  "port": 8300,  
  "noAuth": false,  
  "baseURL": "/admin",  
  "address": "0.0.0.0",  
  "reCaptchaKey": "",  
  "reCaptchaSecret": "",  
  "database": "/etc/filebrowser/database.db",  
  "log": "stdout",  
  "plugin": "",  
  "scope": "/",  
  "allowCommands": true,  
  "allowEdit": true,    
  "allowNew": true,  
  "commands": [  
    "git",  
    "svn"  
  ]  
}
```

### 1.3 Download [filebrowser](https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser) to /usr/bin/

```bash
cd /usr
cd bin
wget https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser
systemctl enable filebrowser
systemctl start filebrowser
```

