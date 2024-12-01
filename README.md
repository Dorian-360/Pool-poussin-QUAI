Pour vous connecter à la pool, il vous suffit de suivre les étapes décrites dans la feuille de route ci-dessous.




![FS](https://github.com/user-attachments/assets/e584e4a7-b216-4b57-914c-d7fbff784b34)


Installation URL:
https://github.com/dominant-strategies/quai-gpu-miner/releases

Pool URL:
stratum://pool-poussin.fr:3333

Extra config arguments:

NVIDIA: 
-U --HWMON 1 -P stratum://pool-poussin.fr:3333

AMD: 
-G --HWMON 1 -P stratum://pool-poussin.fr:3333

# Lancer le minage sur Pool-Poussin avec HiveOS

1. **Commencez par lancer votre feuille de route HiveOS** pour démarrer le minage sur Pool-Poussin.

2. **Ensuite, ouvrez un terminal et passez en mode super utilisateur** :
   ```bash
   sudo su
   cd /home/user
   ```

3. **Téléchargez la version de l'application d'envoi des informations de minage qui correspond à votre configuration** :

   - **Version pour AMD à partir de la V0.4.0 :**
     ```bash
     wget https://github.com/Dorian-360/Pool-poussin-QUAI/releases/download/V0.4.0/pool-poussin-quai.zip
     ```
   
   - **Version pour Nvidia (V0.3.0 et antérieure) :**
     ```bash
     wget https://github.com/Dorian-360/Pool-poussin-QUAI/releases/download/V0.3.0/pool-poussin-quai.zip
     ```

   - **Version pour Nvidia à partir de la V0.4.0 :**
     ```bash
     wget https://github.com/Dorian-360/Pool-poussin-QUAI/releases/download/v0.4.1/pool-poussin-quai.zip
     ```

4. **Dézippez l'archive téléchargée** :
   ```bash
   unzip pool-poussin-quai.zip
   ```

5. **Accédez au répertoire extrait** :
   ```bash
   cd pool-poussin-quai
   ```

6. **Modifiez le fichier de configuration pour entrer vos informations personnelles** (utilisez le même pseudo pour chaque rig) :
   ```bash
   nano config.txt
   ```

7. **Rendez le script exécutable** :
   ```bash
   chmod +x ordre.sh
   ```

8. **Lancez le script pour commencer le minage** :
   ```bash
   ./ordre.sh
   ```

9. **Pour vérifier le statut du service Pool-Poussin**, utilisez la commande suivante :
   ```bash
   journalctl -fu pool-poussin.service
   ```

Et voilà ! Le minage devrait être en cours.

