# Active Directory

Les avantages d'AD sont que la gestion est centralisée qui nous facilite beaucoup la tâche et les domaines nous offrent un processus d'ouverture de session.

### Arbre

Un arbre est une hiérarchie de domaine et de sous-domaines. Le premier dommaine s'appelle le domaine racine. Les domaines et ses sous-domaines partagent une base de nom commune.

### Forêt

Une forêt est un groupe dârbres qui ne forment pas un espace de nom de base commune. 

### Active Directory

Un des principaux avantages du réseau de type client-serveur, c'est la possibilité de centraliser la gestion des comptes-utilisateurs dans une base de données uniques est Active Directory (AD).

AD est une grande base de données dans laquelle seront répertoriés une grande partie des ressources informatiques du réseau. Ces ressources sont appelées Objets Active Directory: 

- Les comptes utilisateurs
- Les groupes d'utilisateurs 
- Les ordinateurs
- Les serveurs
- Les imprimantes

Les serveurs ayant installé AD se nomme "contrôleur de domaine". Ci-dessous, vous avez une structure AD: 

![image](https://user-images.githubusercontent.com/73474137/173202067-ea204a9c-97c3-42f5-8def-35a2b3bc148f.png)

## Réponses aux questions

1. Que contient un service d'annuaire ?

Un annulaire stocke un ensemble d'informations sur des objets ayant un lien les uns avec les autres

2. Sous quelle forme est constitule AD ?

C'est un fichier

3. A qui sert un service d'annuaire ?

Un outils administrateur et pour l'utilisateur final

4. Qu'est-ce qu'un contrôleur de domaine ?

Un logiciel contrôlant les réponses pour limiter le DDOS... Un ordinateur sur lequel nous avons AD qui gère l'accès des utilisateurs réseau

5. Quel est l'avantage d'avoir plusieurs contrôleurs de domaine par domaine ?

S'il y en a un qui tombe en panne l'autre peut prendre sa place.

6. Citez des objets que peut contenir un domaine ?

Utilisateurs, groupes, imprimantes

7. Un administrateur d'un domaine donné, peut-il gérer un autre domaine ?

Il peut gérer tout les sous-domaines, mais pas d'autre domaine

8. Qu'est-ce qu'une UO ?

Des conteneurs administratifs, servant à administrer le serveur

9. Qu'est qu'un "Arbre" ?

C'est un domaines avec ses sous-domaines

10. Citez les fonctions des contrôleurs de domaine.

Ils stockent une copie complète d'AD, ils répliquent les objects d'un domaine vetrs les autres contrôleur et ils gèrent les aspects de l'interaction des utilisateur avec le domaine
