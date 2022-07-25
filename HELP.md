set an environmental variable called HOST_IP that 
has the host's IP address

https://stackoverflow.com/questions/51147929/marathon-on-mesos-failed-to-update-resources-for-container
https://issues.apache.org/jira/browse/MESOS-5544

marathon-lb: https://github.com/mesosphere/marathon-lb

haproxy https://archive-docs.d2iq.com/mesosphere/dcos/services/marathon-lb/1.13/mlb-reference/

docker run -P -e "PORTS=10000" mesosphere/marathon-lb:latest poll -m http://master.mesos:8080 --health-check --group external

--add-host=host.docker.internal:host-gateway https://medium.com/@TimvanBaarsen/how-to-connect-to-the-docker-host-from-inside-a-docker-container-112b4c71bc66
