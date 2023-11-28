

setup_dir:
	mkdir -p ${CURDIR}/data/sonarqube/data
	mkdir -p ${CURDIR}/data/sonarqube/extensions
	mkdir -p ${CURDIR}/data/sonarqube/logs

compose-up:
	make setup_dir
	sudo docker compose up -d

compose-down:
	sudo docker compose down

compose-up-build:
	sudo docker compose up --build
