# intermediate-frontend

# AXL semantic html.
# accessability
# seo
# ARIA roles
# validation

<!-- tailwind css -->
In your current working directory, create a file and name tailwind.config.js
<!-- Add the following code to it: -->

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
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