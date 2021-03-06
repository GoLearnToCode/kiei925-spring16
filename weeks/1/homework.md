# Homework #1: Due Before the Next Class

Please follow these instructions carefully.

**Part A: Preparation**

1. Before doing anything else, read through all of these instructions and jot down how long you estimate it will take you to do this homework. Then keep track of how much time you actually spend on the homework this week.
2. Install the following Chrome Extensions: _ColorZilla_, _JSONView_, and _WhatFont_
1. Draw a wireframe of a simplified version of Etsy.com's home page.  Think about a _minimal home page_, the core offering, and the simplest implementation necessary to gain traction. Take a picture of your wirefame.

**Part B: Build It**

3. Create a new Cloud9 workspace:
  - Name it `hw1`.  
  - You can leave the Description field blank.
  - Use the **Clone from Git** option and specify ```http://github.com/kiei925-winter17/etsy1```
  - Select the **Ruby** template
  - Click "Create Workspace"
2. Once inside the `hw1` project, go to the Terminal window and run this command: `bundle install`
3. Replace the built-in home page with your own code, based on your wireframe (see hints below).  Try to match the fonts and colors that you see on the real Etsy.com website. Your finished HTML does not need to exactly match your wireframe.
3. Upload your wireframe photo into your project as `wireframe.png` (or some other image format).
4. Somewhere on your home page, use HTML to display your estimate and actual time; for example:
``` html
<p><small>I originally estimated 2 hours. It actually took me 12 hours.</small></p>
```
Of course, use your own values instead of the numbers shown above.  Your grade does NOT depend on your estimate vs. actual time.  It is for your information only.

**PART C: Turn It In**
4. Share your workspace with Garrett. Click the "Share" button at the top of your workspace, and enter his username: `garrettqmartin8`.  If it's not obvious how to do that, [watch this quick video](https://docs.c9.io/docs/share-a-workspace).


**GRADING**

- 7 points:  A Rails application whose home page shows a simplified version of the Etsy home page.  Grading is based mostly on mechanics ("does it show a web page"), but decent CSS styling is expected.
- 2 points: An uploaded wireframe.
- 1 point: The home page includes your estimate and actual time. (The time values are not graded. You get a point for simply including the proper HTML to display them).

**HINTS**

- The application layout file is `app/views/layouts.html.erb`
- Your css goes in `app/assets/stylesheets/application.css` after all of the comments
- You will need a Rails controller to represent your home page:
    - Create a file named `app/controllers/products_controller.rb`
    - Peek at the code we wrote in class for an example of the Ruby code for your controller file
    - Create a folder named `app/views/products`
    - Create a file named `app/views/products/index.html.erb` to contain your HTML code
    - Peek at the code we wrote in class for how to code `config/routes.rb`
