FROM node:12
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./
RUN set NODE_OPTIONS=--max_old_space_size=4096
RUN npm ci 
# Bundle app source
COPY . .
EXPOSE 8180
CMD [ "npm", "run", "prod" ]