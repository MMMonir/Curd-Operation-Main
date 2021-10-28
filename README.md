## Curd Operation
### First steps for Backend:
```	npm init -y
	npm install express --save
	npm i express cors mongodb
	npm install -g nodemon
```

- How to ignore upload node_modules
```	Create a file named: gitignore
	and save node_modules
```

- How to auto run Backend
```	package.json > sctipt
	"start": "node index.js",
	"start-dev": "nodemon index.js",
```

- Backend index.js main configuration:
```	
	const express = require('express');
	const cors = require('cors');
	const app = express();
	const port = process.env.PORT || 5000;

	app.use(cors());
	app.use(express.json());
	app.get('/', (req, res) => {
	    res.send('Running my server')
	});
	app.listen(port, () =>{
	    console.log('Running server on port', port)
	});
```