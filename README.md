# TD-OAS-OpenAPI-Specification
* Consignes :

    Créer un repo sur Github et push en utilisant des commits selon les standards des conventional commit (https://www.conventionalcommits.org/en/v1.0.0/) tout au long de vos modifications.
    
    L’intégralité du document doit être écrit en ANGLAIS.

# TD1 : Rappel spécification OpenAPI 3.1.0
* Thème : Gestion de cours étudiants
  Nous voulons documenter la spécification d’une gestion des cours des étudiants. Concentrons
  nous dans ce premier TD sur la spécification de la gestion des groupes et des étudiants.
1. Au niveau de l’OpenAPI, voici le travail attendu :
  a. Points d’entrée attendus :
   - /groups avec les méthodes attendues GET, POST, PUT, DELETE
   - Dans GET /groups, il est possible d’effectuer un filtre par groupName et
par groupYear (une intervalle de dates)
   - PUT /groups est une requête idempotente.
   - /students avec les méthodes attendues GET, POST, PUT, DELETE
   - Dans GET /students, il est possible d’effectuer un filtre par studentName
   - PUT /students est une requête idempotente
   - Dans la v1.0.0 de l’API, le type de group peut juste être de type texte.
Pour faire référence notamment au nom du groupe : J2 par exemple
  b. Caractéristiques des ressources :
   - Group : ID, groupName, groupYear, promotion (valeurs possibles G, H, J, K),
studentNb, students* (liste de Student)
   - Student* : ID, Name, Sex (val*eurs possibles : M ou F), birthdate, reference (ex:
STD23XXX), group (type texte suffit pour la version 1.0.0)
2. À travers cette spécification, nous voulons tester sur Postman si la spécification répond
  vraiment à nos attentes. “Uploader” la spécification sur SwaggerHub afin de bénéficier
  du service du serveur mock, et faites le test de chaque point d’entrée sur Postman en
  créant une collection Postman avec toutes les requêtes.