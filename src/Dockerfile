FROM ubuntu:20.04

COPY . .

RUN apt-get update && \
    apt-get install -y gcc spawn-fcgi libfcgi-dev nginx && \
    rm -rf /var/lib/apt/lists
    
RUN gcc /server/hello.c -o /server/hello.fcgi -lfcgi

RUN echo "#!/bin/bash\nspawn-fcgi -p 8080 -n /server/hello.fcgi &\nnginx -g 'daemon off;'" > start.sh && chmod +x start.sh

CMD ["sh", "./start.sh"] 

USER maganand
USER 0

