# TPSI - 5 anno

# Avviare una macchina su AWS
Fare il login su [AWS Educate](https://www.awseducate.com/signin/SiteLogin).

Accedere alla propria classe e quindi alla console AWS.

Sulla console AWS, selezionare in alto Servizi->Computer->EC2.

Nel menù a sinistra, andare su Instances->Instances.

## Primo avvio
Premere su Launch Instance, lasciare la selezione di default "Amazon Linux 2 AMI (HVM), SSD Volume Type" a 64-bit (x86), premere su Select, lasciare t2.micro, premere Review and Launch.

Aggiungere al security group la porta HTTP.

Avviare l'istanza.

Dalla lista delle istanze, selezionare Connect e seguire le istruzioni.



### Prima configurazione
Una volta fatto l'accesso l'istanza EC2 di AWS, solo la prima volta eseguire i seguenti comandi:

```
sudo yum update
sudo yum install git
sudo amazon-liunux-extras install nginx1.12
```


## Avvii successivi al primo
Dalla console AWS EC2, selezionare l'istanza e premere il bottone in alto Actions->Instance state->Start.
Connettersi all'istanza.

Avviare il web server:
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



