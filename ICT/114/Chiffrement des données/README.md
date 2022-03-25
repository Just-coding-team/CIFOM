# Le chiffrement des données 

Tout d'abord il y a deux méthodes...

1. Le chiffrement ***Réversible***
2. Le chiffrement ***Non-réversible***

La première méthode est utilisé pour la transmisition des messages par example ou d'autre activité où le but final est de déchiffrer la donnée pour qu'un autre individu puisse la lire à l'aide d'une **clé**. 

La deuxième methode est plutôt utilisé pour le stockage de données où la donné sera comparé est ne doit pas être lisible, par example si nous stockons des mots de passes nous voulons ne pas pouvoir les lire

### Vocabulaire français 

Les mots crypter et decrypter sont des anglicismes, en français nous allons plutôt dire chiffrement et déchiffrement. 

La cryptographie serait alors "La science du chiffrement"

### Entropie

**L'entropie nous permet de mesurer la robustesse d'une clé (bits)**

#### Calculer l'entropie d'un mot de passe 

Si notre mot de passe est ```fM3d8DfL``` et nous supposons qu'il utilise majuscules, minuscules et chiffres nous sommes à *62* caractères qui nous donnes un nombre de 2^H = 62^8 possibilité (62 symboles, 8 caractères)

La formule pour calculer l'entropie (H):

