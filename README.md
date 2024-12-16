# 📜 **Tutoriel : Configuration SRBMiner et Mineur Officiel**

## **Objectif**  
Configurer vos paramètres pour **miner du Quai sur [pool-poussin.fr](https://pool-poussin.fr/)** en modifiant uniquement votre **pseudo**.

---

## **1. Configuration de SRBMiner-MULTI**

1. **Ouvrez l'interface SRBMiner-MULTI**  
   Voici comment se présente la fenêtre de configuration :

   ![SRBMiner-MULTI Configuration](Capture d'écran%202024-12-16%20195502.png)

2. **Changement du pseudo**  
   - Remplacez **`PSEUDO`** par **votre propre pseudo** dans le champ **Wallet**.  
     Exemple :  
     ```plaintext
     Dorian.%WAL%
     ```
   - **Worker Name** : Gardez `%WORKER_NAME%`.  
   - **Pool Server:Port** :  
     ```plaintext
     stratum://pool-poussin.fr:3334
     ```

3. **Appliquer les changements**  
   Cliquez sur **"Apply Changes"** comme indiqué ci-dessous :

   ![Appliquer Changements SRBMiner](Capture d'écran%202024-12-16%20195502.png)

---

## **2. Configuration du Mineur Officiel**

1. **Ouvrez l'interface de configuration du Mineur Officiel**  
   La fenêtre ressemble à ceci :

   ![Custom Configuration](Capture d'écran%202024-12-16%20195631.png)

2. **Changer le pseudo**  
   - **Wallet et Worker Template** :  
     Remplacez **`PSEUDO`** par votre pseudo. Exemple :  
     ```plaintext
     Dorian.%WAL%
     ```  

3. **Extra Config Arguments**  
   Ajoutez les lignes suivantes selon votre type de carte graphique :

   - **Pour NVIDIA** :  
     ```plaintext
     -U --HWMON 1 -P stratum://Dorian.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3334
     ```

   - **Pour AMD** :  
     ```plaintext
     -G --HWMON 1 -P stratum://Dorian.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3334
     ```

4. **Appliquer les changements**  
   Cliquez sur **"Apply Changes"** comme indiqué sur l'image suivante :

   ![Appliquer Changements Configuration Personnalisée](Capture d'écran%202024-12-16%20195631.png)

---

## **3. Résultat Final**

Une fois votre pseudo modifié et les paramètres appliqués :
1. **Démarrez votre mineur**.
2. Vérifiez vos résultats sur le **pool de minage** :  
   [pool-poussin.fr](https://pool-poussin.fr/).

---

Ajoutez ce guide dans un fichier **README.md** sur votre dépôt **GitHub**. Placez également les captures d'écran dans le même dossier pour qu'elles s'affichent correctement.

---

🚀 **Bon minage !**
