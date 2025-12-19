# Servidor FTP corporatiu amb Docker i vsftpd

Aquest projecte desplega un servidor FTP utilitzant Docker i vsftpd. El servei permet la gestió d’usuaris autenticats, accés anònim controlat i suporta els modes de connexió actiu i passiu.

## Requisits previs
- Docker Desktop instal·lat
- Docker Compose
- PowerShell a Windows
- Connexió a Internet

## Estructura del projecte
```text
ftp-project/
├── config/
│   └── vsftpd.conf
├── data/
│   ├── public/
│   └── users/
├── logs/
├── Dockerfile
└── docker-compose.yml
```

## Desplegament del servei

cd ftp-project  
Accedeix al directori del projecte.

docker-compose build  
Construeix la imatge Docker amb el servidor FTP.

docker-compose up -d  
Inicia el servei FTP en segon pla.

docker ps  
Comprova que el contenidor està en execució i actiu.

## Accés al servidor FTP

Es recomana utilitzar un client FTP dedicat com FileZilla.

Dades de connexió:
- Host: 127.0.0.1
- Port: 21
- Usuari: empleat1
- Contrasenya: Emp2024!

## Aturar el servei

docker-compose down  
Atura i elimina el contenidor FTP.

## Notes finals
- L’accés anònim només permet la descàrrega de fitxers.
- El mode passiu és el més recomanat per evitar problemes de connexió.
- Per a entorns reals, és millor utilitzar protocols més segurs com FTPS o SFTP.
