This is a readme for my project airship airships fly with a hydrogen gas chamber that can make it lift
🌐 Aahan Patel | Personal Website

A simple, clean and responsive personal website built with HTML, CSS and a little JavaScript. It introduces who I am, shows what I'm learning, and gives people a way to get in touch. The page also has an animated typing effect in the headline, powered by the Typed.js library.

I'm a 14-year-old who loves coding. This project is part of my journey of learning web development and Python, one step at a time.

📑 Table of Contents
Overview
Features
Tech Stack
Project Structure
Getting Started
How the Code Works
Customization Guide
Deployment
Troubleshooting
What I Learned
Roadmap
Safety and Privacy
Contributing
License
Contact
Acknowledgements
📖 Overview

This website is a single-page portfolio. Instead of having three separate files (index.html, contact.html, about.html), everything lives in one index.html file, and the navigation bar scrolls to each section using anchor links.

The goals of this project are:

Build a real website from scratch without a framework.
Keep the code short, readable and easy to edit.
Practice HTML structure, CSS styling and basic JavaScript.
Have something I can share with friends, family and, one day, future teachers or employers.
✨ Features
Single-page layout with Home, About and Contact sections.
Navigation bar that jumps to each section when clicked.
Animated typing effect that cycles through phrases like "Web Developer" and "Python Learner".
Responsive design that works on phones, tablets and computers.
Clean colour scheme with a dark navy navigation bar and blue headings.
No build tools needed. Just open the file in a browser.
Lightweight. The whole page is under 100 lines of code.
🛠 Tech Stack
Technology	Purpose
HTML5	Structure and content of the page
CSS3	Layout, colours, fonts and spacing
JavaScript	Runs the typing animation
Typed.js	Library that creates the typing effect

No frameworks, no package managers and no build steps. Just the basics.

📁 Project Structure
my-website/
│
├── index.html     # The whole website (HTML + CSS + JS)
└── README.md      # This file

As the site grows, it can be split into more files:

my-website/
│
├── index.html
├── style.css      # Styles moved out of index.html
├── script.js      # JavaScript moved out of index.html
├── images/        # Pictures and icons
└── README.md
🚀 Getting Started
Prerequisites

You only need two things:

A web browser (Chrome, Edge, Firefox or Safari).
A text editor such as VS Code, Notepad or Sublime Text.
Run it on your computer
Download or copy the code and save it as index.html (lowercase, exactly this name).
Double-click the file, or drag it into your browser window.
The website opens. That's it!
Run it with a local server (optional)

If you use VS Code, install the Live Server extension, right-click index.html and choose Open with Live Server. The page then refreshes automatically every time you save.

If you have Python installed, you can also run this in the project folder:

bash
python -m http.server 8000

Then open http://localhost:8000 in your browser.

⚠️ The typing animation loads Typed.js from the internet, so you need to be online for the effect to work.

🔍 How the Code Works
1. HTML: the structure

The page has four main parts inside the <body>:

html
<nav>...</nav>              <!-- Navigation bar -->
<section id="home">...</section>     <!-- Hero / introduction -->
<section id="about">...</section>    <!-- About me -->
<section id="contact">...</section>  <!-- Contact details -->
<footer>...</footer>         <!-- Copyright line -->

Each navigation link points to a section's id:

html
<a href="#about">About</a>   <!-- scrolls to <section id="about"> -->
2. CSS: the style
Rule	What it does
* { margin: 0; padding: 0; box-sizing: border-box; }	Removes default browser spacing so layouts are predictable
body	Sets the font (Arial), text colour and line height
nav	Dark navy bar with centred links
section	Limits content width to 700px and centres it on the page
#home	Centres the text in the introduction
h2	Gives section headings the blue accent colour
footer	Matches the navigation bar colour

The key idea is max-width: 700px; margin: auto;. This keeps text from stretching across wide screens and centres it neatly.

3. JavaScript: the typing animation
html
<script src="https://unpkg.com/typed.js@3.0.0/dist/typed.umd.js"></script>
<script>
  new Typed('#element', {
    strings: ['Web Developer', 'Python Learner'],
    typeSpeed: 50,
    backSpeed: 30,
    loop: true
  });
</script>
The first <script> loads the Typed.js library.
The second <script> creates a new Typed object that types into the element with id="element".
The script must come after the HTML element it controls, which is why it sits at the bottom of the <body>.
Typed.js options
Option	Meaning
strings	The list of phrases to type
typeSpeed	Typing speed in milliseconds per character (lower is faster)
backSpeed	Deleting speed in milliseconds per character
loop	true repeats forever, false plays once
startDelay	Wait time before typing begins
backDelay	Pause before deleting a phrase
showCursor	true or false to show the blinking cursor
🎨 Customization Guide
Change the text

Find these lines in index.html and replace them with your own words:

html
<h1>Hi, I'm Aahan Patel</h1>
<p>Write a few lines about yourself and your skills here.</p>
<p>Email: you@example.com</p>
Change the typing phrases
js
strings: ['Web Developer', 'Python Learner', 'Game Builder'],
Change the colours

