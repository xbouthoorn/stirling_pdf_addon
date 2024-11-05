ARG BUILD_FROM
FROM frooodle/s-pdf:latest

# Expose the application port
EXPOSE 8080

# Copy the run script
COPY run.sh /run.sh
RUN chmod a+x /run.sh

# Set the default command
CMD [ "/run.sh" ]
