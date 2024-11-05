ARG BUILD_FROM
FROM $BUILD_FROM

# Install dependencies
RUN apk add --no-cache \
    python3 \
    py3-pip \
    git

# Install Stirling-PDF
RUN pip3 install stirling-pdf

# Set working directory
WORKDIR /data

# Copy and make the run.sh script executable
COPY run.sh /
RUN chmod a+x /run.sh

# Expose the application port
EXPOSE 8080

# Run the script
CMD [ "/run.sh" ]
