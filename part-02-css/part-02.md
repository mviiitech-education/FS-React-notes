### RWD

- flex

link:favicon

- floating:
  - float : right;
  - float : left;

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        
    </style>
</head>

<body>
    <p>hello fr om line 1</p>
    <p id="line-2">hello from line 2</p>
    <p>hello from line 3</p>
    <p class="last">hello from line 4</p>
    <p class="last">hello from line 5</p>
</body>

</html>
```

### INSTAGRAM

```html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>instagram</title>
    <!-- link:favicon -->
    <link rel="shortcut icon" href="./instagram-logo.png" type="image/x-icon">
    <style>
        body {
            padding: 0px;
            margin: 0px;
            height: 100vh;
            /* viewport(screen) height */
            background-color: gray;
            font-size: large;
            font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        }

        .flex-center {
            /* center */
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .mobile-phone {
            height: 650px;
            width: 400px;
            background-color: white;
            border: 5px solid black;
            border-radius: 20px;
        }

        header {
            background-color: ghostwhite;
            height: 5%;
            border-top-left-radius: 15px;
            border-top-right-radius: 15px;
        }

        .camera {
            height: 25px;
            width: 25px;
            border-radius: 50%;
            background-color: black;
        }

        main {
            width: 100%;
            padding: 10px;
        }

        .section-01 {
            height: 200px;
            display: flex;
        }

        img {
            height: 60px;
            width: 60px;
            border-radius: 50%;
        }

        .profile-section {
            width: 30%;
        }

        .detail-section {
            width: 70%;
            display: flex;
            justify-content: space-around;
            text-align: center;
        }
    </style>
</head>

<body class="flex-center">
    <!-- div.mobile-phone -->
    <div class="mobile-phone">
        <header class="flex-center">
            <div class="camera"></div>
        </header>
        <main id="instagram">
            <section>
                <p>avinash</p>
            </section>
            <section class="section-01">
                <div class="profile-section">
                    <img src="https://i.pinimg.com/736x/b6/1b/ed/b61bed48c000da085d0775a9ae02dc6b.jpg" alt="luffy">
                </div>
                <div class="detail-section">
                    <div>
                        <div>4</div>
                        <div>posts</div>
                    </div>
                    <div>
                        <div>40</div>
                        <div>followers</div>
                    </div>
                    <div>
                        <div>40</div>
                        <div>following</div>
                    </div>
                </div>
            </section>
        </main>
    </div>
</body>

</html>
```


### MAIN TASK

```html
<!DOCTYPE html>
<html lang="en" contenteditable>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>task</title>
    <style>
        body {
            font-family: monospace;
            background-color: black;
            color: white;
        }

        ol {
            /* margin-top: 100px; */
            background-color: #303841;
            margin-left: 10px;
            margin-right: 10px;
            width: 543px;
        }

        li::marker {
            content: counter(list-item) "  ";
            color: #848b93;
        }

        .red-pink {
            color: #ec5f66;
        }

        .orange {
            color: #f8ae57;
        }

        .blue {
            color: #5db4b3;
        }

        .bg-red-pink {
            background-color: #ec5f66;
        }

        .bg-gray {
            background-color: #404954;
        }

        .indent-4::before {
            content: "abcd";
            opacity: 0;
        }

        pre {
            margin-top: 0px;
            margin-bottom: 0px;
        }
    </style>
</head>

<body onload="start()">
    <ol>
        <li><span class="red-pink">#</span> who created world wide web:</li>
        <li class="bg-gray indent-4">- Tim Berner lee: Working in CERN</li>
        <li class="bg-gray indent-4">- HTML created1989</li>
        <li class="orange">-------------------------------------------------</li>
        <li><span class="red-pink">#</span> world wide web and html:</li>
        <li class="bg-gray indent-4">- how it is related.</li>
        <li class="bg-gray indent-4">- Enables content sharing over the Internet through user-friendly ways.</li>
        <li class="orange">-------------------------------------------------</li>
        <li><span class="red-pink">#</span> Browser:</li>
        <li class="bg-gray indent-4">- First browser: Netscape</li>
        <li><span class="blue">[</span> <span class="orange">browser Engine</span> <span class="blue">]</span>:</li>
        <li><span style="color: #6396cb;">Browser-engine</span>
            <span class="bg-red-pink">
                is core concept of web browser responsible for rendering, web content, interpreting HTML,
                CSS, and Javascript code, and displaying webpages to user.
        </li>
        </span>
        <li class="bg-gray  indent-4">Examples:</li>
        <li class="bg-gray">
            <pre>        - Blink        : developed by google </pre>
        </li>
        <li class="bg-gray">
            <pre>        - Webkit       : developed by Apple </pre>
        </li>
        <li class="bg-gray">
            <pre>        - Gecko        : developed by Mozilla </pre>
        </li>
        <li class="bg-gray">
            <pre>        - Trident      : developed by Microsoft </pre>
        </li>
        <!-- <script src="./script.js"></script> -->
</body>

</html>
```

