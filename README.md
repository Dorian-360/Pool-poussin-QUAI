📘 Tutoriel : Configuration SRBMiner et Mineur Officiel
Objectif
Configurer vos paramètres pour miner du Quai sur pool-poussin.fr en modifiant uniquement votre pseudo.

1. Configuration de SRBMiner-MULTI
Ouvrez l'interface SRBMiner-MULTI
Voici comment se présente la fenêtre de configuration :

![SRBMiner-MULTI Configuration](Capture d'écran 2024-12-16 195502.png)

Changement du pseudo

Remplacez PSEUDO par votre propre pseudo dans le champ Wallet.
Exemple :
plaintext
Copier le code
Dorian.%WAL%
Worker Name : Gardez %WORKER_NAME%.
Pool Server:Port :
plaintext
Copier le code
stratum://pool-poussin.fr:3334
Appliquer les changements
Cliquez sur "Apply Changes" comme indiqué ci-dessous :

![Appliquer Changements SRBMiner](Capture d'écran 2024-12-16 195502.png)

2. Configuration du Mineur Officiel
Ouvrez l'interface de configuration du Mineur Officiel
La fenêtre ressemble à ceci :

![Custom Configuration](Capture d'écran 2024-12-16 195631.png)

Changer le pseudo

Wallet et Worker Template :
Remplacez PSEUDO par votre pseudo. Exemple :
plaintext
Copier le code
Dorian.%WAL%
Extra Config Arguments
Ajoutez les lignes suivantes selon votre type de carte graphique :

Pour NVIDIA :

plaintext
Copier le code
-U --HWMON 1 -P stratum://Dorian.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3334
Pour AMD :

plaintext
Copier le code
-G --HWMON 1 -P stratum://Dorian.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3334
Appliquer les changements
Cliquez sur "Apply Changes" comme indiqué sur l'image suivante :

![Appliquer Changements Configuration Personnalisée](Capture d'écran 2024-12-16 195631.png)

3. Résultat Final
Une fois votre pseudo modifié et les paramètres appliqués :

Démarrez votre mineur.
Vérifiez vos résultats sur le pool de minage :
pool-poussin.fr.
