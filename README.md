### Install System ###
ansible-playbook -i hosts sys.yml --limit eth-node


### Provisioning Nomad ###
ansible-playbook -i hosts nomad.yml --limit eth-node 


### Building Docker images: ###
cd docker && docker build . -t studzvg/erigon:07092021  -f Dockerfile_erigon && docker build . -t studzvg/erigon_rpcdaemon:07092021 -f Dockerfile_rpcdaemon

