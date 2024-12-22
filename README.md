# 📜 **Tutoriel : Configuration du Mineur Officiel**

## **Objectif**

Configurer vos paramètres pour **miner du Quai sur [pool-poussin.fr](https://pool-poussin.fr/)** en modifiant uniquement votre **pseudo**.

---

## **1. Configuration de votre feuille de route hiveos**

1. **Crée un mineur custom**  
   La fenêtre ressemble à ceci :

   ![Capture d'écran 2024-12-16 195502](https://github.com/user-attachments/assets/bd1e2389-b301-4655-825f-397e13b1ae99)

2. **Mettre le lien installation URL**

### **Pour NVIDIA**

   - **Étape 1** : Lancer avec la version **0.3.0** du mineur :
   ```
   https://github.com/dominant-strategies/quai-gpu-miner/releases/download/v0.3.0/quai-gpu-miner-v0.3.0.tar.gz
   ```
   - **Étape 2** : Ensuite, mettez à jour vers la version **0.4.1** :
```
  https://github.com/dominant-strategies/quai-gpu-miner/releases/download/v0.4.1/quai-gpu-miner-nvidia-v0.4.1.tar.gz
```

### **Pour AMD**

   - **Lancer avec la version 0.4.1** du mineur pour AMD :
   ```
   https://github.com/dominant-strategies/quai-gpu-miner/releases/download/v0.4.1/quai-gpu-miner-amd-v0.4.1.tar.gz
   ```
3. **le pseudo se trouve dans Extra Config Arguments**  
   - **Wallet et Worker Template** :  
     ```
     %WAL%.%WORKER_NAME%
     ```

   - **Pool Server:Port** :  
     ```
     stratum://pool-poussin.fr:3334
     ```

4. **Extra Config Arguments**  
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