Edit the colour codes in the <style> block:

Colour	Where it's used	Try instead

#1e293b	Navigation bar and footer	
#0f172a, 
#064e3b, 
#4c1d95

#2563eb	Headings and typing text	
#16a34a, 
#dc2626, 
#9333ea
#222	Body text	#111, #333
Change the font

Replace Arial, sans-serif in the body rule with another font, for example Georgia, serif or "Courier New", monospace.

Add a new section

Copy a section and change its id, then add a link in the navigation bar:

html
<nav>
  <a href="#projects">Projects</a>
</nav>

<section id="projects">
  <h2>Projects</h2>
  <p>Describe what you've built here.</p>
</section>
Add smooth scrolling

Add this one line to the CSS to make the page glide to each section:

css
html { scroll-behavior: smooth; }
🌍 Deployment

Putting the site online is free with these services. Ask a parent or guardian before publishing (see Safety and Privacy).

Option A: GitHub Pages
Create a free account at github.com.
Create a new repository and upload index.html and README.md.
Go to Settings → Pages.
Under Source, choose the main branch and save.
After a minute, your site is live at https://your-username.github.io/repository-name.
Option B: Netlify
Create a free account at netlify.com.
Drag and drop your project folder onto the Netlify dashboard.
Netlify gives you a live link right away.
Option C: Vercel
Create a free account at vercel.com.
Import your GitHub repository.
Click Deploy.

💡 Whichever host you use, the main page must be named index.html in lowercase.

🧰 Troubleshooting
Problem	Likely cause	Fix
"Forbidden" or 403 error	Wrong file name, wrong folder or wrong permissions on a host	Rename the file to index.html, upload it to the public folder (public_html or htdocs), set file permission to 644 and folder to 755
Page shows plain code	File saved as .txt	Save with the .html extension and choose "All files" in the save window
Typing effect doesn't appear	No internet, or the script runs before the element exists	Check your connection and keep the script at the bottom of <body>
Typing effect shows nothing	The #element id is missing or misspelled	Make sure <span id="element"></span> exists
Styles not applying	Typo or missing brace in CSS	Check every { has a matching } and every line ends with ;
Links don't scroll	href doesn't match a section id	href="#about" needs id="about"
Looks odd on phone	Missing viewport tag	Keep <meta name="viewport" content="width=device-width, initial-scale=1"> in <head>
Duplicate content	Code pasted more than once	Keep only one copy, from the first <!DOCTYPE html> to the first </html>
Tips for finding bugs
Press F12 in your browser to open Developer Tools.
Look at the Console tab for red error messages.
Use the Elements tab to inspect and test CSS live.
Use a validator such as validator.w3.org to check your HTML.
📚 What I Learned
How an HTML document is structured, from <!DOCTYPE html> to </html>.
How anchor links and id attributes create in-page navigation.
How the CSS box model works, and why box-sizing: border-box helps.
How to centre content with max-width and margin: auto.
How to load an external JavaScript library with a <script> tag.
Why a <script> placed at the end of the body can find elements above it.
How to read error messages and fix mistakes such as duplicate tags and typos.
🗺 Roadmap

Ideas for future versions:

 Add a Projects section with cards
 Add a Skills section with progress bars or tags
 Add a dark mode toggle
 Add smooth scrolling and hover effects
 Make the navigation bar stay at the top while scrolling
 Add a working contact form
 Move CSS and JavaScript into separate files
 Add a photo or avatar
 Add a small Python project showcase
 Publish the site online
🔒 Safety and Privacy

Because this is a personal website that others can see, I follow these rules:

✅ I ask a parent or guardian before publishing anything online.
✅ I use an email address that a parent or guardian knows about.
❌ I do not share my home address, phone number or school name.
❌ I do not post private photos or information about other people.
❌ I do not put passwords or secret keys in my code.
🤝 Contributing

This is a personal learning project, but feedback is welcome!

Fork the repository.
Create a new branch: git checkout -b my-idea
Make your changes and commit: git commit -m "Add my idea"
Push the branch: git push origin my-idea
Open a Pull Request and describe what you changed.

Friendly suggestions and tips for improving the code are always appreciated.

📄 License

This project is released under the MIT License. You're free to use, copy and modify it, as long as you keep the license notice.

MIT License

Copyright (c) 2026 Aahan Patel

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
📬 Contact

Aahan Patel

📧 Email: you@example.com
💻 GitHub: github.com/your-username

Thanks for visiting my website! ⭐ If you like the project, feel free to give it a star on GitHub.

🙏 Acknowledgements
Typed.js by Matt Boldt for the typing animation.
MDN Web Docs for clear HTML, CSS and JavaScript guides.
W3Schools for beginner-friendly tutorials.
freeCodeCamp for free coding lessons.
My family and friends for their support and encouragement.

Made with ❤️ and a lot of curiosity by Aahan Patel, 2026.
