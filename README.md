# coltogdyuhg.github.io
<div>
  <label class="toggle-button">
  	<input type="checkbox" class="toggle-checkbox">
    <span class="slider"></span>
    <span class="label label-dark">Dark</span>
    <span class="label label-light">Light</span>
  </label>
</div>

<style>
/* The switch - the box around the circle */
.toggle-button {
    position: relative;
    display: flex;
    width: 200px;
    height: 40px;
    margin: 10px;
    align-items: center;
    justify-content: space-around;
    flex-wrap: nowrap;
    flex-direction: row;
}

.toggle-checkbox {
  display: none;
}

.slider {
  position: absolute;
  top: 0;
  left: 65px;
  width: 80px;
  height: 40px;
  background-color: #ec6838;
  border-radius: 40px;
  transition: background-color 0.2s, transform 0.2s;
}

.slider:before {
  content: "";
  position: absolute;
  top: 4px;
  left: 4px;
  width: 32px;
  height: 32px;
  background-color: white;
  border-radius: 50%;
  transition: transform 0.2s;
}

/* When the checkbox is checked, change the background color and move the circle to the right */
.toggle-checkbox:checked + .slider {
  background-color: #ccc;
  transform: translateX(0px);

}

.toggle-checkbox:checked + .slider:before {
  transform: translateX(40px);

}

/* Label styles */
.label {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 16px;
  font-weight: bold;
  color: #ccc;
  transition: color 0.2s;
  text-align: center;
}

.label-light {
  color: #ccc;
 	right: 0px;
}

.label-dark {
  left: 0px;
  color: #ec6838;
}

.toggle-checkbox:checked + .label-light {
  color: #ccc;
}

.toggle-checkbox:checked + .label-dark {
  color: #fff;
  background-color: #ccc;
}

</style>










proxy list down below      DO NOT SHARE SITE






 http://listings.showmyhomes.com/
http://info.sundby.com/
http://learn.gurdit.com/
http://listed.compuinter.com/
http://education.ldtp.com/
https://edu.estic.org/
https://about.actsministries.org/
https://lxt.surfnet.ca/
https://my-family.photo-frame.com/
https://spanish.awiki.org/

https://utopiaunblocker.com
https://info.angle.twlab.org/
https://class.books.rebro.org/
https://edu.graph.acepod.com/
https://guide.angle.worldcreate.org/
https://ela.plant.wild1.org/
https://core.info.port0.org/

https://algebra.thehorseplace.us/
https://k12.folklandmanagement.com/app
https://info.svmblocker.com/app
https://government.sotna.org/app
https://forest.katieprallphotography....
https://teams.prosports.cl/app
https://en.silentpatriot.com/app
https://help.robot-agachado.net/app
https://edu.worksheetsforteachers.xyz...
https://worksheets.hidict.cn/app
https://derpman.lol/app
https://geoquiz.goncharmaster.ru/app
https://login.cloudbusinessportal.com...
https://edu.mazovec.ru/app
https://go.jaleh.info/app


https://fe.epqg0jw1n4ontfz5hx8yul6wrdut7xg.tk/
https://whywhywhy.deleesportsmedicine.com/  
https://diabetesiscool.sprk.lol/ 
https://kaydenhas4eyes.myddns.me/ 
https://mathup.99berserkers.com/ 
https://pxnguin.vlad.md/  
https://penguin.seburn.net/ 




import express from "express";
import http from "node:http";
import path from "node:path";
import { createBareServer } from "@tomphttp/bare-server-node";
import request from "@cypress/request";

const __dirname = path.resolve();
const server = http.createServer();
const app = express(server);
const bareServer = createBareServer("/bare/");

app.use(express.json());
app.use(
  express.urlencoded({
    extended: true,
  })
);

app.use(express.static(path.join(__dirname, "static")));
app.get('/app', (req, res) => {
  res.sendFile(path.join(__dirname, './static/index.html'));
});
app.get('/student', (req, res) => {
  res.sendFile(path.join(__dirname, './static/loader.html'));
});
app.get('/apps', (req, res) => {
  res.sendFile(path.join(__dirname, './static/apps.html'));
});
app.get('/gms', (req, res) => {
  res.sendFile(path.join(__dirname, './static/gms.html'));
});
app.get('/lessons', (req, res) => {
  res.sendFile(path.join(__dirname, './static/agloader.html'));
});
app.get('/credits', (req, res) => {
  res.sendFile(path.join(__dirname, './static/credits.html'));
});
app.get('/partners', (req, res) => {
  res.sendFile(path.join(__dirname, './static/partners.html'));
});
app.get("/worker.js", (req, res) => {
  request("https://cdn.surfdoge.pro/worker.js", (error, response, body) => {
    if (!error && response.statusCode === 200) {
      res.setHeader("Content-Type", "text/javascript");
      res.send(body);
    } else {
      res.status(500).send("Error fetching worker script");
    }
  });
});
app.use((req, res) => {
  res.statusCode = 404;
  res.sendFile(path.join(__dirname, './static/404.html'))
});

server.on("request", (req, res) => {
  if (bareServer.shouldRoute(req)) {
    bareServer.routeRequest(req, res);
  } else {
    app(req, res);
  }
});

server.on("upgrade", (req, socket, head) => {
  if (bareServer.shouldRoute(req)) {
    bareServer.routeUpgrade(req, socket, head);
  } else {
    socket.end();
  }
});

server.on("listening", () => {
  console.log(`Doge Unblocker @ Port 8000`);
});

server.listen({
  port: 8000,
});






