FROM node:14

WORKDIR /app

COPY . .

RUN npm install

RUN npm install --force --prefix client

RUN npm run --prefix client build

EXPOSE 5000

CMD ["npm", "start"]

#add .env
#MONGO_URL = connection_link
#NODE_ENV = production
#JWT_SECRET = secret

#build test: 
#docker build -t nutritrack .
#docker run -it -p 5000:5000 nutritrack

#deployment
#change file name to Dockerfile.web
#heroku login
#heroku container:login
#heroku container:push --recursive -a nutritrack
#heroku container:release -a nutritrack web
#heroku open --app nutritrack