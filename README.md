# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Responsive Flexbox Page</title>
  <link rel="stylesheet" href="style.css">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

  <!-- Navigation Bar -->
  <nav class="navbar">
    <div class="logo">MyBrand</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Content Layout -->
  <main class="container">
    <section class="main-content">
      <h1>Welcome to My Website</h1>
      <p>This responsive page uses Flexbox and adapts to different screen sizes using media queries.</p>
    </section>

    <aside class="sidebar">
      <h2>Sidebar</h2>
      <p>This section contains extra info or links.</p>
    </aside>
  </main>

  <footer class="footer">
    &copy; 2025 MyBrand. All rights reserved.
  </footer>

</body>
</html>


/* General Reset & Font */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
  color: #333;
}

/* Navigation Bar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #222;
  padding: 15px 20px;
  color: white;
}
.logo {
  font-size: 24px;
  font-weight: bold;
}
.nav-links {
  list-style: none;
  display: flex;
}
.nav-links li {
  margin-left: 20px;
}
.nav-links a {
  color: white;
  text-decoration: none;
}
.nav-links a:hover {
  text-decoration: underline;
}

/* Main Container Layout */
.container {
  display: flex;
  padding: 20px;
  gap: 20px;
}

/* Content Section */
.main-content {
  flex: 3;
  background-color: white;
  padding: 20px;
  border-radius: 8px;
}

/* Sidebar Section */
.sidebar {
  flex: 1;
  background-color: #eee;
  padding: 20px;
  border-radius: 8px;
}

/* Footer */
.footer {
  text-align: center;
  padding: 15px;
  background-color: #222;
  color: white;
  margin-top: 20px;
}

/* Responsive Design */
@media (max-width: 768px) {
  .container {
    flex-direction: column;
  }

  .nav-links {
    flex-direction: column;
    margin-top: 10px;
  }

  .nav-links li {
    margin: 10px 0;
  }
}

@media (max-width: 480px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .logo {
    margin-bottom: 10px;
  }

  .nav-links {
    width: 100%;
    justify-content: space-around;
  }

  .container {
    padding: 10px;
  }
}

