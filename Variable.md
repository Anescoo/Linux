# LES VARIABLES

>- Définition

  
  Dans un language de programmation, une variable est un espace de stockage pour un résultat. Cependant les possibilités d'une variable sont intimement liées au language de programmation auquel ont fait référence. Par exemple une variable en C++ aura six caractéristiques : 
  
  - **son nom** : sous quel nom est déclaré la variable.
  - **son type** : c'est la convention d'interprétation de la séquence de bits qui constitue la variable. 
  - **sa valeur** : c'est la séquence de bits elle-même.
  - **son adresse** : c'est l'endroit dans la mémoire où elle est stockée.
  - **sa visibilité** : c'est un ensemble de règles fixe qui peut utiliser la variable. (public, private, protected).
  - **sa durée de vie** : c'est la portion de code dans laquelle la variable existe.
---
>- Les Types
  
  Ils existent de nombreux types de variable : 

- **string** : Chaîne de texte
- **int** : Nombre entier *32 bits*
- **char** : Symbole
- **bool** : Booléen (la valeur peut être *true* ou *false*)
- **long** : Nombre entier *64 bits*
- **decimal** : Nombre décimal *128 bits* avec la lettre « d » à la fin
- **double** : Nombre décimal à virgule flottante de *8 octets*
- **single** : Nombre décimal à virgule flottante de *32 bits*
- **DateTime** : Date et heure
- **array** : Tableau (décrit en détail plus loin dans l’article)
- **hashtable** : Table de hachage


---

- **$NomVariable** = 'Hello'
    - déclaration de variable


        ![](Images/nomvariable.PNG)
---
- **$NomVariable.GetType()**
  - pour connaitre le type de la variable

    ![](Images/typevariable.PNG)
---
- **[type]$NomVariable** = 'Hello'
  - forcer le typage d'une variable
  
    ![](Images/typeforce.PNG)

---

- **Get-Variable | Out-String**
  - Afficher les variables
  
    ![](Images/getvariable.PNG)

---
    Pour Imprimer une variable :

1. *Enregistrer dans un fichier .txt*
- **$varshell = "Hello World!"**
- **$varshell | Out-File C:Users\arnau\Documents\Hello_World.txt**
    - >J'enregistre le fichier texte avec le chemin indiqué
      
      ![](Images/1.PNG) 

    - >Je me déplace dans le dossier **Documents** et je constate la présence du fichier **.txt** (nommé *"Hello_World"*)
![](Images/2.PNG)


2. *Enregistrer dans un ficher .csv*
- **$varsh1 = Get-Process**
- **$varsh1 | SELECT Name, Path |Export-Csv -Path C:\Users\arnau\Documents\processes.csv**
   - > J'enregistre le fichier **.csv** avec le chemin indiquée
  ![](Images/3.PNG)

    - > Je me déplace dans le dossier **Documents** et je constate la présence du fichier **.csv** (nommé *"processes"*)
  ![](Images/4.PNG)
---
    Pour lire un fichier que vous avez exporté
- **Get-Content C:Users\arnau\Documents\processes.csv**
  - > Après avoir exécuté la commande, une liste de tous les fichiers exportés s'est affiché
  ![](Images/5.PNG)

---
    Pour Effacer une variable
- **Clear-Variable -name varshell #without $**
  - > Après avoir exécuté la commande, la variable *"$"* s'est bien effacé
  ![](Images/6.PNG)

---
    Supprimer une variable
- **Remove-Variable -name varshell #without $**
  - > Après avoir exécuté la commande, la variable *"$"* s'est bien supprimé
  ![](Images/7.PNG)
 
---

6. [Boucles](https://github.com/Anescoo/Linux/blob/main/Boucles.md) (page suivante)