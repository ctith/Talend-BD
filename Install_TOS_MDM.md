1. télécharger fichier zippé + jar (serveur SOAP MDM en java): https://fr.talend.com/products/mdm/mdm-open-studio/ 

2. pour installer mdm, cliquer sur le .jar
- apache tomcat
- H2 Embedded
- port 8180
- TMDM_DB talend ****** ****** (talend)

3. lancer le serveur apache tomcat = serveur web http en cliquant dans le dossier serveur > startup.bat
> catalina.home est la variable d’environnement qui pointe vers tomcat donc on peut rajouter cette variable dans le fichier startup.bat si MDM la demande

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2010_26_49-Talend%20MDM.png)

4. http://localhost:8180/talendmdm/auth/login.jsp 
- id: admin
- mdp: talend
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2010_26_27-Talend%20MDM.png)

5. lancer talend, mettre à jour les librairies puis ajouter un server tomcat
- id : admin
- mdp : talend
![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/server%20tomcat.png)

6. créer une analyse
*analyse inter-tables* : analyse de qualité de données
- analyse de redondance : clé étrangère et clé primaire
ex: table client (clé primaire) et table commande (clés étrangères) : 1 client peut avoir plusieurs commandes

*analyse de colonnes* 
- nominal values analysis (ex: analyse de code postaux, pas besoin de préciser que ce sont des int)
- analyse de colonne simple (nombre de null par colonne, nb de répétition de valeur par colonne
- analyse données discrète : analyse de données numériques

![](https://github.com/ctith/Talend-BD/blob/master/Talend-screenshot/2018-04-12%2010_39_52-Cr%C3%A9er%20une%20nouvelle%20analyse.png)
