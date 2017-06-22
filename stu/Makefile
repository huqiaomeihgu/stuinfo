CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= add.cgi del.cgi mod.cgi sel.cgi selscore.cgi mod2.cgi add2.cgi sel2.cgi sel3.cgi del2.cgi mod3.cgi del3.cgi

all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi
install:
		cp *.cgi /usr/lib/cgi-bin/sx/
		cp head.html footer.html /usr/lib/cgi-bin/sx/
		sudo cp -r public/ index.html index2.html login.html /var/www/html/
