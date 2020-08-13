#!make
.DEFAULT_GOAL := dev

install-role:
	ansible-galaxy install -r dependencies.yml  --force

ping:
	ansible all -i inventory/prod.yaml -m ping
	
prod:
	ansible-playbook -i inventory/prod.yaml -K playbook.yml --verbose

dev:
	ansible-playbook -i hosts.ini -K playbook.yml