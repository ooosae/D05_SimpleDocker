P = $(CURDIR)

all: hello.c
	gcc -o hello.fcgi hello.c -lfcgi
go:
	spawn-fcgi -p 8080 -n hello.fcgi
nginx:
	sudo nginx -c $(P)/nginx.conf
clean:
	sudo systemctl stop nginx
