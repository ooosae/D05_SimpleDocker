P = $(CURDIR)

build:
	sudo docker build -t my-nginx-server:latest .
	sudo docker images

run:
	sudo docker run -p 80:81 -v $(P)/nginx/nginx.conf:/etc/nginx/nginx.conf my-nginx-server:latest

