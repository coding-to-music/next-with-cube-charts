# next-with-cube-charts

# 🚀 Javascript full-stack 🚀

https://github.com/coding-to-music/next-with-cube-charts

https://next-with-cube-charts.vercel.app

By SHADID HAQUE https://github.com/Shadid12

https://mydashboard-ten.vercel.app/

https://cube.dev/blog/building-nextjs-dashboard-with-dynamic-charts-and-ssr

https://github.com/Shadid12/next-with-cube

## Example setting up Cube

https://cube.dev/blog/building-nextjs-dashboard-with-dynamic-charts-and-ssr

Create a new .env.local file in the root directory of your project. Add the following environment variables.

```
# .env
NEXT_PUBLIC_CUBEJS_API_URL='<Your-Cube-API-Endpoint>'
NEXT_PUBLIC_CUBEJS_TOKEN='Your-Cube-Token'
```

You can find the Cube API endpoint from the Cube dashboard. Navigate to Settings from the Cube dashboard. There is a field called Cube.js API in the overview tab. Copy the url from there and add it to your .env

We will also need to generate a Cube token to connect to Cube Cloud from our Next.js application. Please Select the Env vars tab in your Settings and copy the CUBEJS_API_SECRET value.

With this secret, we can generate a JWT token. You can run the following node script to generate a JWT token.

```
// file get-jwt-token.js
// npm install jsonwebtoken

// run via
// node get-jwt-token.js

const jwt = require("jsonwebtoken");
// const CUBE_API_SECRET = "<Secret>";
const CUBE_API_SECRET =

const cubejsToken = jwt.sign({}, CUBE_API_SECRET, { expiresIn: "30d" });

console.log(cubejsToken);
```

## Environment Values

```java
  process.env.NEXT_PUBLIC_CUBEJS_TOKEN,
  { apiUrl: process.env.NEXT_PUBLIC_CUBEJS_API_URL }

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/next-with-cube-charts.git
git push -u origin main
vercel --prod --confirm

# vercel env add
```

## Getting started

Follow this tutorial to learn about the implementation of this demo application.
