# Mapr / Ezmeral 
Distribution MapR - Monitoring d’Hadoop et de certains services avec Sensu

# Description

Ce projet consiste à déployer et configurer un cluster Hadoop avec MapR en utilisant Ansible. L'installation comprend un minimum de trois nœuds Hadoop et un nœud edge. Le déploiement est automatisé avec des playbooks Ansible qui gèrent l'installation et la configuration des services tels que Hive, Drill et MapR-DB. De plus, Sensu est configuré pour surveiller le cluster, y compris les services comme HiveServer2, JobHistoryServer et CLDB.

# Documentation
<ul>
<li><a href="https://docs.sensu.io/sensu-go/latest/operations/deploy-sensu/install-sensu/">Documentation officielle : instalation Sensu</a></li>
<li><a href="https://docs.sensu.io/sensu-go/latest/observability-pipeline/observe-process/populate-metrics-influxdb/">Documentation officielle : Rassembler des métriques avec un contrôle Sensu</a></li>
