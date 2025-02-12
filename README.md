# 📜 **Tutoriel : Configuration du Mineur Officiel**

## **Objectif**

Configurer vos paramètres pour **miner du Quai sur [pool-poussin.fr](https://pool-poussin.fr/)**.

---

## **1. Configuration de votre feuille de route hiveos**

1. **Crée un mineur custom**  
   La fenêtre ressemble à ceci :

![Capture d'écran 2025-02-12 110959](https://github.com/user-attachments/assets/46ed2be3-05c1-45f4-9a4d-c2ecaf2f5bec)

2. **Mettre le lien installation URL**

### **Pour NVIDIA**

   - **Lancer avec la version 0.5.0** du mineur pour NVIDIA:
   ```
   https://github.com/dominant-strategies/quai-gpu-miner/releases/download/v0.5.0/quai-gpu-miner-nvidia-v0.5.0.tar.gz
   ```

### **Pour AMD**

   - **Lancer avec la version 0.5.0** du mineur pour AMD :
   ```
   https://github.com/dominant-strategies/quai-gpu-miner/releases/download/v0.5.0/quai-gpu-miner-amd-v0.5.0.tar.gz
   ```
3. **Suite de la feuille de route**  
   - **Wallet et Worker Template** :  
     ```
     %WAL%.%WORKER_NAME%
     ```

   - **Pool Server:Port** :  
     ```
     stratum://pool-poussin.fr:3335
     ```

4. **Extra Config Arguments**  
   Ajoutez les lignes suivantes selon votre type de carte graphique Exemple :

   - **Pour NVIDIA** :  
     ```
     -U --HWMON 1 -P stratum://PSEUDO.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3335
     ```

   - **Pour AMD** :  
     ```
     -G --HWMON 1 -P stratum://PSEUDO.%WAL%.%WORKER_NAME%:x@pool-poussin.fr:3335
     ```

4. **Appliquer les changements**  
   Cliquez sur **"Apply Changes"** et lancez votre feuille de route.

---

## **3. Résultat Final**

Une fois les paramètres appliqués :
1. **Démarrez votre mineur**.
2. Vérifiez vos résultats sur votre **Dashboard** en entrant votre wallet dans la barre de recherche du pool:  
   [pool-poussin.fr](https://pool-poussin.fr/).
3. Vous avez la possibilité de modifier vos propres paramètre de minage directement dans Menu => Settings de votre Dashboard:
-    ✅ **Minimum Payout**
-    ✅ **Définir un pseudo** (pour faciliter l'accès au dashboard sur mobile)
-    ✅ **Supprimer les workers inutiles** (leurs gains sont conservés)


---
![Capture d'écran 2025-02-12 112022](https://github.com/user-attachments/assets/18f7480e-0028-47c7-a42e-b2538cde76b0)

🚀 **Bon minage !**
