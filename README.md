# Start NodeJS Express
> Instalação
```
$ npm init
$ npm install express
$ npm install nodemon
```

>package.json
```
...
 "type": "module",
  "scripts": {
    "dev": "nodemon ./src/index.js"
  },
...
```

> index.js
```
import express from ‘express’;
	const app = express();
	app.use(express.json());

	app.get(‘/api/ping’, (request, response) => {
	response.send({
	message: ‘pong’
});
});
	
	app.listen(8000, () => {
		console.log(“Servidor Iniciado na porta 8000!”)
})
```
> npm run dev - iniciar servidor
