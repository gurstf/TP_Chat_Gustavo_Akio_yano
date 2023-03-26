Reponses

1.PRISE EN MAIN
1.1. La topology s'appelle étoile.
1.2. Dans les logs, on peut voir les informations de le serveur, qui entrée, les messages et le callback handler.
1.3. Le problème c' est que tout monde peut voir les messages envoyé sur le terminal
1.4. Chiffrer les messages et ajouter le mot de passe pour eviter garantir la confidentialite des les données

2.CHIFFREMENT
2.1. Le fonction urandom c'est une option flexible mais deterministe, la generation c'est pour une cadre mathematique. Les inputs de le systems peuvent change le valeur genere, on'appele ça d'entropie.
du coup la fonction urandom c'est pas le mieu pour l'utilisation
2.2. Parce que les cryptographiques primitives sont deja connu pour beaucoup d'utilisateurs
2.3. Parce que le serveur pouvent recuperer les messages anciennes  pour decrypter et voir les messages
2.4. Il manque les confidentialite de les nom d'utilisateurs et la restriction de les membres de change le program

3.AUTHENTICATED SYMETRIC ENCRYPTION
3.1. Parce que on peut tracer possibles modifications dans les messages 
3.2. Attaque par rejeu
3.3. On peut limiter le temps avec timestamp (librarie time) 

4.TTL
4.1. Quand'on ajout du TTL les messages ont la vie limitee, permet d'eviter les attaque par rejeu
4.2. Le message est expire parce que le TTL il n'est pas signe
4.3. Oui, comment le TTL faire les messages avec vie limitee.
4.4. C'est possible que les messages sont expiree avec une probleme de connexion

REGARD CRITIQUE

Oui, il y a des vulnérabilités car les bibliothèques utilisées sont déjà connues, elles permettent aux utilisateurs malveillants d’entrer des données qui peuvent être acceptées et traitées comme des données légitimes.
Pour éviter cela, le serveur doit vérifier chaque détail de sécurité, que ce soit le temps, l’auteur, le cryptage pour garantir son authenticité.
Une bonne méthode pour assurer la sécurité du message serait de cesser d’utiliser urandom, une valeur déterministe et d’utiliser une valeur vraiment aléatoire. 
Il est nécessaire que la clé soit toujours unique et différente, afin de garantir l’authenticité et les éventuels messages frauduleux.
