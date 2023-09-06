
Ecrivez un manifest namespace.yml qui crée un namespace nommé production et lancez la création de ce namespace à partir du manifest

• Toutes vos prochaines ressources doivent être créées dans le namespace production

• Ecrivez un manifest pod-red.yml pour déployer un pod avec l’image mmumshad/simple-webapp-color en précisant que la color souhaitée est la rouge (red), le pod doit posseder le label « app: web »

• Ecrivez un manifest pod-blue.yml pour déployer un pod avec l’image mmumshad/simple-webapp-color en précisant que la color souhaitée est la bleue (blue) le pod doit posseder le label « app: web »

• Lancez la création des deux pods

• Ecrivez un manifest service-nodeport-web.yml qui permettra exposer les pods via un service de type node port, le nodeport devra être le 30008 et les target les ports 8080 de nos pods dont le label est « app: web »

• Lancez la création du service et vérifiez qu’il trouve les deux pods (champ endpoint en utilisant la commande kubectl describe)

• Vérifiez que l’application est bien disponible en ouvrant le port 30008 de votre nœud

--------

 création de manifests à l'aide de la commande impérative 

kubectl create deployment --image=nginx nginx  --dry-run=client -o yaml > nginx.yaml


• Créez un repertoire tp-3 dans Kubernetes-training (après l’avoir recupéré sur votre github) et copiez vos manifests à l’interieur

• Enfin, poussez ce dossier sur github afin de conservez tous vos fichiers 


https://devopssec.fr/article/gerer-manipuler-namespaces-et-resourcequotas-kubernetes