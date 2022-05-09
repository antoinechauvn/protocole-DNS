# protocole-DNS
Approfondissement du protocole DNS

### Qu'est-ce que le protocole DNS?
```
Le protocole et le système DNS permet de résoudre des noms en adresses IP.
DNS est une sorte de service mondial de correspondance entre des noms et des adresses IP. DNS utilise principalement le port UDP 53.
Plus précisément, DNS est un système d’interrogation de registre mondial.
```

## Principe de fonctionnement
### La résolution de noms
La résolution de nom fait généralement référence au Domain Name System (DNS), service Internet qui associe des noms d’hôtes à leurs adresses IP;

La résolution de noms sur les réseaux peut aussi se faire grâce aux technologies suivantes :
* WINS (Windows Internet Naming Service) pour les clients utilisant les noms NetBIOS. Samba peut aussi agir comme serveur WINS,
* NIS Protocole permettant la centralisation d’information sur un réseau Unix. Notamment les noms d’hôtes (/etc/hosts) et les comptes utilisateurs (/etc/passwd).

### Résolution locale
Le fichier `hosts` est un fichier utilisé par le système d’exploitation d’un ordinateur lors de l’accès à Internet. Son rôle est d’associer des noms d’hôtes à des adresses IP.<br>
Lors de l’accès à une ressource réseau par nom de domaine, ce fichier est consulté avant l’accès au serveur DNS et permet au système de connaître l’adresse IP associée au nom de domaine sans avoir recours à une requête DNS.<br>
Les modifications sont prises en compte directement. Il est présent dans la plupart des systèmes d’exploitation.

### Enregistrements DNS
La bases de données d’une zone (un domaine) peut comporter certains types d’enregistrements DNS comme par exemple :

A record ou address record qui fait correspondre un nom d’hôte à une adresse IPv4 de 32 bits distribués sur quatre octets ex: 123.234.1.2 ;
AAAA record ou IPv6 address record qui fait correspondre un nom d’hôte à une adresse IPv6 de 128 bits distribués sur seize octets ;
CNAME record ou canonical name record qui permet de faire d’un domaine un alias vers un autre. Cet alias hérite de tous les sous-domaines de l’original ;
MX record ou mail exchange record qui définit les serveurs de courriel pour ce domaine ;
PTR record ou pointer record qui associe une adresse IP à un enregistrement de nom de domaine, aussi dit “reverse” puisqu’il fait exactement le contraire du A record ;
NS record ou name server record qui définit les serveurs DNS de ce domaine ;
SOA record ou Start Of Authority record qui donne les informations générales de la zone : serveur principal, courriel de contact, différentes durées dont celle d’expiration, numéro de série de la zone ;
SRV record qui généralise la notion de MX record, mais qui propose aussi des fonctionnalités avancées comme le taux de répartition de charge pour un service donné, standardisé dans la RFC 2782.
