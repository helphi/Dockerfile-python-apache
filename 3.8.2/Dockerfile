FROM python:3.8.2-buster

ENV LANG=C.UTF-8 TZ=Asia/Shanghai

RUN apt update &&\
    DEBIAN_FRONTEND=noninteractive apt install -y apache2=2.4.38-3+deb10u3 &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/*

RUN echo "AddHandler cgi-script .cgi .pl .py .sh" >>/etc/apache2/mods-available/cgid.conf
RUN ln -s /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/cgi.load &&\
    ln -s /etc/apache2/mods-available/cgid.load /etc/apache2/mods-enabled/cgid.load &&\
    ln -s /etc/apache2/mods-available/cgid.conf /etc/apache2/mods-enabled/cgid.conf

ADD hello.py /usr/lib/cgi-bin/hello.py
RUN chmod +x /usr/lib/cgi-bin/hello.py

EXPOSE 80
CMD ["apache2ctl", "-DFOREGROUND"]
