# 📊 Générateur de rapport d'analyse exploratoire

## 🚀 Description
Ce projet permet de **générer automatiquement un rapport d'analyse exploratoire (EDA)** à partir de fichiers de données.  
Il utilise la librairie **[`ydata-profiling`](https://github.com/ydataai/ydata-profiling)** pour produire un rapport interactif en HTML contenant :

- Statistiques descriptives 📈  
- Visualisations des distributions et corrélations 📊  
- Détection des valeurs manquantes et doublons 🔎  
- Informations sur la qualité des données 📑  

Le script est **convivial pour les débutants** et permet de charger des fichiers via :  
- **Ligne de commande** (CSV, Excel, JSON, Parquet)  
- **Saisie interactive** dans le terminal  
- **Sélection graphique de fichier** avec une boîte de dialogue  

---

## 🛠️ Installation

### 1. Cloner le dépôt
```bash
git clone https://github.com/<ton-utilisateur>/<nom-du-repo>.git
cd <nom-du-repo>
```

### 2. Créer un environnement virtuel (optionnel mais recommandé)
```bash
python -m venv venv
source venv/bin/activate   # Linux / macOS
venv\Scripts\activate      # Windows
```

### 3. Installer les dépendances
```bash
pip install -r requirements.txt
```

**Exemple de contenu de `requirements.txt` :**
```
pandas
ydata-profiling
openpyxl
pyarrow
tk
```

---

## ▶️ Utilisation

### Option 1 : Mode interactif (terminal)
Lancer le script et répondre aux questions :
```bash
python analyse.py
```
Exemple :
```
👉 Entrez le chemin de votre fichier (CSV, Excel, JSON, Parquet) : events.csv
👉 Nom du rapport de sortie (ex: rapport.html) [Entrée = rapport_analyse.html] : 
✅ Dataset chargé : 1000 lignes, 10 colonnes
📊 Rapport généré : ouvre 'rapport_analyse.html' dans ton navigateur.
```

---

### Option 2 : Sélection graphique de fichier (boîte de dialogue)
Pour un utilisateur novice, le script ouvre une fenêtre pour choisir le fichier :
```bash
python analyse_gui.py
```

---

### Option 3 : Ligne de commande avec arguments
Pour les utilisateurs avancés, tu peux passer le fichier et le nom du rapport directement :
```bash
python analyse.py chemin/vers/fichier.csv -o rapport.html
```

---

## 📂 Structure du projet
```
├── analyse.py             # Script principal (interactive + CLI)
├── analyse_gui.py         # Script avec sélection graphique
├── events.csv             # Exemple de dataset
├── rapport_analyse.html   # Rapport généré (output)
└── requirements.txt       # Dépendances Python
```

---

## ✨ Exemple de sortie

Le rapport HTML généré contient :  

- **Vue d’ensemble** : dimensions, types de colonnes, valeurs uniques  
- **Distributions** : histogrammes, diagrammes circulaires  
- **Corrélations** : heatmap interactive  
- **Qualité des données** : valeurs manquantes, doublons, incohérences  

---

## 📌 Améliorations possibles
- Ajouter des options de filtrage pour certaines colonnes  
- Exporter le rapport en PDF ou JSON  
- Ajouter un mode batch pour analyser plusieurs fichiers d’un coup  

---

## 👤 Auteur
- **Kossi Noumagno**  
Étudiant en Master Ingénierie Mathématique et Data Science, passionné par l’**analyse de données** et l’**IA appliquée**.
