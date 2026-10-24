<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Accessible & Semantic Tech Blog</title>
    <style>
        /* Basic styles for clear layout layout presentation */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: #333;
        }
        header {
            background-color: #2c3e50;
            color: #fff;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        nav ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
            gap: 1.5rem;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover, nav a:focus {
            text-decoration: underline;
        }
        .container {
            display: flex;
            gap: 2rem;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        main {
            flex: 3;
        }
        aside {
            flex: 1;
            background: #f4f4f4;
            padding: 1.5rem;
            border-radius: 8px;
        }
        article {
            border-bottom: 1px solid #ddd;
            padding-bottom: 1.5rem;
            margin-bottom: 2rem;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 6px;
        }
        footer {
            background-color: #2c3e50;
            color: #fff;
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
        }
    </style>
</head>
<body>

    <!-- Step 1 & 2: Header with Site Title and Navigation Menu -->
    <header>
        <h1>WebDev Insights</h1>
        <nav aria-label="Main Navigation">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#articles">Articles</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Step 3: Main Content Area containing key sections and sidebar -->
    <div class="container">
        <main id="main-content">
            <!-- Step 4: Correct Heading Hierarchy (h1 in header, h2 for major section, h3 for articles) -->
            <section id="articles" aria-labelledby="featured-posts-heading">
                <h2 id="featured-posts-heading">Featured Articles</h2>

                <!-- Article 1 -->
                <article>
                    <h3>Understanding Semantic HTML5</h3>
                    <p>Published on <time datetime="2026-10-24">October 24, 2026</time> by Jane Doe</p>
                    
                    <!-- Step 5: Meaningful alt text for images -->
                    <img src="https://via.placeholder.com/600x300" alt="Diagram showing the structural layout of a semantic HTML5 web page including header, nav, main, section, article, aside, and footer elements.">
                    
                    <p>Semantic HTML introduces tags that clearly describe their meaning in a human- and machine-readable way. Elements like <code>&lt;header&gt;</code>, <code>&lt;article&gt;</code>, and <code>&lt;footer&gt;</code> help search engines and screen readers parse content effectively.</p>
                    <!-- Step 6: Clear, descriptive link text -->
                    <a href="#article1" aria-label="Read more about Understanding Semantic HTML5">Read full article on Semantic HTML5</a>
                </article>

                <!-- Article 2 -->
                <article>
                    <h3>Why Web Accessibility (a11y) Matters</h3>
                    <p>Published on <time datetime="2026-10-20">October 20, 2026</time> by John Smith</p>
                    
                    <!-- Step 5: Meaningful alt text for images -->
                    <img src="https://via.placeholder.com/600x300" alt="A person using a laptop with assistive technology displayed on screen.">
                    
                    <p>Accessibility ensures that websites are usable by everyone, including people with visual, auditory, motor, or cognitive disabilities. Using proper landmark roles and semantic HTML is the foundation of accessible design.</p>
                    <!-- Step 6: Clear, descriptive link text -->
                    <a href="#article2" aria-label="Read more about Web Accessibility">Read full article on Web Accessibility</a>
                </article>
            </section>
        </main>

        <!-- Sidebar / Complementary Content -->
        <aside aria-label="Sidebar Content">
            <section>
                <h2>About the Blog</h2>
                <p>WebDev Insights provides tutorials and articles on modern front-end engineering, web performance, and digital accessibility.</p>
            </section>

            <section>
                <h2>Quick Links</h2>
                <ul>
                    <li><a href="#wcag-guidelines">WCAG 2.2 Guidelines</a></li>
                    <li><a href="#html5-spec">HTML5 Specification Document</a></li>
                </ul>
            </section>
        </aside>
    </div>

    <!-- Step 1: Footer -->
    <footer>
        <p>&copy; 2026 WebDev Insights. All rights reserved.</p>
    </footer>

</body>
</html>

Step-by-Step Breakdown of Requirements Satisfied
Semantic Page Structure (<header>, <nav>, <main>, <section>, <article>, <aside>, <footer>):

Replaced generic <div> tags with semantic structural tags to define explicit regions/landmarks on the page.

Navigation (<nav>):

Encapsulated page-level links inside <nav> with an aria-label="Main Navigation" attribute so assistive technologies can navigate directly to the menu.

Main Content (<main>):

Wrapped primary page content inside <main id="main-content">, separating it from non-primary content such as headers, footers, and sidebars.

Heading Hierarchy:

<h1>: Website title (top level).

<h2>: Main content section headings ("Featured Articles", "About the Blog").

<h3>: Article titles within the content section.

Meaningful Image alt Text:

Updated generic alt text (e.g., alt="image") to descriptive phrases explaining the visual context (e.g., alt="Diagram showing the structural layout of a semantic HTML5 web page...").

Understandable Links & Page Sections:

Made link anchor texts descriptive (avoided vague "click here" or "read more" text alone) and added aria-label where needed for screen reader context.