# Prise en main

Telechargement du fichier de test dataset

[Kaggle Dataset](https://www.kaggle.com/datasets/eliasdabbas/web-server-access-logs)

[GoAccess Officiel](https://goaccess.io/)

[GoAccess GitHub](https://github.com/allinurl/goaccess)

Commande de base trop longue si le fichier est trop gros
```bash
cat access.log | docker run --rm -i -e LANG=$LANG allinurl/goaccess -a -o html --log-format COMBINED - > report.html
```

Commande dev pour test sur 1 jour
```bash
cat access.log | docker run --rm -i -e LANG=$LANG allinurl/goaccess -a -o html --log-format COMBINED - > report.html
```

```bash
head -n 1000000 access.log | docker run --rm -i -e LANG=$LANG allinurl/goaccess -a -o html --log-format COMBINED - > report.html
```

Démarrer docker
```bash
docker compose up -d
```

Démarrer apache dans docker
```bash
docker exec live-php8-1 apachectl start
```
