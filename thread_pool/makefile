httpserver: web_main.o http_conn.o
	g++ web_main.o http_conn.o -lpthread -o httpserver

web_main.o: locker.h threadpool.h http_conn.h web_main.cpp
	g++ -c web_main.cpp -o web_main.o

http_conn.o: http_conn.h http_conn.cpp
	g++ -c http_conn.cpp -o http_conn.o

clean:
	rm -f httpserver web_main.o http_conn.o