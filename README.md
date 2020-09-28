# Demo mixed loadbalancing

Dimostrazione di microservizi in bilanciamento interno.

Docker compose viene usato per creare:

- **webserver internal**: raggiungibile solo da service
- **webserver external**: in ascolto in SSL e raggiungibile solo da rotta
- **reverse proxy**: (nginx) verso __webserver external__ per avere un service in plain http
- **haproxy**: bilancia in modalità active/backup verso internal/external come services.

