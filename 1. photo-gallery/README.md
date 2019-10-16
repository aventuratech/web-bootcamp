Awesome Photo Gallery
=====================

the best way to learn how to program websites is programming websites, so we are going to jump right in and create a site!
In this course we are going to build a photo gallery that highlights some beautiful stock photography shared by the 
good people at picsum.

Section 1 
---------

    
Section 2
---------

add the image tiles, learn about flex, style cards

1. add a new section for the slides and style it

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600&display=swap" rel="stylesheet">
    <style>
        body, html{
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .hero{
            position: relative;
        }

        .hero-image{
            width: 100%;
            height: auto;
        }

        .hero-text{
            position: absolute;
            right: 0;
            bottom: 0;
            left: 0;
            padding: 5rem 2.5rem;
            text-align: center;
            color: #fff;
            background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.5));
        }

        .hero-text h1{
            font-weight: 300;
            font-size: 3rem;
            margin: 0 0 .5rem 0;
        }

        .slides{
            background: #424242;
            padding: 1rem;
        }
    </style>
</head>
<body>
    <section class="hero">
        <img class="hero-image" src="https://picsum.photos/seed/hero/1040/780">
        <div class="hero-text">
            <h1>Awesome Photo Gallery</h1>
            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
    </section>
    <section class="slides">
        slides go here...
    </section>
</body>
</html>
```
2. add five images

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600&display=swap" rel="stylesheet">
    <style>
        body, html{
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .hero{
            position: relative;
        }

        .hero-image{
            width: 100%;
            height: auto;
        }

        .hero-text{
            position: absolute;
            right: 0;
            bottom: 0;
            left: 0;
            padding: 5rem 2.5rem;
            text-align: center;
            color: #fff;
            background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.5));
        }

        .hero-text h1{
            font-weight: 300;
            font-size: 3rem;
            margin: 0 0 .5rem 0;
        }

        .slides{
            background: #424242;
            padding: 1rem;
        }
    </style>
</head>
<body>
    <section class="hero">
        <img class="hero-image" src="https://picsum.photos/seed/hero/1040/780">
        <div class="hero-text">
            <h1>Awesome Photo Gallery</h1>
            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
    </section>
    <section class="slides">
        <img src="https://picsum.photos/seed/slide1/240">
        <img src="https://picsum.photos/seed/slide2/240">
        <img src="https://picsum.photos/seed/slide3/240">
        <img src="https://picsum.photos/seed/slide4/240">
        <img src="https://picsum.photos/seed/slide5/240">
    </section>
</body>
</html>
```

3. add image wrappers

