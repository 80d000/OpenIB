FROM ubuntu:latest
#installing deps 
RUN apt -qy update ; apt -qqy upgrade ; apt -qqy install \ 
	graphicsmagick \ 
	gifsicle \ 
	nginx \	
	php \ 
	php-mysql \ 
	ffmpeg \ 
	php-pear
#nginx runtime
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
	&& ln -sf /dev/stderr /var/log/nginx/error.log
EXPOSE 80
STOPSIGNAL SIGQUIT
ENTRYPOINT ["nginx", "-g", "daemon off;"]
