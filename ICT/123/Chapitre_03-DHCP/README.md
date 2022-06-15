Le protocole DHCP (Dynamic Host Configuration Protocol) est un protocole permettant de centraliser la configuration des machines du réseau au niveau de l'adressage IP.

Ce service permet de fournir aux stations clientes tous les paramètres TCP/IP, comme :

- l'adresse IP
- le masque de sous-réseau
- la passerelle par défault
- l'adresse des serveurs de nom (DNS)
- le suffixe de domaine

C'est la machine qui centralise la gestion des adresses IP. Dans le monde Microsoft, un serveur DHCP est une machine avec un système d'exploitation de Windows serveur avec le rôle de serveur DHCP configuré.

Les avantages du DHCP:

- limitation les conflits d'adresses IP
- La gestion des adresses est centralisée, donc plus simple
- Grâce au bail, il est possible d'avoir plus de clients potentiels que d'adresses dans le réseau (attention au pic!)
- Pour les périphériques mobles, l'adresse sera assignée automatiquement au bon sous.réseau... (tablettes, smartphones, portables, ...)

La demande pour obtenir une adresse par un client DHCP s'effectue en plusieurs phases.

- La station cliente émet un broadcast MAC (FF:FF:FF:FF:FF:FF) sur le réseau
- L'ensemble des serveurs DHCP va recevoir la demande et envoyer une proposition au client 
- La première proposition reçue va être choisie par le client 
- Le client va diffuser un message de sélection à tous les serveurs
- Le serveur concerné va envoyer au client les paramètres et une confirmation de bail

Le bail est la durée définie par l'administateur du serveur DHCP (J, H, M). Il est possible, depuis la station cliente, de forcer la libération ou il renouvellement du (ipconfig /release et ipconfig /renew)

Par défault un client DHCP essaie de renouveler son bail à la moitié et au 87.5 du temps alloué. En cas d'échec, le client DHCP va émettre de nouveau une demande d'obtention d'adresse aux serveurs DHCP.

L'étendue configurée est nécessaire pour un serveur pour pouvoir distribuer des adresses. Une étendue est un pool d'adresses d'élimité par la première et dernière adresse $ assignier. 

Elle contient aussi:

- le masque de sous-réseau
- l'adresse de la passerelle (gateway)
- la durée du bail 
- l'adresse du serveur DNS 
- l'adresse du serveur Wins 
- d'éventuelles adresses à exclure 

![image](https://user-images.githubusercontent.com/73474137/173922409-79ce3303-37e8-431c-8e0b-7b758ab59fab.png)

La pile IP d'un client Windows doit être configurée ainsi pour être client DHCP.

![image](https://user-images.githubusercontent.com/73474137/173922700-81ae5fc3-01f0-4f4e-81f9-fa5d1d359234.png)

![image](https://user-images.githubusercontent.com/73474137/173922720-69112dc8-989f-4d87-af86-0cf195e285b9.png)

![image](https://user-images.githubusercontent.com/73474137/173922843-4be13591-e5c6-4868-993a-06deeb45c904.png)

