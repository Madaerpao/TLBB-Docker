FROM daald/ubuntu32:trusty
#FROM ubuntu:14.04

WORKDIR /home/tlbb

RUN chmod -R 0777 /home/tlbb

RUN dpkg --add-architecture i386 && apt-get update

RUN apt-get install -y libc6:i386 libncurses5:i386 libstdc++6:i386 unixodbc:i386 unixodbc-dev:i386 libmyodbc:i386 ssh mysql-client ; exit 0

# If x64
#RUN apt install -f -y ; exit 0
#RUN rm -r /usr/share/libtool/libltdl/Makefile.in
#RUN apt install -f -y

ADD ./config/odbc.ini /etc/odbc.ini

EXPOSE 7384 12680 22
CMD ["tail","-f","/dev/null"]

RUN sudo chmod -R 0777 /home/tlbb/Server/* ; exit 0
