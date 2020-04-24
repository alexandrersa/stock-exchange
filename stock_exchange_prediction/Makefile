.PHONY: setup local_setup run

setup:
	pip install --upgrade pip
	pip install -r requirements.txt

local_setup:
	pip install --upgrade pip
	pip install -r requirements-local.txt
	cp -Rvf local.env .env

run:
	@docker-compose up -d
	python manage.py migrate
	python manage.py makemigrations
	python manage.py runserver
