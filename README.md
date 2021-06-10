# Tailwind CSS Starter template


# Tailwindcss Installation guide

Please refer the following urls.

https://themesberg.com/blog/tailwind-css/tutorial
https://tailwindcss.com/docs/installation

## Install Tailwind via npm

npm init

npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

## Add Tailwind as a PostCSS plugin

// postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}

## Create your configuration file

npx tailwindcss init

// tailwind.config.js
module.exports = {
  future: {},
  purge: [],
  theme: {
  extend: {},
  },
  variants: {},
  plugins: [
    require('tailwindcss'),
    require('autoprefixer'),
  ]
}

## Adding Tailwind to your CSS

To do this, create a new CSS file called main.css (or any other preferred name) and add the following lines of code inside it:

@tailwind base;

@tailwind components;

@tailwind utilities;


## Processing your CSS with Tailwind

npx tailwindcss build main.css -o output.css

## Reduce loading time and file size by purging the unused classes from your CSS

Add the following line of code to your configuration file:
    
purge: {
  enabled: true,
  content: [
      './**/*.html'
  ]
}
