# 
# each single docker engine should run only one Dozzle container (agent or master)
#  
# SELECT one of the following options:

setup_dir:
	mkdir -p ${CURDIR}/data

docker-agent-up:
	make setup_dir
	sudo docker compose up -d dozzle-agent

docker-agent-down:
	sudo docker compose down dozzle-agent


docker-master-up:
	make setup_dir
	sudo docker compose up -d dozzle

docker-master-down:
	sudo docker compose down dozzle
