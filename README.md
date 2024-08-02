
# Classification des Feuilles de Plantes avec ResNet 🌱

## Présentation du Projet 📋

Ce projet vise à classifier les images des feuilles de plantes, en particulier celles de pommes de terre, à l'aide d'un modèle de deep learning basé sur l'architecture ResNet. Le modèle est conçu pour être robuste et efficace, utilisant des blocs de convolution résiduels pour capturer des caractéristiques complexes dans les images.

## Table des Matières 📑

- [Présentation du Projet](#présentation-du-projet-📋)
- [Installation](#installation-🛠️)
- [Prétraitement des Données](#prétraitement-des-données-🖼️)
- [Architecture du Modèle](#architecture-du-modèle-🏗️)
- [Entraînement](#entraînement-🏋️)
- [Résultats](#résultats-📊)
- [Contributeurs](#contributeurs-🤝)

## Installation 🛠️

1. **Cloner le Dépôt** :

   ```bash
   git clone https://github.com/username/plant-leaf-classification.git
   cd plant-leaf-classification
   ```
2. **Installer les Dépendances** :
   Assurez-vous d'avoir Python installé (version 3.7 ou plus récente). Ensuite, installez les packages requis :

   ```bash
   pip install -r requirements.txt
   ```
3. **Structure des Répertoires** :
   Assurez-vous que votre structure de répertoires pour les images est la suivante :

   ```
   /Data
   ├── TrainData
   │   ├── Classe1
   │   ├── Classe2
   │   └── ...
   └── TestData
       ├── Classe1
       ├── Classe2
       └── ...
   ```

## Prétraitement des Données 🖼️

- **Chargement des Images** :
  Le script utilise `os.walk` pour parcourir le répertoire du dataset, en chargeant les images de chaque sous-dossier correspondant à une classe. Les images sont redimensionnées à 64x64 pixels pour assurer l'uniformité.
- **Normalisation** :
  Les images sont normalisées pour avoir une moyenne de 0 et un écart-type de 1, ce qui stabilise le processus d'apprentissage.
- **Visualisation** :
  Utilisez la fonction `plot_images` pour visualiser des exemples d'images du dataset.

## Architecture du Modèle 🏗️

L'architecture du modèle repose sur ResNet, avec les éléments suivants :

- **Blocs ResNet** : Ces blocs permettent au modèle de s'entraîner plus efficacement en permettant le passage d'informations entre les couches via des connexions résiduelles.
- **Pooling Global** : Le pooling global réduit chaque carte de caractéristiques à une seule valeur, ce qui aide à prévenir le surapprentissage et à réduire le nombre de paramètres.

Le modèle est compilé avec l'optimiseur Adam et la fonction de perte `categorical_crossentropy`, optimisée pour une classification multi-classes.

## Entraînement 🏋️

Le modèle est entraîné pendant 100 époques avec une taille de batch de 64 :

- **Données d'Entraînement** : Les images prétraitées et normalisées sont utilisées pour l'entraînement.
- **Sauvegarde du Modèle** : Une fois l'entraînement terminé, le modèle est sauvegardé sous le nom `ResNet_model_groupe_2.h5`.

Pour entraîner le modèle, exécutez simplement le script :

```bash
python train_model.py
```

## Résultats 📊

Le modèle est évalué en fonction de l'accuracy, avec des performances mesurées sur plusieurs essais :

- Les résultats montrent une précision moyenne de **84,90%** sur 10 tests.

## Contributeurs 🤝

Ce projet a été développé par :

- **ISSA IBRAHIM Moubarak**
- **Abdourahamen Bachir**

---

Cet exemple de README fournit des instructions claires pour comprendre, installer, et exécuter le code. Il peut être ajusté en fonction des spécificités du projet ou de la structure de votre code

Voici un exemple de README pour le code que vous avez fourni :

---

# Classification des Feuilles de Plantes avec ResNet 🌱

## Présentation du Projet 📋

Ce projet vise à classifier les images des feuilles de plantes, en particulier celles de pommes de terre, à l'aide d'un modèle de deep learning basé sur l'architecture ResNet. Le modèle est conçu pour être robuste et efficace, utilisant des blocs de convolution résiduels pour capturer des caractéristiques complexes dans les images.

## Table des Matières 📑

- [Présentation du Projet](#présentation-du-projet-📋)
- [Installation](#installation-🛠️)
- [Prétraitement des Données](#prétraitement-des-données-🖼️)
- [Architecture du Modèle](#architecture-du-modèle-🏗️)
- [Entraînement](#entraînement-🏋️)
- [Résultats](#résultats-📊)
- [Contributeurs](#contributeurs-🤝)

## Installation 🛠️

1. **Cloner le Dépôt** :

   ```bash
   git clone https://github.com/username/plant-leaf-classification.git
   cd plant-leaf-classification
   ```
2. **Installer les Dépendances** :
   Assurez-vous d'avoir Python installé (version 3.7 ou plus récente). Ensuite, installez les packages requis :

   ```bash
   pip install -r requirements.txt
   ```
3. **Structure des Répertoires** :
   Assurez-vous que votre structure de répertoires pour les images est la suivante :

   ```
   /Data
   ├── TrainData
   │   ├── Classe1
   │   ├── Classe2
   │   └── ...
   └── TestData
       ├── Classe1
       ├── Classe2
       └── ...
   ```

## Prétraitement des Données 🖼️

- **Chargement des Images** :
  Le script utilise `os.walk` pour parcourir le répertoire du dataset, en chargeant les images de chaque sous-dossier correspondant à une classe. Les images sont redimensionnées à 64x64 pixels pour assurer l'uniformité.
- **Normalisation** :
  Les images sont normalisées pour avoir une moyenne de 0 et un écart-type de 1, ce qui stabilise le processus d'apprentissage.
- **Visualisation** :
  Utilisez la fonction `plot_images` pour visualiser des exemples d'images du dataset.

## Architecture du Modèle 🏗️

L'architecture du modèle repose sur ResNet, avec les éléments suivants :

- **Blocs ResNet** : Ces blocs permettent au modèle de s'entraîner plus efficacement en permettant le passage d'informations entre les couches via des connexions résiduelles.
- **Pooling Global** : Le pooling global réduit chaque carte de caractéristiques à une seule valeur, ce qui aide à prévenir le surapprentissage et à réduire le nombre de paramètres.

Le modèle est compilé avec l'optimiseur Adam et la fonction de perte `categorical_crossentropy`, optimisée pour une classification multi-classes.

## Entraînement 🏋️

Le modèle est entraîné pendant 100 époques avec une taille de batch de 64 :

- **Données d'Entraînement** : Les images prétraitées et normalisées sont utilisées pour l'entraînement.
- **Sauvegarde du Modèle** : Une fois l'entraînement terminé, le modèle est sauvegardé sous le nom `ResNet_model_groupe_2.h5`.

Pour entraîner le modèle, exécutez simplement le script :

```bash
python train_model.py
```

## Résultats 📊

Le modèle est évalué en fonction de l'accuracy, avec des performances mesurées sur plusieurs essais :

- Les résultats montrent une précision moyenne de **84,90%** sur 10 tests.

## Contributeurs 🤝

Ce projet a été développé par :

- **ISSA IBRAHIM Moubarak**
- **Abdourahamen Bachir**

---

Cet exemple de README fournit des instructions claires pour comprendre, installer, et exécuter le code. Il peut être ajusté en fonction des spécificités du projet ou de la structure de votre code

Voici un exemple de README pour le code que vous avez fourni :

---

# Classification des Feuilles de Plantes avec ResNet 🌱

## Présentation du Projet 📋

Ce projet vise à classifier les images des feuilles de plantes, en particulier celles de pommes de terre, à l'aide d'un modèle de deep learning basé sur l'architecture ResNet. Le modèle est conçu pour être robuste et efficace, utilisant des blocs de convolution résiduels pour capturer des caractéristiques complexes dans les images.

## Table des Matières 📑

- [Présentation du Projet](#présentation-du-projet-📋)
- [Installation](#installation-🛠️)
- [Prétraitement des Données](#prétraitement-des-données-🖼️)
- [Architecture du Modèle](#architecture-du-modèle-🏗️)
- [Entraînement](#entraînement-🏋️)
- [Résultats](#résultats-📊)
- [Contributeurs](#contributeurs-🤝)

## Installation 🛠️

1. **Cloner le Dépôt** :

   ```bash
   git clone https://github.com/username/plant-leaf-classification.git
   cd plant-leaf-classification
   ```
2. **Installer les Dépendances** :
   Assurez-vous d'avoir Python installé (version 3.7 ou plus récente). Ensuite, installez les packages requis :

   ```bash
   pip install -r requirements.txt
   ```
3. **Structure des Répertoires** :
   Assurez-vous que votre structure de répertoires pour les images est la suivante :

   ```
   /Data
   ├── TrainData
   │   ├── Classe1
   │   ├── Classe2
   │   └── ...
   └── TestData
       ├── Classe1
       ├── Classe2
       └── ...
   ```

## Prétraitement des Données 🖼️

- **Chargement des Images** :
  Le script utilise `os.walk` pour parcourir le répertoire du dataset, en chargeant les images de chaque sous-dossier correspondant à une classe. Les images sont redimensionnées à 64x64 pixels pour assurer l'uniformité.
- **Normalisation** :
  Les images sont normalisées pour avoir une moyenne de 0 et un écart-type de 1, ce qui stabilise le processus d'apprentissage.
- **Visualisation** :
  Utilisez la fonction `plot_images` pour visualiser des exemples d'images du dataset.

## Architecture du Modèle 🏗️

L'architecture du modèle repose sur ResNet, avec les éléments suivants :

- **Blocs ResNet** : Ces blocs permettent au modèle de s'entraîner plus efficacement en permettant le passage d'informations entre les couches via des connexions résiduelles.
- **Pooling Global** : Le pooling global réduit chaque carte de caractéristiques à une seule valeur, ce qui aide à prévenir le surapprentissage et à réduire le nombre de paramètres.

Le modèle est compilé avec l'optimiseur Adam et la fonction de perte `categorical_crossentropy`, optimisée pour une classification multi-classes.

## Entraînement 🏋️

Le modèle est entraîné pendant 100 époques avec une taille de batch de 64 :

- **Données d'Entraînement** : Les images prétraitées et normalisées sont utilisées pour l'entraînement.
- **Sauvegarde du Modèle** : Une fois l'entraînement terminé, le modèle est sauvegardé sous le nom `ResNet_model_groupe_2.h5`.

Pour entraîner le modèle, exécutez simplement le script :

```bash
python train_model.py
```

## Résultats 📊

Le modèle est évalué en fonction de l'accuracy, avec des performances mesurées sur plusieurs essais :

- Les résultats montrent une précision moyenne de **84,90%** sur 10 tests.

## Contributeurs 🤝

Ce projet a été développé par :

- **ISSA IBRAHIM Moubarak**
- **Abdourahamen Bachir**

---

Cet exemple de README fournit des instructions claires pour comprendre, installer, et exécuter le code. Il peut être ajusté en fonction des spécificités du projet ou de la structure de votre code.

Voici un exemple de README pour le code que vous avez fourni :

---

# Classification des Feuilles de Plantes avec ResNet 🌱

## Présentation du Projet 📋

Ce projet vise à classifier les images des feuilles de plantes, en particulier celles de pommes de terre, à l'aide d'un modèle de deep learning basé sur l'architecture ResNet. Le modèle est conçu pour être robuste et efficace, utilisant des blocs de convolution résiduels pour capturer des caractéristiques complexes dans les images.

## Table des Matières 📑

- [Présentation du Projet](#présentation-du-projet-📋)
- [Installation](#installation-🛠️)
- [Prétraitement des Données](#prétraitement-des-données-🖼️)
- [Architecture du Modèle](#architecture-du-modèle-🏗️)
- [Entraînement](#entraînement-🏋️)
- [Résultats](#résultats-📊)
- [Contributeurs](#contributeurs-🤝)

## Installation 🛠️

1. **Cloner le Dépôt** :

   ```bash
   git clone https://github.com/username/plant-leaf-classification.git
   cd plant-leaf-classification
   ```
2. **Installer les Dépendances** :
   Assurez-vous d'avoir Python installé (version 3.7 ou plus récente). Ensuite, installez les packages requis :

   ```bash
   pip install -r requirements.txt
   ```
3. **Structure des Répertoires** :
   Assurez-vous que votre structure de répertoires pour les images est la suivante :

   ```
   /Data
   ├── TrainData
   │   ├── Classe1
   │   ├── Classe2
   │   └── ...
   └── TestData
       ├── Classe1
       ├── Classe2
       └── ...
   ```

## Prétraitement des Données 🖼️

- **Chargement des Images** :
  Le script utilise `os.walk` pour parcourir le répertoire du dataset, en chargeant les images de chaque sous-dossier correspondant à une classe. Les images sont redimensionnées à 64x64 pixels pour assurer l'uniformité.
- **Normalisation** :
  Les images sont normalisées pour avoir une moyenne de 0 et un écart-type de 1, ce qui stabilise le processus d'apprentissage.
- **Visualisation** :
  Utilisez la fonction `plot_images` pour visualiser des exemples d'images du dataset.

## Architecture du Modèle 🏗️

L'architecture du modèle repose sur ResNet, avec les éléments suivants :

- **Blocs ResNet** : Ces blocs permettent au modèle de s'entraîner plus efficacement en permettant le passage d'informations entre les couches via des connexions résiduelles.
- **Pooling Global** : Le pooling global réduit chaque carte de caractéristiques à une seule valeur, ce qui aide à prévenir le surapprentissage et à réduire le nombre de paramètres.

Le modèle est compilé avec l'optimiseur Adam et la fonction de perte `categorical_crossentropy`, optimisée pour une classification multi-classes.

## Entraînement 🏋️

Le modèle est entraîné pendant 100 époques avec une taille de batch de 64 :

- **Données d'Entraînement** : Les images prétraitées et normalisées sont utilisées pour l'entraînement.
- **Sauvegarde du Modèle** : Une fois l'entraînement terminé, le modèle est sauvegardé sous le nom `ResNet_model_groupe_2.h5`.

Pour entraîner le modèle, exécutez simplement le script :

```bash
python train_model.py
```

## Résultats 📊

Le modèle est évalué en fonction de l'accuracy, avec des performances mesurées sur plusieurs essais :

- Les résultats montrent une précision moyenne de **84,90%** sur 10 tests.

## Contributeurs 🤝

Ce projet a été développé par :

- **ISSA IBRAHIM Moubarak**
