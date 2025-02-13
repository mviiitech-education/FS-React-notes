## Interactive Elements

- `<details>`: Represents a disclosure widget from which the user can obtain additional information.
- `<summary>`: Summary, caption, or legend for a `<details>`element.

### `code examples`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Basic HTML Structure</title>
  </head>
  <body>
    <header>
      <h1>Welcome to My Website</h1>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <section id="home">
        <h2>Home</h2>
        <p>This is the home section.</p>
      </section>
      <section id="about">
        <h2>About</h2>
        <p>This is the about section.</p>
      </section>
    </main>
    <footer>
      <p>&copy; 2024 My Website</p>
    </footer>
  </body>
</html>
```

### TASK

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Task 01</title>
    <style>
      body {
        font-family: Arial, sans-serif;
      }

      header {
        background-color: #f4f4f4;
        padding: 10px;
      }

      nav ol {
        list-style-type: none;
        padding: 0;
      }

      nav ol li {
        margin: 5px 0;
      }

      nav ol li a {
        text-decoration: none;
        color: #333;
      }

      nav ol li a:hover {
        text-decoration: underline;
      }

      main {
        margin-top: 10px;
        padding: 10px;
        background-color: #e2e2e2;
        border-radius: 5px;
      }

      section {
        margin: 20px 0;
        padding: 10px;
        background-color: #f9f9f9;
        border-radius: 5px;
      }

      table {
        width: 100%;
        border-collapse: collapse;
      }

      table,
      th,
      td {
        border: 1px solid #ddd;
        padding: 8px;
      }

      th {
        background-color: #f2f2f2;
      }

      form {
        display: flex;
        flex-direction: column;
        width: 300px;
        margin-top: 20px;
      }

      form label {
        margin-bottom: 5px;
      }

      form input {
        margin-bottom: 10px;
        padding: 8px;
        border: 1px solid #ccc;
        border-radius: 3px;
      }

      form button {
        padding: 10px;
        background-color: #333;
        color: white;
        border: none;
        border-radius: 3px;
        cursor: pointer;
      }

      form button:hover {
        background-color: #555;
      }

      footer {
        margin-top: 20px;
        padding: 10px;
        background-color: #f4f4f4;
        text-align: center;
      }
    </style>
  </head>

  <body>
    <header>
      <nav>
        <ol>
          <li>
            <a href="#shinchan-nohara">👉 shinchan-nohara </a>
          </li>
          <li>
            <a href="#kazama">👉 kazama </a>
          </li>
          <li>
            <a href="#neni">👉 neni </a>
          </li>
          <li>
            <a href="#bochan">👉 bochan </a>
          </li>
          <li>
            <a href="#mazow">👉 mazow </a>
          </li>
        </ol>
      </nav>
      <main>
        If you <strong>click</strong> on the above content you can
        <em>go to particular content</em>
      </main>
    </header>

    <section id="shinchan-nohara">
      <h2>Shinchan Nohara</h2>
      <p>Details about Shinchan Nohara.</p>
      <img
        height="100"
        width="100"
        src="https://wallpapers.com/images/hd/shin-chan-amazed-3ifhnlv2ww6kuwb9.jpg"
      />
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Age</th>
            <th>Hobby</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>Shinchan</td>
            <td>5</td>
            <td>Mischief</td>
          </tr>
          <tr>
            <td>2</td>
            <td>Kazama</td>
            <td>5</td>
            <td>Reading</td>
          </tr>
        </tbody>
      </table>
    </section>

    <section id="kazama">
      <h2>Kazama</h2>
      <p>Details about Kazama.</p>
    </section>

    <section id="neni">
      <h2>Neni</h2>
      <p>Details about Neni.</p>
    </section>

    <section id="bochan">
      <h2>Bochan</h2>
      <p>Details about Bochan.</p>
    </section>

    <section id="mazow">
      <h2>Mazow</h2>
      <p>Details about Mazow.</p>

      <form action="/submit" method="post">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required />

        <label for="age">Age:</label>
        <input type="number" id="age" name="age" required />

        <label for="hobby">Hobby:</label>
        <input type="text" id="hobby" name="hobby" required />

        <button type="submit">Submit</button>
      </form>
    </section>

    <footer>
      <p>&copy; 2024 Your Website. All rights reserved.</p>
    </footer>
  </body>
</html>
```
