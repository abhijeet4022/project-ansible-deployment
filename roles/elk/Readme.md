# To clean up old elasticsearch
sudo systemctl stop elasticsearch
sudo systemctl disable elasticsearch
sudo yum remove -y  elasticsearch
sudo rm -rf /etc/elasticsearch
sudo rm -rf /var/log/elasticsearch
sudo rm -rf /var/lib/elasticsearch
sudo rm -rf /usr/share/elasticsearch
sudo rm -f /etc/elasticsearch/elasticsearch.keystore
sudo rm -f /var/run/elasticsearch/elasticsearch.pid
sudo systemctl daemon-reload
sudo rm -f /etc/systemd/system/elasticsearch.service
sudo rm -f /etc/elasticsearch/elasticsearch.keystore
sudo rm -rf /var/lib/elasticsearch/*
sudo rm -rf /tmp/output
