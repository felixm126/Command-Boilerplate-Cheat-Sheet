# Command-Boilerplate-Cheat-Sheet
<h3>CSS/JS/AXIOS link</h3>

link href="style.css" rel="stylesheet"/

<script src="https://unpkg.com/axios/dist/axios.min.js"> </script> <br>
<script defer src="script.js"> </script>

<h3>MONGOOSE</h3>
npm install mongoose <br>
mkdir db models seed <br>
touch db/index.js models/{publisher,book,index}.js seed/{publishers,books}.js <br>
**publihser & book name can change**

<h3>EXPRESS</h3>
npm init -y <br>
npm install express <br>
(need to install project by project basis)

<h3>NODEMON</h3>
npm install nodemon --save-dev <br>
(need to install project by project basis) <br>
<br>
Npm run dev (running server)

<h3>**BOILERPLATES**</h3>

<h3>MONGOOSE</h3>

db/index.js page: <br>
const mongoose = require('mongoose') <br>
<br>
mongoose
    .connect('mongodb://127.0.0.1:27017/booksDatabase') <br>
    .then(() => { <br>
        console.log('connected!') <br>
    }) <br>
    .catch((e)=> { <br>
        console.error('error!', e.message) <br>
    }) <br>
<br>
mongoose.set('debug', true) <br>
<br>
const db = mongoose.connection <br>
<br>
module.exports = db <br>


<h3>EXPRESS</h3>

<bold>Server page: </bold> <br>
const express = require('express') <br>
const cors = require('cors') <br>
<br>
const PORT = process.env.PORT || 3001 <br>
<br>
const app = express() <br>
<br>
<br>
app.use(cors()) <br>
app.use(express.json()) <br>
app.use(express.urlencoded ({extended: false})) <br>
<br>
<br>
app.listen(PORT, () => { <br>
  console.log(`Express server listening on port ${PORT}`)<br>
}) <br>
<br>
app.get('/', (req, res) => { <br>
    res.send("welcome to my page") <br>
  })<br>
<br>
<br>

package.json page: <br>
"start": "node server.js", <br>
"dev": "nodemon server.js" <br>
**add this under "script"

    
<bold> Controller pages: </bold><br>
  module.exports = { <br>
    get1, <br>
    get2, <br>
}
