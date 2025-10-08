# ProjetEmailM1
Projet Interopérabilité | M1

Introduction

Le courrier électronique (e-mail) est un cas d’école de l’interopérabilité puisqu’il permet à des
utilisateurs utilisant une grande variété de matériels de communiquer.
Il est basé essentiellement sur 2 types de protocoles :

- Le premier permet de transférer des courriers électroniques d’une machine à une autre
machine. Il s’agit du premier protocole utilisé pour le mail : SMTP (Simple Mail Transfer
Protocol) https://datatracker.ietf.org/doc/html/rfc5321 .
- Le second permet de consulter des courriers électroniques à distance. Il s’agit de POP3
(Post Office Protocol) https://datatracker.ietf.org/doc/html/rfc1081 et de IMAP (Internet
Mail Access Protocol) https://datatracker.ietf.org/doc/html/rfc3501 .
Dans le cadre de ce projet on vous propose de créer un serveur capable de parler le protocole
SMTP et le protocole POP ou IMAP.
Côté client, on pourra utiliser un client générique comme telnet ou un client standard comme
Thunderbird (à condition de gérer suffisamment de commandes du protocole considéré).
Travail demandé

1) Version 1 : SMTP simple
Dans cette première version, on ne vous demande que de gérer les commandes minimales de
SMTP : MAIL, RCPT et DATA. Le courrier électronique envoyé par le client sera stocké dans
un fichier (boîte mail) dont le nom correspondra au paramètre de la commande RCPT.

3) Version 2 : Gestion des commandes HELO et/ou EHLO
Maintenant, on souhaite pouvoir gérer la procédure permettant d’identifier la version du
protocole parlée par le serveur : HELO pour la version basique du protocole ou EHLO pour la
version étendue. Étant donné que la gestion complète du protocole est hors périmètre de ce
projet, il conviendra d’indiquer une réponse 502 Command not implemented lors de la
réception de EHLO et ensuite de répondre 250 Ok lors du HELO suivant. Une fois cette version
terminée votre serveur devrait pouvoir communiquer avec des clients Mail standards comme
Thunderbird.

4) Version 3 : ajout de POP3
On veut désormais que le serveur permette la consultation à distance des courriers stockés dans
les fichiers (boîtes mail) en suivant le protocole POP3 (ou optionnellement le protocole IMAP).
Il ne s’agit pas ici d’implémenter la totalité du protocole mais de se concentrer sur la base.
Pour POP3, notamment, il nous faudra gérer les commandes QUIT, STAT, LIST et RETR.

5) Version 4 : Options
Dans cette version finale on pourra implémenter d’autres commandes de SMTP, POP3 ou
IMAP. On pourra, par exemple, mettre en place une authentification.
