# BAD Server
The Blockchain for Allocation and Decentralization Group Website

## Usage
Start the containers with `docker-compose start`

Navigate to [127.0.0.1:8000](http://127.0.0.1:8000/)

## Installation
Requires Docker and docker-compose
```bash
git clone https://github.com/PhilipConte/badserver
cd badserver
echo "BAD_DEBUG=1
BAD_SECRET_KEY=super_secure_tm" > .env
docker-compose up -d
docker-compose exec web python manage.py makemigrations
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
```