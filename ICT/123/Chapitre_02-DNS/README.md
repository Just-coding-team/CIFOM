# DNS

Le DNS est un ensemble des communications informatiques se faisant avec le protocole TCP/IP et les adresses IP. Communiquer avec des machines avec les adresses IP n'est pas pratique, c'est la raison pour laquelle nous avons créé des DNS qui transform des noms en IP et vice-versa.

Un nom DNS entièrement qualifié est appelé FQDN (full qualified domain name)

![image](https://user-images.githubusercontent.com/73474137/173857016-f6b9f863-009e-4827-94a6-c4b533014463.png)

Le domaine de premier niveau est appelé TLD (top level domain)

![image](https://user-images.githubusercontent.com/73474137/173857434-7319e79f-d850-46c5-899d-5a2619b17b32.png)

Les serveurs root répertorient les serveurs DNS de chaque TLD. Les serveurs DNS de chaque TLD répertorient les serveurs DNS des domaines inscrits sous leur TLD. Les serveurs DNS des domaines répertorient l'ensembles des machines du domaine.

![image](https://user-images.githubusercontent.com/73474137/173857605-80cbec80-a77f-48a6-a5dd-299e9278074a.png)

![image](https://user-images.githubusercontent.com/73474137/173858228-cd783266-aee3-4dda-a1c7-ae52ba3771de.png)

Les résolutions DNS effectuées sont stockées en cache à 2 endroits. 

- Dans le cache du serveur DNS 
- Dans le cache de l'ordinateur client 

Par conséquent, l'ordre de recherche lors d'une résolution est le suivant:

1. cache du client 
2. zones hébergées sur le serveur DNS local
3. Cache du serveur DNS local
4. Résolution par l'arborescence DNS

Le ser veur DNS est la machine sur laquelle tourne le service DNS. Il héberge une ou plusieurs zones DNS. Une zone DNS contient l'ensemble relations "noms de machines" <=> "adresse IP" d'une domaine.

Une zone de recherche directe permet de trouver l'IP en fonction du nom de la machine, et une zone de recherche inverse permet de trouver un nom de machine en fonction de l'adresse IP. Il y aura un ou plusiquers serveurs DNS par domaine.

**Choissisez la Zone principale pendant la création d'une nouvelle zone**

![image](https://user-images.githubusercontent.com/73474137/173867611-7b29288e-b5af-4068-9482-9964a6586518.png)

![image](https://user-images.githubusercontent.com/73474137/173867759-b0830ffc-8fbe-46ce-aec5-def4c799e091.png)

![image](https://user-images.githubusercontent.com/73474137/173867818-cba1aad2-f5b8-4da5-84fa-4e63b133cd9b.png)

![image](https://user-images.githubusercontent.com/73474137/173867872-3974756c-528c-439a-8048-aeafdd0ce97d.png)

![image](https://user-images.githubusercontent.com/73474137/173868009-2fce17f0-dc5d-437f-83a0-fe12f8147f8e.png)

![image](https://user-images.githubusercontent.com/73474137/173868078-db9f5d1a-5dbb-4455-9aa3-16ecefd1ec06.png)
