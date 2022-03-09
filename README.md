###################################################################################
how to run project in clusters
###################################################################################

- install docker desktop (https://docs.docker.com/desktop/windows/install/)
- enable kubernetes for docker in (docker settings) (https://andrewlock.net/running-kubernetes-and-the-dashboard-with-docker-desktop/) (system restart required)
- make a docker hub account (https://hub.docker.com/signup)
- install skaffold (https://skaffold.dev/docs/install/)
- istall ingress ngnix (https://kubernetes.github.io/ingress-nginx/deploy/)
- go to host file add suitable host (c:\Windows\System32\Drivers\etc\hosts.) ##eg (127.0.0.1 cheqone.dev) (for windows only)

####################################################################################
create new microservices
####################################################################################

1. Doc for creating new microservice and start that

a) nest new service_name --skip-git

b) Go that newly created service copy Dockerfile run following command
docker build -t docker_user_name/cheq-notification .

c) Push the docker image to docker hub (not mandatory)

d) create the deployment file - (cheq-auth-depl.yaml) for the new microservice in the infra folder

e) create the cluster ip service file for the new microservice in the infra folder

f) add the newly created microservice configuration to the skaffold.yaml file for hot reloading.