```html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600&display=swap" rel="stylesheet">
    <style>
        body, html{
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .hero{
            position: relative;
        }

        .hero-image{
            width: 100%;
            height: auto;
        }

        .hero-text{
            position: absolute;
            right: 0;
            bottom: 0;
            left: 0;
            padding: 5rem 2.5rem;
            text-align: center;
            color: #fff;
            background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.5));
        }

        .hero-text h1{
            font-weight: 300;
            font-size: 3rem;
            margin: 0 0 .5rem 0;
        }

        .slides{
            background: #424242;
            padding: 1rem;
        }
    </style>
</head>
<body>
    <section class="hero">
        <img class="hero-image" src="https://picsum.photos/seed/hero/1040/780">
        <div class="hero-text">
            <h1>Awesome Photo Gallery</h1>
            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
    </section>
    <section class="slides">
        <div class="slide">
            <img src="https://picsum.photos/seed/slide1/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide2/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide3/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide4/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide5/240">
        </div>
    </section>
</body>
</html>
```
4. display them in a centered row with flex and style wrappers

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600&display=swap" rel="stylesheet">
    <style>
        body, html{
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .hero{
            position: relative;
        }

        .hero-image{
            width: 100%;
            height: auto;
        }

        .hero-text{
            position: absolute;
            right: 0;
            bottom: 0;
            left: 0;
            padding: 5rem 2.5rem;
            text-align: center;
            color: #fff;
            background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.5));
        }

        .hero-text h1{
            font-weight: 300;
            font-size: 3rem;
            margin: 0 0 .5rem 0;
        }

        .slides{
            background: #424242;
            padding: 4px;
            display: flex
        }

        .slide{
            flex: 1;
            margin: 8px;
            border-radius: 4px;
            overflow: hidden;
            box-shadow: 0.3em 0.3em 1em rgba(0,0,0,0.3);
        }

        .slide img{
            width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <section class="hero">
        <img class="hero-image" src="https://picsum.photos/seed/hero/1040/780">
        <div class="hero-text">
            <h1>Awesome Photo Gallery</h1>
            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
    </section>
    <section class="slides">
        <div class="slide">
            <img src="https://picsum.photos/seed/slide1/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide2/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide3/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide4/240">
        </div>
        <div class="slide">
            <img src="https://picsum.photos/seed/slide5/240">
        </div>
    </section>
</body>
</html>
```

5. replace hero image on slide click 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600&display=swap" rel="stylesheet">
    <style>
        body, html{
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .hero{
            position: relative;
        }

        .hero-image{
            width: 100%;
            height: auto;
        }

        .hero-text{
            position: absolute;
            right: 0;
            bottom: 0;
            left: 0;
            padding: 5rem 2.5rem;
            text-align: center;
            color: #fff;
            background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.5));
        }

        .hero-text h1{
            font-weight: 300;
            font-size: 3rem;
            margin: 0 0 .5rem 0;
        }

        .slides{
            background: #424242;
            padding: 4px;
            display: flex
        }

        .slide{
            flex: 1;
            margin: 8px;
            border-radius: 4px;
            overflow: hidden;
            box-shadow: 0.3em 0.3em 1em rgba(0,0,0,0.3);
        }

        .slide img{
            width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <section class="hero">
        <img id="hero-image" class="hero-image" src="https://picsum.photos/seed/hero/1040/780">
        <div class="hero-text">
            <h1>Awesome Photo Gallery</h1>
            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
    </section>
    <section class="slides">
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide1')">
            <img src="https://picsum.photos/seed/slide1/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide2')">
            <img src="https://picsum.photos/seed/slide2/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide3')">
            <img src="https://picsum.photos/seed/slide3/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide4')">
            <img src="https://picsum.photos/seed/slide4/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide5')">
            <img src="https://picsum.photos/seed/slide5/240">
        </div>
    </section>
    <script type="text/javascript">
        const switchImage = (image) => {
            // get a reference to the hero image element
            const hero = document.getElementById("hero-image");

            // now load a full resolution version  
            const large = image + '/1040/780';

            // and set the hero image src
            hero.src = large;
        }
    </script>
</body>
</html>
```

6. preload images to eliminate the delay switching

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,500,600&display=swap" rel="stylesheet">
    <style>
        body, html{
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
        }

        .hero{
            position: relative;
        }

        .hero-image{
            width: 100%;
            height: auto;
        }

        .hero-text{
            position: absolute;
            right: 0;
            bottom: 0;
            left: 0;
            padding: 5rem 2.5rem;
            text-align: center;
            color: #fff;
            background-image: linear-gradient(rgba(0,0,0,0), rgba(0,0,0,.5));
        }

        .hero-text h1{
            font-weight: 300;
            font-size: 3rem;
            margin: 0 0 .5rem 0;
        }

        .slides{
            background: #424242;
            padding: 4px;
            display: flex
        }

        .slide{
            flex: 1;
            margin: 8px;
            border-radius: 4px;
            overflow: hidden;
            box-shadow: 0.3em 0.3em 1em rgba(0,0,0,0.3);
        }

        .slide img{
            width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <section class="hero">
        <img id="hero-image" class="hero-image" src="https://picsum.photos/seed/hero/1040/780">
        <div class="hero-text">
            <h1>Awesome Photo Gallery</h1>
            <p class="lead">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
    </section>
    <section class="slides">
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide1')">
            <img src="https://picsum.photos/seed/slide1/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide2')">
            <img src="https://picsum.photos/seed/slide2/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide3')">
            <img src="https://picsum.photos/seed/slide3/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide4')">
            <img src="https://picsum.photos/seed/slide4/240">
        </div>
        <div class="slide" onclick="switchImage('https://picsum.photos/seed/slide5')">
            <img src="https://picsum.photos/seed/slide5/240">
        </div>
    </section>
    <script type="text/javascript">
        // preload images to avoid delay when you switch the src
        for (let i = 1; i <= 5; i++) {
            const image = new Image();
            image.src = 'https://picsum.photos/seed/slide' + i + '/1040/780';
            console.log('pre-loading ' + image.src);
        }
        
        const switchImage = (image) => {
            // get a reference to the hero image element
            const hero = document.getElementById("hero-image");

            // now load a full resolution version  
            const large = image + '/1040/780';

            // and set the hero image src
            hero.src = large;
        }
    </script>
</body>
</html>
```



Section 3
---------

add about section with alternating blocks / text. review on mobile device, and learn about responsive design

1. create the about section
2. add three blocks with an image and lorem ipsum
3. lay the blocks out with flex
4. alternate image / text in blocks with flex direction
5. review section on mobile
6. update blocks so they display on mobile devices

Section 4
---------

add contact section with google map, social media sharing links

1. 

Section 5
---------

add navigation to page and scroll with javascript 

Section 6
---------

change hero image when you click the cards

Section 7
---------

load images from picsum API

Section 8
---------

deploy your page to github pages


    


## Getting Started

there are three languages that we use for every website:

* HTML: this is the language that we use to write pages that are displayed in the browser
* CSS: this is the language that we use to make the HTML pages beautiful
* JavaScript: this is the language that we use to bring our web pages to life

You are going to learn a little of each over the course of this course.

To get started you need to create the basic HTML page:

1. create a new folder called `awesome-photo-gallery`
2. add a new file to the awesome photo gallery called `index.html`
3. Copy and paste the template below into the `index.html` file

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
</head>
<body>
</body>
</html>
```

If you open the page in the browser you will see blank page. Not very exciting, but this is the beginning of every 
website. Now you are ready to get creative!

You will notice that this template has two sections, the `<head>` and the `<body>`:

* the head is where you tell the browser more about your page, things like the title, language, description, etc
* the body is where all of the content that the browser should display.

## The page head

! Setup title and description

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Awesome Photo Gallery</title>
    <meta name="description" content="Some beautiful stock photography"/>
</head>
<body>
</body>
</html>
```

If you reload your browser now its still a blank page, but you might notice that the browser tab now shows that you are
on your "Awesome Photo Gallery".

## Adding some content

1. add hero section
2. add large image to hero and explain images
3. add h1 and explain how headers work
4. add lead p with lorem ipsum (explain lorem ipsum)





