FROM frooodle/s-pdf:latest

# Install Tini
RUN apk add --no-cache tini

# Copy the run.sh script
COPY run.sh /run.sh
RUN chmod +x /run.sh

# Use Tini as the entrypoint
ENTRYPOINT ["/sbin/tini", "--"]

# Set the default command
CMD ["/run.sh"]
