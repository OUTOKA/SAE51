# Synthèse collecte et traitement des logs de fonctionnement


### Récupération des logs:

$ tail -f /var/log/nginx/access.log
$ tail -f /var/log/syslog

limiter le nb de logs (5 dans ce cas):

$ tail -n 5 /var/log/syslog

filtrer les logs:

$ grep "erreur" /var/log/syslog

### Utiliser des outils de visualisation de logs

- Logwatch : Un outil de surveillance de logs qui peut être configuré pour envoyer des rapports par e-mail avec les informations les plus pertinentes.

- ELK Stack : L'acronyme d'Elasticsearch, Logstash et Kibana. Ces outils fonctionnent ensemble pour collecter, indexer et visualiser les logs de manière centralisée. 

### How to View Systemd Logs and What a User might find there

    journalctl to view all logs.
    journalctl -u [service_name] to view logs specific to a particular service.
    journalctl -b to view logs from the current boot.
    journalctl –since “YYYY-MM-DD HH:MM:SS” to filter logs by a specific time range.
