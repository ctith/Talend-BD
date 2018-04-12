# TP MDM

## 1. Importer fichiers csv de travail

Cliquer en haut à droite sur **Profiling**

Importer les fichiers Clients_InfoPerso_2.csv et Clients_InfoPro_2.csv
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_33_47-Nouveau%20fichier%20d%C3%A9limit%C3%A9.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_36_00-Editer%20un%20fichier%20d%C3%A9limit%C3%A9%20existant.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_34_14-Nouveau%20fichier%20d%C3%A9limit%C3%A9.png)

## 2. Créer une analyse simple de colonne

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_40_51-.png)

Sélectionner les colonnes à afficher puis rafraichir le tableau
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_42_09-S%C3%A9lection%20de%20colonne(s).png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_42_28-.png)

Définir les regex pour chacun des modèles
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_47_33-.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2011_44_31-S%C3%A9lecteur%20de%20mod%C3%A8le.png)

Visualisation des résultats

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/view1.png)

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/view2.png)

## 3. Envoyer les fichiers csv dans une BDD

Cliquer en haut à droite sur **Integration**


## 4. Créer un modèle de données

Cliquer en haut à droite sur **MDM**

ajouter nouvelle entité

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_40_05-Nouvelle%20entit%C3%A9.png)

ajoute nouvel élément métier

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_39_44-Ajouter%20un%20nouvel%20%C3%A9l%C3%A9ment%20m%C3%A9tier.png)

rajouter une clé étrangère (set the foreign key puis set the foreign key infos)

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_48_16-Configurer%20la%20cl%C3%A9%20%C3%A9trang%C3%A8re.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_48_06-Select%20Xpath.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_48_36-Talend-BD_Talend-screenshot%20at%20master%20%C2%B7%20ctith_Talend-BD.png)

Visualisation du modèle sous forme xpath

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_49_52-Editing%20Talend-BD_TP_MDM.md%20at%20master%20%C2%B7%20ctith_Talend-BD.png)


## 5. Créer une view

Créer une vue web sur les clients

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_58_45-Nouvelle%20Vue.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2014_58_37-S%C3%A9lectionnez%20une%20Entit%C3%A9.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_05_59-.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_06_23-.png)

## 6. Déployer le modèle sur le serveur

Vérifier que le serveur est bien réglé
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_11_15-server.png)

Clic droit sur Data Model > System > Client MDM > Déployer le modèle pour tous les éléments créés (container, modele, vue)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_09_52-.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_09_40-.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_15_58-.png)

## 7. Accéder au modèle crée sur un navigateur web

### Connexion à Talend UI via un navigateur web

http://localhost:8180/talendmdm/ui

Pour visualiser les données :
- id: user
- mdp: user

Pour pouvoir créer des clients :
- id: administrator
- mdp: administrator

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_21_51-Talend%20MDM.png)

### Créer des clients

Quand on crée un premier client qui habite dans un appartement, l'UI ne l'affiche pas car nous avons créé une vue qui n'affiche que les clients habitant dans une maison. Quand on crée un client qui habite dans une maison, il sera affiché dans la vue. Si on veut afficher tous les clients, il faut enlever la contrainte sur la maison et tout redéployer sur le serveur.

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_39_19-Talend%20MDM.png)

## 8. Créer un job talend pour alimenter la BDD

Cliquer en haut à droite sur **Integration**

### Créer une connexion MDM
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_48_09-connexionMDM.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_48_26-Connexion%20au%20MDM.png)

Créer un MDM Client Output (clic droit sur le MDM)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_51_52-.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_52_00-.png)

### Créer un job

On va envoyer nos données des fichiers csv dans le serveur donc ce qui nous intéresse sont que les infos du MDM concernant les clients. On les récupère grâce au composant tMap.

Faire la correspondance des noms de champs entre les colonnes à celle du modèle MDM
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2016_08_46-Talend%20Open%20Studio%20for%20MDM%20-%20tMap%20-%20tMap_1.png)

Cliquer sur "..." de xpath
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2016_05_19-Talend%20MDM.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2016_05_07-tMDMOutput_1.png)

Pour pouvoir envoyer les clients, il faut d'abord créer une table département comme elle est utilisée en clé étrangère.
Il faudra alors supprimer les départements redondants.

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2016_50_35-job%20dept.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2016_50_49-job%20client.png)

### Créer un trigger

Permet de récupérer toutes les opérations effectuées dans un job.

Clic droit sur un job > Generate Talend Job Trigger 

Dans Event Management > Trigger: modifier les xpath expression pour garder les opérations que l'on veut enregistrer dans un trigger
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2017_04_36-trigger01.png)

Puis faire un job qui va extraire les triggers qui nous intéresse
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2016_56_40-trigger02.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2017_05_19-trigger03.png)
