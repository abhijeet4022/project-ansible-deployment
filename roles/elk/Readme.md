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

-------------------------------------------------------------------------------
Authentication and authorization are enabled.
TLS for the transport and HTTP layers is enabled and configured.

The generated password for the elastic built-in superuser is : cwW5lfWCz1mAX0zhmUCz

If this node should join an existing cluster, you can reconfigure this with
'/usr/share/elasticsearch/bin/elasticsearch-reconfigure-node --enrollment-token <token-here>'
after creating an enrollment token on your existing cluster.

You can complete the following actions at any time:

Reset the password of the elastic built-in superuser with
'/usr/share/elasticsearch/bin/elasticsearch-reset-password -u elastic'.

Generate an enrollment token for Kibana instances with
'/usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana'.

Generate an enrollment token for Elasticsearch nodes with
'/usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s node'.
