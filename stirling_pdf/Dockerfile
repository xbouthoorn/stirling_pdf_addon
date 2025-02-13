# Use the frooodle/s-pdf image as the base
FROM frooodle/s-pdf:latest-fat

# Install Tini to manage processes
RUN apk add --no-cache tini

# Copy and make the run.sh script executable
COPY run.sh /run.sh
RUN chmod +x /run.sh

# Use Tini as the entrypoint to handle processes
ENTRYPOINT ["tini", "--"]

# Expose ingress port
EXPOSE 8099

# Run Stirling-PDF through the copied run.sh script
CMD ["/run.sh"]
