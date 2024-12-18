
---

## **2. Configuration du Mineur Officiel**

1. **Ouvrez l'interface de configuration du Mineur Officiel**  
   La fenêtre ressemble à ceci :

   ![Capture d'écran 2024-12-16 195502](https://github.com/user-attachments/assets/bd1e2389-b301-4655-825f-397e13b1ae99)

2. **Changer le pseudo dans Extra Config Arguments**  
   - **Wallet et Worker Template** :  
     ```
     %WAL%.%WORKER_NAME%
     ```

   - **Pool Server:Port** :  
     ```
     stratum://pool-poussin.fr:3334
     ```

3. **Extra Config Arguments**  
   Ajoutez les lignes suivantes selon votre type de carte graphique et remplacez **PSEUDO** par votre pseudo. Exemple :

   - **Pour NVIDIA** :  
     ```
     -U --HWMON 1 -P stratum://PSEUDO.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3334
     ```

   - **Pour AMD** :  
     ```
     -G --HWMON 1 -P stratum://PSEUDO.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3334
     ```

4. **Appliquer les changements**  
   Cliquez sur **"Apply Changes"** et lancez votre feuille de route.

---

## **3. Résultat Final**

Une fois votre pseudo modifié et les paramètres appliqués :
1. **Démarrez votre mineur**.
2. Vérifiez vos résultats sur le **pool de minage** :  
   [pool-poussin.fr](https://pool-poussin.fr/).

---

🚀 **Bon minage !**
