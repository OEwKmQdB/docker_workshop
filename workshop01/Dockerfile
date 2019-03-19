FROM node:latest

ENV DB_HOST=mydb DB_PORT=3306
ENV DB_USER=root DB_PASSWORD=changeit
ENV APP_DIR=/app APP_PORT=3000

WORKDIR ${APP_DIR}

# Add Statements
ADD config config
ADD public public
ADD views views
ADD package-lock.json .
ADD package.json .
ADD main.js .

# Install Libs
RUN npm install

# Expose Port
EXPOSE 3000

# Run Application
CMD ["node", "main.js"]