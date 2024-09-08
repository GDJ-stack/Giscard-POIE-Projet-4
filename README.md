# Mapr / Ezmeral 
Distribution MapR - Monitoring d’Hadoop et de certains services avec Sensu

# Description

Ce projet consiste à déployer et configurer un cluster Hadoop avec MapR en utilisant Ansible. L'installation comprend un minimum de trois nœuds Hadoop et un nœud edge. Le déploiement est automatisé avec des playbooks Ansible qui gèrent l'installation et la configuration des services tels que Hive, Drill et MapR-DB. De plus, Sensu est configuré pour surveiller le cluster, y compris les services comme HiveServer2, JobHistoryServer et CLDB.

# Arboresce du projet 

└── mapr
    ├── LICENSE
    ├── README.md
    ├── ansible
    │   ├── add_services.yml
    │   ├── ansible.cfg
    │   ├── ansible_setup_passwordless_ssh.yml
    │   ├── configure_agent_sensu.yml
    │   ├── configure_sensu_backend.yml
    │   ├── configure_sensuctl.yml
    │   ├── deploy_mapr.yml
    │   ├── initialise_sensu.yml
    │   ├── install_agent_sensu.yml
    │   ├── install_ansible.yml
    │   ├── install_sensu.yml
    │   ├── inventory.ini
    │   ├── inventory_creation.sh
    │   ├── manip.md
    │   ├── mapr_cluster_setup
    │   │   |
    │   │   ├── defaults
    │   │   │   └── main.yml
    │   │   |
    │   │   │   
    │   │   ├── handlers
    │   │   │   └── main.yml
    │   │   ├── meta
    │   │   │   └── main.yml
    │   │   ├── tasks
    │   │   │   ├── attach_disks.yml
    │   │   │   ├── check_service_up.yml
    │   │   │   ├── configure_cluster.yml
    │   │   │   ├── main.yml
    │   │   │   ├── modify_config_file.yml
    │   │   │   ├── start_cluster.yml
    │   │   │   ├── upload_license.yml
    │   │   │   └── validation_test.yml
    │   │   ├── tests
    │   │   │   ├── inventory
    │   │   │   └── test.yml
    │   │   └── vars
    │   │       └── main.yml
    │   ├── mapr_configuration
    │   │   |
    │   │   ├── defaults
    │   │   │   └── main.yml
    │   │   ├── files
    │   │   │   └── maprgpg.key
    │   │   ├── handlers
    │   │   │   └── main.yml
    │   │   ├── meta
    │   │   │   └── main.yml
    │   │   ├── tasks
    │   │   │   ├── add_repository_credential.yml
    │   │   │   ├── create_user_group.yml
    │   │   │   ├── get_license.yml
    │   │   │   ├── install_mapr_services.old.yml
    │   │   │   ├── install_mapr_services.yml
    │   │   │   ├── install_utilities.yml
    │   │   │   ├── main.yml
    │   │   │   ├── open_port.yml
    │   │   │   └── update_hosts.yml
    │   │   ├── template_inventory
    │   │   └── vars
    │   │       └── main.yml
    │   ├── restart_history_server.yml
    │   ├── start_cluster.yml
    │   └── start_sensu_backend.yml
    ├── instructions.txt
    └── vagrant
        ├── config.yml
        ├── setup_ansible_user.sh
        └── vagrantfile

# Documentation
<ul>
<li><a href="https://docs.sensu.io/sensu-go/latest/operations/deploy-sensu/install-sensu/">Documentation officielle : instalation Sensu</a></li>
<li><a href="https://docs.sensu.io/sensu-go/latest/observability-pipeline/observe-process/populate-metrics-influxdb/">Documentation officielle : Rassembler des métriques avec un contrôle Sensu</a></li>
