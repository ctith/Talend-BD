1. télécharger fichier zippé + jar (serveur SOAP MDM en java): https://fr.talend.com/products/mdm/mdm-open-studio/ 

2. pour installer mdm, cliquer sur le .jar
- apache tomcat
- H2 Embedded
- port 8180
- TMDM_DB talend ****** ****** (talend)

3. lancer le serveur apache tomcat = serveur web http en cliquant dans le dossier serveur > startup.bat
> catalina.home est la variable d’environnement qui pointe vers tomcat donc on peut rajouter cette variable dans le fichier startup.bat si MDM la demande

4. http://localhost:8180/talendmdm/auth/login.jsp 
- id: admin
- mdp: talend

5. lancer talend, mettre à jour les librairies puis ajouter un server tomcat
- id : admin
- mdp : talend
