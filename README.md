# Create-PyTorch-Model-for-Raspberry-
a Jupyter notebook for creating a PyTorch object recognition model that can run on a Raspberry Pi
 
<h1 style="text-align: center;">
  <p align="center">
Les étapes préalables
</h1></p>
</br>
<p align="left"> 

  ### *GitBash*
pour que tout fonctionne sous Windows nous devons installer certains programmes. En premier nous allons télécharger et installer l'application GitHub: 
  
- <a href="https://git-scm.com/"> Application GitHub </a>

  Choisir la version correspondant à votre système d'exploitation. Ce programme permettra de pouvoir cloner des "repositories" GitHub dont nous aurons besoin par la suite 
y compris le Github présent contenant tous les codes dans des jupyter nootebook pour l'entrainement de notre modèle.

### *Python* 
Ensuite télécharger et installer  python (notebook testé avec python 3.13.15) :
 - <a href="https://www.python.org/downloads/windows/"> Python </a>


### *Utilisation des GPUs (mémoire de la carte graphique)*
Cette étape n'est pas obligatoire mais fortement conseillé si vous souhaitez accéler l'apprentissage du modèle en utilisant l'accélaration des cartes vidéos.
Cependant en fonction des versions CUDA et CuDNN installé sur votre ordinateur des petites variations dans le notebook seront à effectuer
suivez les instructions suivantes
</br>
##### *Installer CUDA *
Il vous faudra vous rendre sur le site <a href="https://developer.nvidia.com/cuda-toolkit-archive">CUDA</a> et télécharger et installer la version compatible avec votre carte graphique 

 
<h1 style="text-align: center;">
  <p align="center">
    Création et preparation de votre environement virtuel python
</h1></p>
</br>
<p align="left"> 


## Les étapes
<br />
<b>Etape 1.</b> Créer un dossier de travail sur votre ordinateur (par exemple pytorch_models)
<br/>
<br/>
<b>Etape 2.</b> ouvrir une invite de commande et se positionner dans le dossier que vous venez de créer</br>

```
cd pytorch_models
```

<b>Etape 3.</b> dans l'invite de commande cloner le repository actuel en tapant :

```
git clone https://github.com/brice-ronsin/pytorch_models_pi
```


<b>Etape 4.</b> Positionnez vous dans le dossier nouvellement crée 

```
cd pytorch_models_pi
```


<b>Etape 5.</b> Créer un nouvel environement virtuel python du nom que vous souhaitez,  en utilisant le python que vous avez installé (exemple avec python 3.13)

```
py -3.13 -m venv pytorch (pytorch ici, ou le nom que vous souhaitez)
```


<b>Etape 6.</b> Activate votre nouvel environement
```
source pytorch/bin/activate # Linux
.\pytorch\Scripts\activate # Windows 
  remplacer tflite par le nom de votre environnement
```


<b>Etape 7.</b> Installer si vous ne l'avez pas sur votre ordinateur jupyter notebook et mettre à jour jupyterlab

```
pip install jupyter
```
```
pip install jupyterlab==4.4.5
````
<br/>
<b>Etape 9.</b> depuis l'invite de commande taper jupyter notebook pour ouvrir notebook

```
jupyter notebook
```
<br/>
<b>Etape 10.</b> Collecter vos images en utilisant le Notebook <a href="https://github.com/brice-ronsin/mifobio_discoscope/blob/main/1.Mifobio%202025%20collecte%20et%20annotation%20des%20images.ipynb">1.Mifobio 2025 collecte et annotation des images.ipynb</a> - Assurez vous de changer et d'utiliser le bon kernel pour votre environnement virtuel comme montré ci dessous


