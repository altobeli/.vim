# 2 Way Text API
(Requires docker)

#### Setup 

```
make 
```

(You can run the commands from the Makefile manually, if you don't have access to make :)


Start up:

```
make up
```

Health checks (Api and Websocket server):

```
curl localhost:5000/admin/health
curl -k https://localhost:4000/admin/health
```

#### Test

Unit Test
```
npm install
npm test
```

Load Test
```
npm run loadtest <connectionCount>
```

#### Example Usage


Post a Message

```
curl -d '{ "businessId":106000139, "cellPhone":"5106522858","customerId":"3", "shortCode":"50292","message" : "I can not make it"}' -X POST  -H "Content-Type: application/json" http://127.0.0.1:5000/message/save
```

#### CI Integration Suite

After starting the services via ```make up``` (see above),
run the integration suite:
```
make ci
```
# .vim
