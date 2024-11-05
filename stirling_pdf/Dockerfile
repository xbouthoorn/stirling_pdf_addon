# Use the frooodle/s-pdf image as the base
FROM frooodle/s-pdf:latest

# Install Tini
RUN apk add --no-cache tini

# Copy the run.sh script into the container
COPY run.sh /run.sh
RUN chmod +x /run.sh

ENTRYPOINT ["tini", "--", "/scripts/init.sh"]

CMD ["java", "-Dfile.encoding=UTF-8", "-jar", "/app.jar"]

