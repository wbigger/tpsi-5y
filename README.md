# tpsi-5y

Dopo aver fatto partire l'istanza EC2 di AWS, solo la prima volta eseguire i seguenti comandi:

```
sudo yum update
sudo yum install git
sudo amazon-liunux-extras install nginx1.12
```

Poi, in generale ogni volta che ci serve il nostro web server:
```
sudo /usr/sbin/nginx
```

Per accedere all'istanza dal browser, andare sulla console di aws, selezionare l'istanza, nel pannello in basso selezionare "Public DNS (IPv4)" e copiare la stringa nella barra del browser.

Scaricate il vostro progetto da GitHub e copiatelo nella cartella servita dal server:
```
cd
git clone https://github.com/nickname/startbootstrap-something
sudo cp -r startbootstrap-something/* /usr/share/nginx/html/
```



