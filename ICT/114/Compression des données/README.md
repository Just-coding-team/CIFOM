## Quelques termes importants

Compression: encoder le fichier d'une nouvelle manière en sorte qu'ils prennent moins de place

## Général

### Fonctionnement

1. Compression
2. Décompression

![image](https://user-images.githubusercontent.com/73474137/158393217-29d2cef3-6f5c-4185-ad07-344a647189fa.png)

### Type de compression

1. Sans perte: une compression sans perte est une compression où nous perdons pas de données pendant le décompressage (7z, zip, rar)

2. Avec perte: une compression où les données peu importantes sont supprimées pour optimiser la compression (jpeg, mp3)

### Taux de compression 

![image](https://user-images.githubusercontent.com/73474137/158393943-57e22cd1-cfeb-409e-87cc-36c977588634.png)

### Les algorithmes de compression

#### RLE

AAAAAHHHHHHHHHHHHHH -> 5A14H

#### Huffman

HOURRA HOURRA HOURRRRA

![image](https://user-images.githubusercontent.com/73474137/158394643-ff3a01fd-5ad5-455c-b62f-e66af33ea846.png)
![image](https://user-images.githubusercontent.com/73474137/158394679-de11ad0d-ac62-4171-8f57-e6cf0e10c523.png)

#### LZ78

ta_tata_et_ton_tonton

![image](https://user-images.githubusercontent.com/73474137/158399977-1d3f54b1-9749-4d29-b190-7a547ad913eb.png)
![image](https://user-images.githubusercontent.com/73474137/158400026-a3ad701d-ca72-4a88-8635-f9858db0a233.png)

### Compression de vidéos

#### Compression par image

![image](https://user-images.githubusercontent.com/73474137/158834527-ce51e0e9-c62e-435e-b482-fe3d20870c08.png)

**Avantage :**
- Robuste (La perte d'une image n'influe pas la suite de la vidéo)


**Désavantage :**
- Faible taux de compression

#### Prédiction inter images

![image](https://user-images.githubusercontent.com/73474137/158835226-b2c5733e-35f9-4290-a612-9ddf55c46fb1.png)

**Avantage :**
- Compression importante pouvant aller de 50 à 80%


**Désavantage :**
- Moins robuste

### Compression audio

Le principe de compression audio sur la suppression des fréquances qui ne sont pas nécessaires

1. **Echantillonnage:** Prélèvement à des intervales régulières (Hz)
2. **Quantification:** Association d'une valeur unique pour chaque échantillons prélevé (bit)
3. **Signal numérique:** Récupération du code de chaque échantillons sous forme binaire 

![image](https://user-images.githubusercontent.com/73474137/158838599-8f28bae6-9515-4525-9912-62d8001c62e6.png)
