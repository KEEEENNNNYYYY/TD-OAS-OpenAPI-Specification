# TD-OAS-OpenAPI-Specification
* Consignes :

    Créer un repo sur Github et push en utilisant des commits selon les standards des conventional commit (https://www.conventionalcommits.org/en/v1.0.0/) tout au long de vos modifications.
    
    L’intégralité du document doit être écrit en ANGLAIS.


# TD1 : Rappel spécification OpenAPI 3.1.0
Thème : Gestion de bibliothèque

Nous voulons documenter la spécification d’une gestion de bibliothèque. Concentrons nous dans ce premier TD sur la spécification de la gestion des livres et des auteurs. 

* Au niveau de l’OpenAPI, voici le travail attendu :
    Points d’entrée attendus :
  * /books avec les méthodes attendues GET, POST, PUT, DELETE
    Dans GET /books, il est possible d’effectuer un filtre par bookName et par releaseDate (une intervalle de dates)
    * PUT /books est une requête idempotente. 
    Dans la v1.0.0, la propriété author est juste du texte correspondant au nom de l’auteur.


  * /authors avec les méthodes attendues GET, POST, PUT, DELETE
    * Dans GET /authors, il est possible d’effectuer un filtre par authorName 
    * PUT /authors est une requête idempotente


* Caractéristiques des ressources : 
    * Book : ID, bookName, author*, pageNumbers, topic (valeurs possibles : ROMANCE, COMEDY, OTHER), releaseDate


    * Author* : ID, Name, Sex (valeurs possibles : M ou F)

À travers cette spécification, nous voulons tester sur Postman si la spécification répond vraiment à nos attentes. “Uploader” la spécification sur SwaggerHub afin de bénéficier du service du serveur mock, et faites le test de chaque point d’entrée sur Postman en créant une collection Postman avec toutes les requêtes. 

   * Tips : il existe une fonctionnalité sur Postman, qui permet d’uploader une spécification OpenAPI (fichier .yaml) qui génère directement la collection Postman associée.
