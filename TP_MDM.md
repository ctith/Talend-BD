# TP MDM

## 1. Importer fichiers csv de travail

Cliquer en haut à droite sur Profiling

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

Cliquer en haut à droite sur Integration


## 4. Créer un modèle de données

Cliquer en haut à droite sur MDM

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

## 6. Déployer le modèle

Vérifier que le serveur est bien réglé
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_11_15-server.png)

Clic droit sur Data Model > System > Client MDM > Déployer le modèle
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_09_52-.png)
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2015_09_40-.png)
