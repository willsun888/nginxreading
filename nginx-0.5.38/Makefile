
build:
	$(MAKE) -f objs/Makefile

install:
	$(MAKE) -f objs/Makefile install

clean:
	rm -rf Makefile objs

upgrade:
	/Users/willsun/code/nginx-0.5.38/build//sbin/nginx -t

	kill -USR2 `cat /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid`
	sleep 1
	test -f /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid.oldbin

	kill -QUIT `cat /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid.oldbin`

upgrade1:
	# upgrade 0.1.x to 0.2+

	/Users/willsun/code/nginx-0.5.38/build//sbin/nginx -t

	cp /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid.oldbin

	kill -USR2 `cat /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid`
	sleep 1
	test -f /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid.oldbin

	cp /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid.newbin

	kill -QUIT `cat /Users/willsun/code/nginx-0.5.38/build//logs/nginx.pid.oldbin`
