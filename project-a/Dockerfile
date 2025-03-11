FROM node:16-alpine

# Set a label for the environment (will be overridden during deployment)
ENV ENVIRONMENT="default"
ENV PROJECT_NAME="Project-A"

# Create app directory
WORKDIR /app

# Create a simple script
RUN echo 'console.log(`${process.env.PROJECT_NAME} running in ${process.env.ENVIRONMENT} environment`);' > index.js && \
    echo 'console.log(`Container started at ${new Date().toISOString()}`);' >> index.js && \
    echo 'console.log(`Additional environment-specific configuration: ${process.env.ENV_CONFIG}`);' >> index.js

# Set the entrypoint
ENTRYPOINT ["node", "index.js"]
