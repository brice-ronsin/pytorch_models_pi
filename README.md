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

nous devons aussi installer la dépendance ipikernel.<br> 
ipikernel est une dépendance très importante car elle vous permet d'associer votre environnement virtuel à votre notebook jupyter.<br> 
Sans cette dépendance, quand vous lancerez jupyter notebook, ce dernier n'utilisera pas votre environnement virtuel.<br>   
De plus, nous devons aussi créer un noyau Python (kernel) pour les notebooks Jupyter<br>  
Alors que Jupyter garantit la disponibilité du noyau IPython par défaut, ipykernel vous permet d'utiliser différentes versions de Python<br>   
ou même d'utiliser Python dans un environnement virtuel ou conda.<br>  
Pour ajouter le python 3.9.2 nécéssaire à notre Jupyter Notebook, tapez "python -m ipykernel install --user --name=tflite".<br>  
Cela permettra dans votre jupyter notebook d'utiliser le noyau dédié à votre environnemnt virtuel<br>
<br/>
<br/>
<b>Etape 7.</b> Installer les dépendences et ajouter l'environnement virtuel au noyau kernel de notre jupyter notebook

```
pip install ipykernel
```
```
python -m ipykernel install --user --name=tflite
````
<br/>
<b>Etape 8.</b> Installer si vous ne l'avez pas sur votre ordinateur jupyter notebook et mettre à jour jupyterlab

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
<img src="https://github.com/brice-ronsin/mifobio_discoscope/blob/main/pictures/jupyter_notebook.png"> 
<br/>
<br/><br/>
<b>Etape 11.</b> une fois le premier notebook fini (images sauvegardées et annotées) <br/>
nous alons commencer le process d'entrainement en ouvrant <a href="https://github.com/brice-ronsin/mifobio_discoscope/blob/main/2.Mifobio_Train_model.ipynb">2. Mifobio_Train_model.ipynb</a> <br/>
Ce notebook vous permettra de réaliser l'installation de Tensorflow Object Detection, la réalisation de détections, la sauvegarde et l'exportation de votre modèle.
<br /><br/>
<br/>
<br/>

