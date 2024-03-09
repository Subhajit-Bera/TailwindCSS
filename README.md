# Tailwind CSS : Tailwind CLI
 
## Steps for setup Tailwind:
### Prerequisite :
 Need to have Node.js installed in the system </br>
Inside root folder 
* npx tailwindcss init : It will create tailwind.config.js file
* tailwind.config.js :
 ```
 /** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./dist/index.html"],  -> we had to put the destination,where tailwind is applied
  theme: {
    extend: {},
  },
  plugins: [],
}
```
* Inside input.css : use this code
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

* Tailwind css is actually being generated from input.css file
So we have to run this command :
```
npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch
```
-i : we have to provide the destination of input.css file </br>
-o : we have to provide the output destination where we want to generate our css.We can also provide the name of the generated css file :      ./dist/css_filename.css : here the file name given is style.css after that we had to link it with .html file (here index.html)

## Folder Structure
```
root/
|── |dist/
│   ├── index.html  
│   ├── style.css 
├── src/
│   ├── input.css
├── tailwind.config.js
```
