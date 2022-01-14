# prom_email_notification_ec2_host_down_alertmanager
Prometheus  email notification when ec2 host down using Alertmanager

Steps
=====
1. Install prometheus
2. Install node-exporter
3. Install graphana
4. Install alertmanager

1. Install Prometheus :

Here we are setting up the prometheus on EC2 instance. We can setup it either using the promethues executable or using docker image.
We will follow the way of downloading executable and then will do the configuration as per requirement.

a. Goto "https://github.com/prometheus" and search for prometheus.

        git clone https://github.com/prometheus/prometheus.git
        cd prometheus
        make build
        ./prometheus --config.file=promethues.yml
       
 Open the port 9090 to access the prometheus.
 http://"public_ip:9090"
 
 2. Install node-exporter
 
 To extract the metrics of ec2/linux instance we need to istall node-exporter on that instance, it will fetch the metrics at /metrics endpoint.
 
 
