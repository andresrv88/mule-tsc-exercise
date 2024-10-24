FROM adoptopenjdk/openjdk8

WORKDIR /opt

COPY ./mule-enterprise-standalone-4.8.0 ./mule

RUN chmod -R 777 ./mule/bin/

VOLUME ["./mule/bin","./mule/logs", "./mule/conf", "./mule/apps", "./mule/domains"]

# Copy and install license

#CMD echo "------ Copy and install license --------"

#COPY ./muleLicenseKey.lic ./mule/conf/

#RUN .mule/bin/mule -installLicense .opt/conf/muleLicenseKey.lic

EXPOSE 2310 2311 2312 2313

CMD ["./mule/bin/mule", "-M-Dmule.env=docker"]