FROM node:8 
MAINTAINER dharma
WORKDIR /app
#below command will copy all the code to this nodeimage in app
COPY . .
#to run and and complie the code
RUN npm install express
RUN npm install
EXPOSE 8080
# to run the container
CMD ["npm","start"]
