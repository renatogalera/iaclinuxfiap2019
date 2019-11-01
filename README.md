# iaclinuxfiap2019

NAC20 Elder Pereira Fiap 2019 

Provisioning via Docker-compose Mediawiki - Prometheus - Alerta - Alertmanager.

Alerta 
https://github.com/alerta/prometheus-config

Requirements
#Linux Redhat family and Ansible

#Install
```
git clone https://github.com/renatogalera/iaclinuxfiap2019.git
```

#Run
```
ansible-playbook main.yml -e "hostname=NAMEORIPSERVER"
```

Containers
```
mediawiki
mariadb for grafana and mediawiki
grafana
prometheus
alerta
alertmanager
nodeexport
mysqlexport
collectd
mongodb
haproxy
```

Domains (example) on haproxy
```
http://grafana
http://prometheus
http://alerta
http://alertmanager
```
For example, edit /etc/hosts in client machine.

Functions
```
Grafana deploy every 10 seconds dashboards by provisoning function
Prometheus connect mysql_exporter, collect_exporter, node_exporter, haproxy2_exporter
Container ports restricted by internal network
Alerta is very simple web notification for alertmanager/prometheus
```


