• Ecrivez un manifest pod.yml pour déployer un pod avec l’image mmumshad/simple-webapp-color en précisant que la color souhaitée est la rouge

• Lancez votre pod et vérifiez qu’il est bien en cours d’exécution

• Exposez votre pod en utilisant la commande kubectl port-forward <nom de votre pod> 8080:8080 --address 0.0.0.0

• Vérifiez que l’application est bien joignagle en ouvrant le port 8080 de votre node

• Ecrivez un manifest nginx-deployment.yml pour déployer 2 replicas d’un pod nginx (en version 1.18.0)

• Lancez de deployment, vérifier le nombre de pods et vérifiez que le deployment et le replicaset (ainsi que la version de l’image utilisée) ont été créé

• Modifiez le fichier nginx-deployment.yml afin d’utiliser l’image nginx en version latest, appliquer la modification (kubectl apply)

• Que se passe t’il ? Combien de replicasets avez-vous ? Quelle est l’image utilisée par le replicaset en cours d’utilisation ?

• Supprimez toutes les ressources créées et recréez les en utilisant les commandes impératives

• Créez un repertoire Kubernetes-training et un sous-dossier tp-2 et copiez vos manifests à l’interieur

• Enfin, poussez ce dossier sur github afin de conservez tous vos fichiers 
