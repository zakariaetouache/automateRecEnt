# Automate de Reconnaissance d'Entiers

Ce programme implémente un automate fini déterministe (AFD) capable de reconnaître des entiers positifs, négatifs ou sans signe à partir d'une chaîne de caractères saisie par l'utilisateur. Il utilise une table de transition d'état pour déterminer si la chaîne est un entier valide.

## Fonctionnalités
- Accepte des entiers sous les formats suivants : 
  - Un entier sans signe (ex : `123`)
  - Un entier positif avec le signe `+` (ex : `+123`)
  - Un entier négatif avec le signe `-` (ex : `-123`)
- Si la chaîne ne correspond pas à un entier valide, le programme retourne un message d'erreur.
  
## Algorithme
L'automate fonctionne sur trois états différents, et chaque caractère de la chaîne (soit un signe, soit un chiffre) détermine la transition vers l'état suivant.

- **État 0** : État initial. Le programme attend un signe (`+` ou `-`) ou un chiffre.
- **État 1** : Signe détecté, le programme attend un chiffre.
- **État 2** : Chiffres valides détectés.
- **État -1** : État d'erreur, signifiant que la chaîne n'est pas reconnue par l'automate.