![image](https://user-images.githubusercontent.com/73474137/160009897-4acbefaa-2f82-4384-a427-a54fb4e6a651.png)

### Chiffrement

***Réversible:*** Une méthode de cryptographie pour rendre incompréhensible le contenue à toute personnes ayant pas la clé de déchiffrement

***Non-réversible:*** C'set aussi appellé le **hachage** 

#### Diagrame

![image](https://user-images.githubusercontent.com/73474137/159997114-fa0908e9-79e7-4362-9282-eee2f948c0e9.png)

#### Réversible

Un diagrame montrant en gros la base du fonctionnement du chiffrement réversible

![image](https://user-images.githubusercontent.com/73474137/159999153-3fc208e2-b087-4c78-a2ec-5a8e0a4e30c2.png)

##### Chiffrement symétrique

Le chiffrement symétrique est basé sur le fait que nous utilisant la même clé

![image](https://user-images.githubusercontent.com/73474137/159999613-80ace1c0-c2be-42f5-8a55-c67b70a76089.png)

**Avantages:**

- Rapide
- Simple à mettre en oeuvre

**Inconvénient:**

- Il faut échanger la clé qui est la même pour chiffrer et déchiffrer les données

⚠ Cela crée le risque que la clé soit volé lors du transport qui présente un dangé

###### Le chiffre de César

Le principe de ce chiffrement est le décalage des lettres, quelques crans vers la droite ou la gauche

![image](https://user-images.githubusercontent.com/73474137/160001457-71281938-9e0d-4d08-b6f0-63dff8d89af8.png)

**Example:** ```OPERATION ANNULEE``` devient ```RSHUDWLRQ DQQXOHH```

###### Le chiffre de Vigenère

Un peu plus complexe que le chiffre de césar... Cela consiste à prendre une phrase par example ```J'ADORE ECOUTER LA RADIO TOUTE LA JOURNEE```, puis prendre une clé par example ```MUSIQUE``` pour par la suite le ramplacer de la manière suivante avec le tableau ci-dessous:
 
```
J'ADORE ECOUTER LA RADIO TOUTE LA JOURNEE
M USIQU EMUSIQU EM USIQU EMUSI QU EMUSIQU
```

Qui devient

```
V'UVWHY IOIMBUL PM LSLYI XAOLM BU NAOJVUY
```

***La table de Vigenère:***

![image](https://user-images.githubusercontent.com/73474137/160005335-7be08941-8bb3-497f-b9f8-6465c84be46a.png)

##### Le chiffrement asymétrique

Dans ce type de chiffrement réversible nous avons une clé pour chiffrer les données et une autre pour les déchiffrer. Nous nommons ces clés ***La clé publique*** la clé de chiffrement et ***La clé privé*** la clé de déchiffrement. On appelle également ***un certificat***, une paire de clés.

![image](https://user-images.githubusercontent.com/73474137/160010777-a73fd248-29df-43e9-9268-70726554fe7f.png)

***Paire de clés RSA:***

Une clé publique peut être distribué à qui nous voulons, et elle réssemble à quelle que chose comme ça 
```
FwwDQYJKoZIhvcNAQEBBQADSwAwSAJBAIfuRBXf32uNDxjlW889fu27Lks5Ulz3iio7F3Ry0peETVkx1pPm3ENbTx8AK8o+0graPDiCJVpikUoTaYF5GGsCAwEAAQ==
```

Une clé privé doit être secrète, et personne doit la connaître (elle sert à déchiffrer les données, elle réssemble à cela
```
MIIBVQIBADANBgkqhkiG9w0BAQEFAASCAT8wggE7AgEAAkEAh+5EFd/fa40PGOVbzz1+7bsuSzlSXPeKKjsXdHLSl4RNWTHWk+bcQ1tPHwAryj7SCto8OIIlWmKRShNpgXkYawIDAQABAkAaF55yJHsahgUz3jL1YPSQZbHJNsOcnNekq5sg+zl5Y+BmvDrIOy3yFwT01RvyxWX8a7lQjTh7z3yHL428auABAiEAvCN7RtQgoYYUkoigJppL0zbh2xWh0C67E0crOLJvNGsCIQC49fb/qdaL3k4AJtD8euPr0zPtoBkL+MfM/tXba/asAQIhAIUDGN8EjmVkJBtNWNyx7bXQcXGxI4vJ3h1NDbOyA4ktAiEAk+Yy1StE4OEpdBuV316RJIDlNC1h+d28PuLDtUp2nAECIHPL1W3iF9tJSkOKrxyiE9seGNxMm6RVAuE4GRTQoTWa
```

![image](https://user-images.githubusercontent.com/73474137/160011696-602269b0-e66e-4003-9b7f-08f5cd76e946.png)

⚠ Nous ne pouvons pas déchiffrer les données sans la clé privé

**Avantages:**

- Très sûr, car on utilise deux clés, une publique et une privée.
- Il n'y a pas d'échange de clé comme pour le chiffrement symétrique.

**Inconvénients:**

- Un peu plus difficile à mettre en œuvre que le symétrique.
- Plus lent que le symétrique.

***Echanges des clés publiques:***

1. Publié sa clé sur *un serveur de clés publiques*
2. La partager sur son site internet ou à ses correspondant mail

⚠ Nous pouvons faire certifier notre clé par quelqu'un pour montrer que cette personne nous fait confiance

Examples d'algorithmes asymétriques:

- RSA
- DSA
- Diffie-Hellman

###### Signatures numériques

Le but d'une signature numérique, est un mécanisme cryptographique qui premet d'assurer l'authentité de **l'autheur**

Nous parlons ici du chiffrement **asymétrique**. Cependant nous pouvons aussi utiliser le chiffrement **non-réversible**.

![image](https://user-images.githubusercontent.com/73474137/160019154-023241ac-0732-47ce-b8ee-4d77371c4595.png)

⚠ La signature numérique ne garantit pas la confidentialité mais uniquement l'authenticité de l'auteur

##### Le chiffrement hybride

La cryptographie hybride, fait appel au chiffrement symétrique et asymétrique. Il est utilisé par example dans le protocole HTTPS, ou le logiciel PGP.

***Le principe:***

On utilise le chiffrement asymétrique, qui est très long pour s'échanger les clés secrètes utilisées dans le chiffrement symétrique. Ensuite toutes les autres communications se feront avec le chiffrement symétrique qui lui est beaucoup plus rapide.

Pour optimiser la chose nous utilisons l'algorithme sécuriser pour passer les clés en toutes sécurité pour finalement utiliser l'algorithme rapid

Par exemple, le protocole HTTPS pour HTTP Secure est un protocole d'échange d'informations entre un navigateur web et un serveur, il faut qu'il soit rapide. C'est pourquoi on utilise le chiffrement hybride. Une fois la clé de chiffrement symétrique échangée par chiffrement asymétrique (clé publique et clé privée) le navigateur et le serveur peuvent communiquer de manière sûre et plus rapide que s'ils faisaient du chiffrement symétrique lors de chaque échange.

#### Non-réversible

Autrement appellé aussi le hashage, que l'on crypte pour ne plus le décrypter (On l'appelle aussi une empreinte)

A l'aide de l'algorithme md5 le texte ```Rendez-vous à 10:00 précise devant l'entrée.```nous donnerait ```a33570a5ec94f9daffa5ae154f781144```.

Ce qui est bien avec ces algorithme c'est que si nous changeons une lettre le resultat final ne sera plus du tout le même, par example:

```
Rendez-vous à 11:00 précise devant l'entrée.
```

Nous donnera 

```
ce4e2b9750cb4844cf21b57f9f07400e
```

Nous pouvons remarquer que les deux hash ne sont pas du tout les même

##### Utilité

Un hash peu être laissé comme une empreite dans un logiciel, qu'on pourrait comparer après l'installation et s'assurer que nous n'avions pas installé un autre logiciel

Il peut être aussi utiliser pour comparer et stocker des mots de passes dans la base de donnée

##### Quelques algorithmes de hashage

- MD5 et SHA1 (plus trop sûr)
- SHA3, SHA256, SHA512 
- BCrypt (Récent et très sûr)

### Les attaques

1. Attaque par dictionnaire ou "rainbow table"

Il s'agit du premier type d'attaque, la plus rapide. Nous utilisant une table avec des mots de passe volé pour s'introduire dans un environement. On l'appelle des ***tbales arc-en-ciel** ou ***rainbow table***.

![image](https://user-images.githubusercontent.com/73474137/160183071-6161a1db-c0b9-49ab-8f32-cd0e58c6969a.png)

2. Attaque par brute force

Nous essayons toutes les possibilites possible. **Aucun mot de passe ne peut résister à cette technique**, seulement les mots de passe plus complexe et long prendront plus de temps nécessaire.

### Le sel

Pour parvenir le rainbow tables attacs nous allons ajouter du sel dans l'enregistrement dans la base de données.

Par example si nous utilisant le nom utilisateur ```toto```, mot de passe ```Salut!123``` et le sel en tant que ```@°ç11M```, donc nous stockons le sous la forme ```totoSalut!123@°ç11M``` qui nous donne avec le chiffrement SHA1 ```c0f766ae737dd0e70ed184c60ea2eda8cd781a92```. Si ```lulu``` à le même mot de passe, elle n'aura pas le même hash à cause du nom ```010d1505821af044bad7d29cadeaaabe525c4d85```

### BCrypte

La méthode de hashage qu'on utilise aujourd'hui plutôt que SHA-x ou le MD5. BCrypte à l'avantage de générer différent hash pour le même mot de passe. Le principal avantage de Bcrypt c’est son extrême lenteur qui fait que le brute force devient extrêmement lent et donc inutilisable.

![image](https://user-images.githubusercontent.com/73474137/160185389-5d329958-7250-4f7c-8c4e-3e3faf232f87.png)

### Signature numérique en détails

![image](https://user-images.githubusercontent.com/73474137/160185570-066a41ea-93ad-42be-b3da-a5b021b83e0a.png)

Example avec PGP:

```
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512

Voici le compte IBAN pour le versement : CH63 0900 0000 2500 9779 8
-----BEGIN PGP SIGNATURE-----

iQFEBAEBCgAuJxxGYWJpYW4gSMOqY2hlIDxmYWJpYW4uaGVjaGVAZ21haWwuY29t
PgUCYc2wOQAKCRDFdIzJVQMixgKcB/9HQ9vC+2umrobGwBktSaRi8Xydp+vn8YQd
q3Z9+HQGd2pLAvQGfCpAMfvw0nWYipYBl61itHgsXFUPjthB5wSmeGz3tLpI+i7/
bkQ2BL9W+vncefMdtdBD3l8HIQ/kq2mXnv+42Rr31FyL0Ge/JcXXVEih4Hf2LMYw
A+7NRs85IQq+vxtJ0+/dgRdxmScP63k5LZPlTNg1n3xL3CSSATj6Cj3MJFr7FjWZ
PHjzRs+XASmdbYrHuAZRfZLdFBfvW3/ykxoCSqnwa64jgGE9OoAUUMZfO7Jf5Mpf
ZP0rb1vyd640uaGD5mLVezoK9dsA3Y6mVGmpLjQteKe/t5yBO8K5
=gsdw
-----END PGP SIGNATURE-----
```

On distingue les éléments suivants :

1. Le hachage utilisé pour créer l'empreinte.
2. Le message en clair.
3. Le chiffrement de l'empreinte.

### Certificat numérique

**Un certificat numérique**, ou appellé aussi une clé publique, pet être vu en tant qu'une carte d'identité numérique. Il est utilisé principalement pour **identifier et authentifier**, mais aussi pour le chiffrement.

Un bon example est le protocole **HTTPS**, qui a le transfert sécurisé de données. C'est la version améiloré du protocole HTTP avec le chiffrement **SSL** ou **TLS**

![image](https://user-images.githubusercontent.com/73474137/160186718-afd1a534-88af-4911-8095-39aa8fd51608.png)

En résumé, on utilise le protocole HTTPS pour sécuriser les données échangées entre le navigateur et le serveur pour éviter qu'un "hacker" intercepte ces données telles que votre numéro de carte de crédit, vos informations personnelles, etc. lorsqu'elles sont envoyées au serveur.
