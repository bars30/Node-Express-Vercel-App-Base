## A base code for a Node Express app hosted on Vercel, free of any errors. The 404 and 500 errors from Vercel have been resolved.

🔴1️⃣If you are using local host for just in cmd writing "node index.js" --> 💠uncomment this part // Start the server
30 // app.listen(PORT, () => {
31 //     console.log(`Server is running on http://localhost:${PORT}`);
32 // });  
🔸and comment this part 
36// Export the Express app as a serverless function
37// module.exports = app;

💠 But if you it will use in Vercel then you need to comment this part 

30 // Start the server
31 // app.listen(PORT, () => {
32 //     console.log(`Server is running on http://localhost:${PORT}`);
// });
🔸and uncomment this part 
36 // Export the Express app as a serverless function
37 module.exports = app; 
|💀|| If you will don't to this you will git error, in local you will can't to node index js, in vercel you will have error 500

〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
🔴🔴🔴Vercel 404 Error🔴🔴🔴

🖍️ For don't getting Vercel 404 error, your vercel.json need to be like this ->
{
 "version":2,
 "builds": [
   { "src": "*.js", "use": "@vercel/node" }
 ],
 "routes": [
     {
       "src": "/(.*)",
       "dest": "/"
     }
 ]
}


〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️〰️
🔴🔴🔴Vercel 500 Error🔴🔴🔴

🖍️For this do the first point in 3 line (in this read.me file)
🖍️Also you need in Vercel 404 & 505 error time to this
Check package.json:

Open your package.json file and ensure that express is listed under the dependencies section. If it's not, you need to add it.
{
  "dependencies": {
    "express": "^4.x.x"  // Add this line if it is missing
  }
}

That's very important







