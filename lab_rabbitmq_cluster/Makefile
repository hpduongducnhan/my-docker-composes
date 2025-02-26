

setup_dir:
	mkdir -p ${CURDIR}/data

compose-up:
	make setup_dir
	sudo docker compose up -d

compose-down:
	sudo docker compose down

compose-up-build:
	sudo docker compose up --build


join-cluster:
	@docker exec rabbitmq_02 rabbitmqctl stop_app
	@docker exec rabbitmq_02 rabbitmqctl join_cluster rabbit@rabbitmq-01
	@docker exec rabbitmq_02 rabbitmqctl start_app
	@docker exec rabbitmq_03 rabbitmqctl stop_app
	@docker exec rabbitmq_03 rabbitmqctl join_cluster rabbit@rabbitmq-01
	@docker exec rabbitmq_03 rabbitmqctl start_app
	@echo "Cluster setup complete"

check-cluster-status:
	@docker exec rabbitmq_01 rabbitmqctl cluster_status