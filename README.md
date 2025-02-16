# LogGate
An micro service for storing/searching logs, create an app, invoke endpoint with token, which includes appId, iat. review logs

Goal: made to store the logs in db/local for later debugging purpose

## How it work

- Visit the service with proper credential (user:root, pass:toor)
- You will see a `+ADD` button which will open a new page if clicked, That new page will have a form
  - Log store life : 30days, 90days, forever
  - Service Name: My New App
  - Notification: enabled/disabled
- You will see all the already created services just below the `+ADD` button which will open a new page if clicked and will show more details of the clicked service
  - You can update the service
  - You can delete the service
  - You can view the logs and perform searches
  - You can activate/deactivate the service
  - You can clear the logs manually

## Dependencies

- Typescript
- ngRok
- rabbitMQ
- MongoDB
- Express
- NodeJs
- Redis
- Socket.IO
- Handlebars

## Todo

- [ ] Create a simple express application with basic handlebars included within docker image
- [ ] Add socket.io and redis.io to the docker
- [ ] Create Routes for handling logics for creating app to receiving logs
- [ ] Create workflow and deploy on render

## Endpoints

- [POST] /log/push `{ token: jwt }`

## Open Source

You are free to contribute into this repository. just create a pull request
