FROM alpine:latest

# Set a label for the environment (will be overridden during deployment)
ENV ENVIRONMENT="default"
ENV PROJECT_NAME="Main Project"

# Create a simple script that outputs environment info
RUN echo '#!/bin/sh' > /app.sh && \
    echo 'echo "Application running in ${ENVIRONMENT} environment"' >> /app.sh && \
    echo 'echo "Project: ${PROJECT_NAME}"' >> /app.sh && \
    echo 'echo "Container started at $(date)"' >> /app.sh && \
    echo 'echo "Additional environment-specific configuration: ${ENV_CONFIG}"' >> /app.sh && \
    chmod +x /app.sh

# Set the entry point to run our script
ENTRYPOINT ["/app.sh"]
