To host frontend and backend separatly on vercel i hosted 

noteapp/
      -->frontend
      --> backend/
                 packages.json
                  .env 
                  & remove that app.lesten instead should be " module.exports = app;"
                   while hosting on vercel
                  root directory will be backend (folder)
                  Build command should be empty 
                  output directory empty
                  npm install
                  and add vercel.json to backend same path as server.js
                  vercel.json
 ```
{
  "version": 2,
  "builds": [
    {
      "src": "backend/server.js",
      "use": "@vercel/node"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "backend/server.js"
    }
  ]
}
```


after this the backend will on live 

IN frontend just change the 
http:localhost:5000/api/notes to https://noteapp-dazeou3a0-anwarhackers-projects.vercel.app/api/notes 
like this 


and i got an error because the vercel by default it treat or make our project to private or apply protection 
So

 in vercel dashnoard --> settings --> development protection --> all projects are available then like to 3 dots to particular project and to --> view project settings 

simply deseable --> Vercel Authentication and try again 


//

https://chatgpt.com/c/690731f3-fb10-8323-bdc8-4617f6e73d79

//
