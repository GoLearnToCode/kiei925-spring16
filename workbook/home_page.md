# How To Create a Home Page 

When you start a new web application, often the first thing you want to do is change the home page.  Here's how.

When creating your site's home page, you have three choices.

3. Invent an artifical resource and use it as your home page resource
1. Adopt an existing resource (see below if you don't know anything about _resources_ yet)

If you need to learn more about resources, go to <%= workbook_link 'Creating Resources in Rails', :resource %>.

### Option 1: Invent an Artifical Resource

For this step, most develoeprs create a resource named `pages`.  Yes, it's not very creative.  But sometimes we have
some arbitrary web pages that just don't seem to belong to any other resource.  An _About_ page, terms and conditions, 
privacy policy statements... these all need to be web pages, and they need to belong somewhere in our application.

In Rails, we adopt the notion that our application is simply a container of resources.  All web pages belong to a resource of some kind.  For a static web pages that doesn't seem to belong anywhere else, let's just invent a resource named `pages` and declare victory.

**STEP 1: The Route**

In your `config/routes.rb` file:

```
root 'pages#home'
```

Rails uses the word "root" to mean "home page".  Go figure.

Try refreshing your browser.  You should see a big error message.  That's good!  It means it's time for Step 2.

**STEP 2: The Controller**

Every resource needs a _controller_, which consists of a `controller class` and a `folder` to contain the HTML files for the resource.  Start by adding a new file to your project named:

`app/controllers/pages_controller.rb`

Next, add a folder named this:

`app/views/pages`

Go into `app/controllers/pages_controller.rb` and add this code:

```
class PagesController < ApplicationController

end
```

Try refreshing your browser.  You should see a big error message.  That's good!  It means it's time for Step 3.

**STEP 3: The View**

When we created the route `pages#home`, we actually promised a resource named `pages` (which we now have) and an HTML file named `app/views/pages/home.html.erb` which we don't have yet.  So add a file by that name, and add this code into it:

```
<h1>Hello, World!</h1>
```

Try refreshing your browser.  You should see "Hello, World!".  If not, _read the error message as best you can_ and review the steps above.


### Option 2: Adopt an Existing Resource

This is the easiest option, if you have already have a resource you can repurpose.  All you need is to draw the route.  Suppose you want to use your product listing page as your home page.  In `config/routes.rb`, add this:

`root 'products#index'`

and you're done!

