# intermediate-frontend

# AXL semantic html.

# accessability

# seo

# ARIA roles

# validation

<!-- tailwind css -->

In your current working directory, create a file and name tailwind.config.js

<!-- Add the following code to it: -->

/** @type {import('tailwindcss').Config} \*/
module.exports = {
content: ["./src/**/\*.{html,js}"],
theme: {
extend: {},
},
plugins: [],
}

1. Create a directory src inside of 2. your current working directory
2. Create a file called input.css inside src
3. Inside the file add the following code:

@tailwind base;
@tailwind components;
@tailwind utilities;

4. IN THE TERMINAL RUN THIS TO CREATE YOUR OUTPUT.CSS
   npx tailwindcss -i ./src/input.css -o ./src/output.css --watch

# css preprocessors

What is SASS/SCSS? SASS (Syntactically Awesome Style Sheets) and SCSS (Sassy CSS) are popular CSS preprocessors that add powerful features to CSS.

hey allow developers to write code that is more:

- maintainable,
- scalable, and
- readable
  by introducing:

  # variables, nesting, modules, mixins, and more.

  # variables

      They are declared using the $ symbol.

      $primary-color: #333;$font-stack: Helvetica, sans-serif;

      body {
      font: 100% $font-stack;
      color: $primary-color;
      }
  # netsings
  Nesting enables you to write CSS rules in a hierarchical structure that mirrors the HTML structure, improving readability and organization.

  nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}

# Mixins
Mixins allow you to create reusable chunks of CSS. You can pass arguments to mixins to make them more flexible.

@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, 0.25);
  color: #fff;
}

.info {
  @include theme;
}
.alert {
  @include theme(DarkRed);
}
Functions 

# functions
SASS functions let you perform calculations and return values. They are useful for creating dynamic styles.

@function double($number) {
  @return $number * 2;
}

.box {
  width: double(20px);
}

# Partials and Import
# Partials 
1. Partials are small SASS files that contain snippets of CSS. They are useful for organizing styles into modular, reusable pieces. A partial file name begins with an underscore (e.g., _variables.scss).

2. Importing Partials You can import partials into your main SASS file using the @use or @import rule to keep your styles organized.  

// styles.scss
@use 'variables';
@use 'mixins';

body {
  font: 100% variables.$font-stack;
}

# Compiling SASS/SCSS

Tools for Compiling

To use SASS/SCSS, you need to compile it into standard CSS. This can be done using command-line tools, task runners, or build systems like:

1. Command Line: sass input.scss output.css
2. Watching Files: sass --watch input.scss:output.css
3. Build Tools: Webpack, Gulp, or Grunt

<!-- installing sass -->
npm install sass -v 3.7.4