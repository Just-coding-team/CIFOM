# Les états

Préparation de la base de donnée pour l'impression.

> Création utilisation de l'**Assistant** est conseillé

### Ajout de champs existant 

Dans le cas où nous avons oublié ou supprimé un champ sans faire exprès nous avons le champ ***Ajouter des champs existants*** pour ajouter un champ

![image](https://user-images.githubusercontent.com/73474137/158769632-74746bc9-88a8-4ea6-a56c-a3df928effa8.png)

### Trier les données

![image](https://user-images.githubusercontent.com/73474137/158789232-7ddfbffa-69ec-4434-81df-5a979f9fa9b6.png)

A partir de la nous pouvons ajouter des tris et des regroupement

*Regroupement:* Servent à mieux organiser notre état en sorte de section qui sont plus facilement aménagable (possible de rencontrer des petits problèmes avec des sous-regroupement

*Tris:* Servent à trier dans un ordre donné nos compartiment des états

***Image d'example:***

![image](https://user-images.githubusercontent.com/73474137/158789303-a3fef75b-f432-4062-947b-faa88e45782c.png)

### Les requêtes parametrées 

Pour les requêtes parametrées nous inserons une variable qui n'existe pas dans le ou dont le nom est la question dans la partie ***Critères*** de la donnée voulu. Example:

![image](https://user-images.githubusercontent.com/73474137/158791275-a41690d4-1367-45d8-a9db-553cbfd233f9.png)

![image](https://user-images.githubusercontent.com/73474137/158791496-9ac5ea82-01a4-4765-bedc-dd0fe51c34a5.png)

### Gestion des images

Pour les images il y a une preconfiguration faite, dans l'onglet **Format** des propriétées nous parametrons le *Type d'image* en *Attaché* et *l'Image* en *Aucun*. Pour finir nous devons spécifier la source dans **Données**, en mettant ***[CurrentProject].[Path] & "\Dossier\" & [Nom_de_image]***

### Macro

> Une macro a pour objectif d'automatiser des actions ou de rationaliser les actions dans un application.

#### Création d'une macro

Tout d'abord nous cliquons sur l'icon ci-dessous 

![image](https://user-images.githubusercontent.com/73474137/158792676-350cf2ec-7a9b-43c7-a5cf-7e322a82fd2c.png)

Pour ensuite ajouter des arguments. ***Attention le formulaire doit être ouvert pour la condition where***

![image](https://user-images.githubusercontent.com/73474137/158792935-8bf91569-89f6-4488-857c-84b521f9a9a9.png)

Dans la condition **Where** nous comparons si ***Val1*** de l'état est [operateur] à ***Val2*** du formulaire qui l'active, où dans notre cas
- Val1: *[IDEleve]*
- Val2: *[Formulaires]![frmEleve]![IDEleve]*
