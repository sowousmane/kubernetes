Ecrivez un manifest mysql-volume.yml déployant un pod (nommé mysql-volume) mysql, avec les paramètre d’environnement

 

suivants : nom bdd: eazytraining, login: eazy, mot de passe: eazy, mot de passe compte root: password

 

• Faites en sorte que le dossier contenant la base de données soit persistant en le montant sur votre nœud dans /data-volume en

 

utilisant le principe de volumes

 

• Lancez la création de votre pod, vérifiez que votre pod a bien démarré et que ce dernier consomme effectivement le dossier local /data-volume


• Ecrivez pv.yml (volume persistent de taille 1 Go utilisant le dossier local /data-pv pour stocker les donneés) et pvc.yml (volume persistent claim de taille 100 Mo utilisant le PV créé précedement pour stocker les données)
 
kubectl apply -f pv.yml  
kubectl apply -f pvc.yml 

 • Lancez la creation de vos pv et pvc et verifies qu’ils sont bien crées et prêt à être consommés

 
kubectl describe persistentvolumeclaim pvc
kubectl describe pv

• Ecrivez un manifest mysql-pv.yml déployant mysql (nommé mysql-pv) comme précédemment à la seule différence qu’il utilisera comme volume de stockage le PVC créé précédemment

 

• Vérifiez que votre pod consomme bien le stockage

kubectl apply -f mysql-pv.yml
kubectl describe po mysql-pv 

kubectl apply -f mysql-volume.yml
kubectl describe po mysql-volume 


• Créez un repertoire tp-4 dans Kubernetes-training (après l’avoir recupéré sur votre github) et copiez vos manifests à l’interieur

 

• Enfin, poussez ce dossier sur github afin de conservez tous vos fichiers 