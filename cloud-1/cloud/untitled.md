# Manually Install

## 2.Manually Install

### 2.1 Edit [filebrowser.service](https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser.service)

```bash
nano /lib/systemd/system/filebrowser.service
```

```bash
[Unit] 
Description=filebrowser 

[Service] 
User=root 
ExecStart=/usr/bin/filebrowser --port 8090 
Restart=on-abort 

[Install] 
WantedBy=multi-user.target
```

### 2.2 Download [filebrowser](https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser) to /usr/bin/

```bash
cd /usr
cd bin
wget https://github.com/vpslinuxinstall/Filebrowser/blob/master/filebrowser
systemctl enable filebrowser
systemctl start filebrowser
```

## 

