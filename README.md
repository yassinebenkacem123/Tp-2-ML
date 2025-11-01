# 🧠 TP2 – Apprentissage Profond avec TensorFlow / Keras
**Module : Technologies de l’Intelligence Artificielle**  
**Encadrant : Pr. Youness IDRISSI KHAMLICHI**  
**Filière : Ingénierie Logicielle et Intelligence Artificielle – ILIA2**  
**École : ENSA Fès**

---

## 🎯 Objectif du TP

Ce TP a pour but d’introduire les concepts fondamentaux de l’**apprentissage profond (Deep Learning)** à travers la mise en œuvre de réseaux de neurones artificiels avec **TensorFlow** et **Keras**.  
Les étudiants apprendront à construire, entraîner et évaluer des modèles capables de reconnaître des images issues des jeux de données **MNIST** et **Fashion-MNIST**.

---

## 📘 Contenu du TP

### 🔹 Exercice 1 – Reconnaissance de chiffres manuscrits (MNIST)

**But :** Construire un réseau de neurones entièrement connecté (Dense Neural Network) pour reconnaître les chiffres manuscrits de 0 à 9.

**Dataset :** [MNIST – Kaggle](https://www.kaggle.com/datasets/hojjatk/mnist-dataset)  
**Taille :** 70 000 images (28×28 pixels, niveaux de gris)

#### Étapes :
1. Charger et normaliser les données  
2. Visualiser quelques exemples d’images  
3. Créer un modèle `Sequential` avec les couches :
   - `Flatten()` pour transformer les images 2D en vecteurs 1D  
   - `Dense(128, activation='relu')`  
   - `Dense(10, activation='softmax')`
4. Compiler le modèle avec :
   - Optimiseur : `adam`  
   - Fonction de perte : `sparse_categorical_crossentropy`  
   - Métrique : `accuracy`
5. Entraîner le modèle sur 5 époques  
6. Évaluer les performances sur le jeu de test  
7. Visualiser les courbes d’apprentissage (accuracy et loss)  
8. Afficher quelques prédictions sur des images tests  

---

### 🔹 Exercice 2 – Classification d’images : Fashion-MNIST

**But :** Découvrir le **Deep Learning** à travers la classification d’images de vêtements (T-shirt, pantalon, robe, etc.).

**Dataset :** [Fashion-MNIST – Kaggle](https://www.kaggle.com/datasets/zalando-research/fashionmnist)  
**Taille :** 70 000 images (60 000 train, 10 000 test)

#### Étapes principales :
1. **Exploration** du dataset et visualisation d’exemples  
2. **Prétraitement :**  
   - Normalisation des pixels entre 0 et 1  
   - Encodage des labels (one-hot encoding)
3. **Modèle Dense (ANN)** :  
   - Entraînement et évaluation du modèle
4. **Comparaison des fonctions d’activation** : ReLU, Sigmoid, Tanh, LeakyReLU  
5. **Création d’un modèle CNN (Convolutional Neural Network)** pour améliorer la précision  
6. **Visualisation des performances** et analyse des erreurs  
7. **Data Augmentation** pour enrichir les données d’entraînement

---

## 🧪 Concepts clés abordés

| Concept | Description |
|----------|--------------|
| **Neurone** | Unité de base d’un réseau, effectuant un calcul pondéré puis une activation. |
| **Couche (Layer)** | Regroupe plusieurs neurones traitant une représentation des données. |
| **Fonction d’activation** | Introduit la non-linéarité (ReLU, Sigmoid, Softmax). |
| **Fonction de perte** | Mesure la différence entre la prédiction et la valeur réelle. |
| **Optimiseur** | Méthode d’ajustement des poids (Adam, SGD, RMSprop). |
| **Époque (Epoch)** | Une itération complète sur toutes les données d’entraînement. |
| **Batch** | Sous-ensemble des données utilisé à chaque itération. |
| **Rétropropagation** | Ajustement des poids selon l’erreur obtenue. |

