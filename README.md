# Project to learn about [Sass](https://sass-lang.com/documentation).

## What is Sass? 

<!-- https://sass-lang.com/documentation -->
 > Sass is a stylesheet language that’s **compiled to CSS**.
    It allows you to use `variables`, `nested rules`, `mixins`, `functions`, and more, all with a fully CSS-compatible syntax.
    Sass helps keep large stylesheets well-organized and makes it easy to share design within and across projects.

---

## Introduction

 ### **Sass Syntax**
 
 - Sass contains support for two extensions, and it has different ways of handling these extensions, these are Scss and Sass.
    
    #### Scss

    - This is the **most popular** syntax and this is most easy why contain a syntax **more similar with css**.
    
    - Example:

        ```SCSS
        $defaultColor: #1c1c1c; 
        $defaultFontWeight: 300;
        $titleFontWeight: 600;

        body{
          color: $defaultColor;
          font-weight: $defaultFontWeight;

          h1, h2, h3, h4, h5, h6, .title{
            font-weight: $titleFontWeight;
          }
        }
        ```

    - Result:
        
        ```CSS
        body {
          color: #1c1c1c;
          font-weight: 300;
        }
        body h1, body h2, body h3, body h4, body h5, body h6, body .title {
          font-weight: 600;
        }
        ```
    
    #### Sass
    
    - The `sass` extension is slightly different from the` css` syntax because in `sass` it is not necessary to use "{}" or ":;", only indented syntax is used.

    - Example:

        ```SASS
        $defaultColor: #1c1c1c
        $defaultFontWeight: 300
        $titleFontWeight: 600

        body
          color: $defaultColor
          font-weight: $defaultFontWeight

          h1, h2, h3, h4, h5, h6, .title
            font-weight: $titleFontWeight
        ```

    - Result:
        
        ```CSS
        body {
          color: #1c1c1c;
          font-weight: 300;
        }
        body h1, body h2, body h3, body h4, body h5, body h6, body .title {
          font-weight: 600;
        }
        ```
---

## Install

 - I will install `Sass` with [Npm](https://www.npmjs.com/), but your can [install](https://sass-lang.com/install) from another place.

    #### Install `Npm`

     - `sudo apt update`
     - `sudo apt upgrade`
     - `sudo apt-get install npm`

     - Or you can see other ways to [install](https://www.npmjs.com/get-npm)
     
    #### Installing `Sass` with Npm

     - `npm install -g sass`
     
 - To verify that the installation worked, execute: `sass --version`
   
---
  
## Using

 ### How to compile `Scss\Sass` to `Css`

 - Simple Compile

    - `sass (First parameter is your sass file path) (Second parameter is your css file path)`
    - Example: `sass public/sass/base.sass public/css/style.css`
    
 - Compile using `Watch`

    - Using the `watch` method, sass will check every change in the first file and compile every change made, and is the most pratic.
    - Example: `sass --watch public/sass/base.sass public/css/style.css`
    - To stop file watch, press `Ctrl + C`
    
    
 