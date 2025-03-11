FROM python:3.9-slim

# Set a label for the environment (will be overridden during deployment)
ENV ENVIRONMENT="default"
ENV PROJECT_NAME="Project B"

# Create app directory
WORKDIR /app

# Create a simple script
RUN echo 'import os' > app.py && \
    echo 'from datetime import datetime' >> app.py && \
    echo "print(f\"{os.environ.get('PROJECT_NAME')} running in {os.environ.get('ENVIRONMENT')} environment\")" >> app.py && \
    echo "print(f\"Container started at {datetime.now().isoformat()}\")" >> app.py && \
    echo "print(f\"Additional environment-specific configuration: {os.environ.get('ENV_CONFIG')}\")" >> app.py

# Set the entrypoint
ENTRYPOINT ["python", "app.py"]
