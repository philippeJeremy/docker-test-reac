FROM node:alpine

USER node

WORKDIR '/home/node'

COPY package.json .

RUN npm install

COPY --chown=node:node . .

CMD ["npm", "start"]

# docker build -t myreact .
# docker run --name react -p 3000:3000 myreact
# docker run --name react --rm -p 3000:3000 --mount type=bind,src="$(pwd)",target=/app --mount type=volume,target=/app/node_modules myreact