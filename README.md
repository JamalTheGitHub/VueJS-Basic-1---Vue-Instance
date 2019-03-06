# Vue Basic 1 => The Vue Instance

Assuming you have Vue installed as well as the extension <strong>Live Server</strong>, create a folder called "VueJS Tutorials". This folder will be your playground for practicing VueJs as well as learning VueJS. Now lets proceed to learning VueJS!!

NOTE that this tutorial is done with <strong>Visual Studio Code</strong> and you NEED to have understanding of Javascript before proceeding.

===============================================================================================

First things first, create an <strong>index.html</strong>. Lay down the frame;
    <!DOCTYPE html>
    <html>

    </html>

Now, whatever code that we will be doing in the <strong>html</strong> will be shown later in the local server on the web browser via <strong>Live Server</strong> extension. Next step is to add the <strong>head</strong> and the <strong>body</strong> into the <strong>html</strong>.
    <!DOCTYPE html>
    <html>
      <head>


      </head>
      <body>




      </body>
    </html>

Next in the <strong>head</strong> we need to add <strong>meta charset="utf-8"</strong>. <strong>meta charset="utf-8"</strong> is defined as a character encoding capable of encoding all possible characters in Unicode. The encoding is variable-length and uses 8-bit code units. To understand more about this, please use <strong>google</strong>. Anyways, here is how we add it to the <strong>head</strong>;

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">


      </head>
      <body>




      </body>
    </html>

Then we add the <strong>title</strong> in our head.

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>VueJS Tutorial</title>

      </head>
      <body>




      </body>
    </html>

What this does is that when you run the <strong>Live Server</strong> extension, there will be a tab opened in your web browser and the name of the tab will correspond to the name you put in the <strong>title</strong> section inside the <strong>head</strong>. Now add <strong>Vue</strong> script source and stylesheet link up in the <strong>head</strong>.

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>VueJS Tutorial</title>
        <link href="styles.css" rel="stylesheet"/>
        <script src="https://unpkg.com/vue">

      </head>
      <body>




      </body>
    </html>

Since we want to link up to the stylesheet, create a file called "styles.css". This file will be used to manipulate the looks of your website later. The <strong>script src="https://unpkg.com/vue</strong> is just enabling us to use the VueJS in the <strong>index.html</strong> file after installing it. Finally add a local <strong>JavaScript</strong> source in the body called "app.js;

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>VueJS Tutorial</title>
        <link href="styles.css" rel="stylesheet"/>
        <script src="https://unpkg.com/vue">

      </head>
      <body>



        <script src="app.js"></script>
      </body>
    </html>

Now create a file called <strong>"app,js"</strong>. This will be the file where we will manipulate the JavaScript(<strong>JS</strong>). Basically that is it for the most basic <strong>html</strong> template.

Alright, moving on to the real reason why we are here, to learn VueJS!. Start by opening the file "app.js". First things first, lets make a <strong>Vue Instance</strong>.

In the app.js;

    new Vue({});

Basically <strong>Vue Instance</strong> is just an object that VueJS provided us with. Okay, so what does <strong>Vue Instance</strong> do? Well, it controls the whole part or a certain part of our application. It will take the object, <strong>{}</strong>, as a parameter and inside the object is where we put datas, options or methods to describe how this <strong>Vue Instance</strong> is going to control the application. Add this, inside the object;

    new Vue({
      el: ""
    });

This <strong>el:</strong> means to target the element in order to control it. For now it is empty hence the empty <strong>""</strong>. Now create an element that will be the root element. Lets go back into the <strong>index.html</strong> file and add the following to the <strong>body</strong>.

In the index.html;

    <body>
      <div id="vue-app">
        <h1>{{ name }}</1>
      </div>

    
      <script src="app.js"></script>
    </body>

Notice that we have added a <strong>div</strong> with an <strong>id</strong> of "vue-app". Inside the div we have also put a header(h1) with <strong>{{ name }}</strong> in it. Basically we are calling a data from <strong>app.js</strong> but the data "name" has not been defined in our <strong>app.js</strong>. Now lets go back to <strong>app.js</strong> and tweak Our code in order for it to work.

In the app.js;

    new Vue({
      el: "#vue-app"
      data: {
        name: "James"
      }
    });

Alright, before we go live with the <strong>Live Server</strong> extension, lets go through on what just happened. First of all, notice that <strong>el:</strong> is targeting the <strong>element</strong> with the id of "vue-app" which in this case is the <strong>div</strong> that we created in the <strong>index.html</strong>. Also, notice that the <strong>hashtag(#)</strong> before the <strong>vue-app</strong> because we are using the <strong>id</strong> selector. If it was a <strong>class</strong> selector, therefore we would use <strong>full stop(.)</strong> instead. Now we need to establish an <strong>object</strong> in the <strong>data</strong>. Basically this is the <strong>data</strong> => <strong>data:</strong> and this is the object within the <strong>data</strong> => <strong>{}</strong>, anything in that particular <strong>{}</strong> associated with the <strong>data</strong> is called <strong>data property</strong>. The <strong>data</strong> is where we store all of our information for this <strong>Vue Instance</strong>. Inside the <strong>{}</strong> is where we store our <strong>key value pairs</strong> which can be many things. Now remember in the <strong>index.html</strong> we made the <strong>element div</strong> and in it we have this, <strong>{{ name }}</strong>. That is the <strong>data property</strong> called name and since we already defined it in the <strong>data</strong> with <strong>name: "James"</strong>, the program know that when we run it and go live with the extension of <strong>Server Live</strong>, it will retrieve the information inside the <strong>Vue Instance</strong> of <strong>app.js</strong>. Now go live with <strong>Server Live</strong> and see the result.

That is it for now! Go the the next tutorial once you have grasp this tutorial!