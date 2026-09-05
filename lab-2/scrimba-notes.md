# scrimba



##### **Accessible Development Intro**

* ###### Accessible content is available, and its functionality can be operated, *by literally anyone.* 



##### **Understanding Web Accessibility**

**Principles and Practices**

###### 

###### **ATs- Assistive Technologies**

* Screen readers
* Speech recognition software
* Screen magnifiers
* Alternative input devices 





###### **The Accessibility Tree** 

<button>I'm a button</button> **CORRECT!**

<div>I'm trying to be a button!</div> **WRONG!**



**CHROME BROWSER** 

**Guide for using accessibility tree in Chrome DevTools:**

[**https://developer.chrome.com/blog/full-accessibility-tree/**](https://developer.chrome.com/blog/full-accessibility-tree/)

Open dev tools. There will be a tab called accessibility. Click on that then click on enable full page accessibility tree. Your dev tool will ask you to reload, and when you do, you will see an accessibility button pop up. If you click on it, you will see the accessibility tree. 



###### **Accessibility Testing**

* Using AT
* Contrast Checkers
* Automated Tools

  * &#x09;-Lighthouse (select from Chrome DevTools)
  * &#x09;-Accessibility Inspector
  * &#x09;-aXe
* AI assistants



##### **Aside: Text Contrast**

###### **Accessibility Guidelines (Web Content Accessibility Guidelines (WCAG) 2.0**

* Well-defined requirements on things like text, images, HTML code, etc.
* **Different levels called:**

  * **A = NOT ACCESSIBLE**
  * **AA = ACCESSIBLE**

    * 4.5:1 contrast for normal text
    * 3:1 for large text (>=24px)
  * **AAA = HIGHEST GRADE OF ACCESSIBILITY**

    * 7:1 contrast for normal text
    * 4.5:1 for large text (>=24px)



###### **Color Contrast**

* The contrast that text has against its background



**Contrast ratio checker:** [**https://webaim.org/resources/contrastchecker/**](https://webaim.org/resources/contrastchecker/)

\-OR-

Ctrl shift C



*Challenge:*

*Change the color of each text so that they all fulfill the WCAG's AA requirements (a contrast ratio of 4.5)*



\*\*Red and Green cannot reach a contrast of 7.



##### **Aside: Use of Color**

Pair the color indicator with an icon aw well as to add the status text.

Helps with color blindness. 



&#x20; <div class="indicator"><span>✔</span></div>**Online**

&#x20;               </div>

&#x20;           </div>

&#x20;       </div>

&#x20;       <div class="user-card">

&#x20;           <img src="images/kevin-the-minion.png" alt="User's name" class="profile-pic">

&#x20;           <div class="user-info">

&#x20;               <h3>Kevin the Minion</h3>

&#x20;               <div class="status">

&#x20;                   <div class="indicator offline"><span>X</span></div>**Offline**

&#x20;               </div>





##### **Aside: Text Contrast**

*Challenge:*

*1. Identify any elements on the page where the text contrast is poor.*

*2. Change those elements according to the AAA requirements.*

*3. Google 'background-blend-mode' and see if you can figure out how to make the background image brighter (About Section).*



.hero-heading span {

&#x20;   color: #007000;

&#x20;   font-weight: 700;

&#x20;   line-height: 1;

&#x20;   display: block; 

}



.hero-image {

&#x20;   max-width: 350px;

&#x20;   position: absolute;

&#x20;   right: -20px;

&#x20;   top: -50px;

&#x20;   z-index: -1;

}



.social-links {

&#x20;   display: flex;

&#x20;   justify-content: space-between;

&#x20;   align-items: center;

&#x20;   margin: 0 auto;

&#x20;   padding: 20px 40px;

&#x20;   width: 800px;

&#x20;   color: #ffffff;

}



.about-section {

&#x20;   background-color: rgba(255, 255, 255, 0.85);

&#x20;   background-blend-mode: lighten;

&#x20;   background-image: url(images/clouds.jpg);

&#x20;   background-size: cover;

&#x20;   display: flex;

&#x20;   justify-content: center;

&#x20;   align-items: center;

&#x20;   width: 700px;

&#x20;   margin: 0 auto;

&#x20;   padding: 40px;

&#x20;   border: 2px solid #333333;

}



body {

&#x20;   background-image: url('images/background.jpg');

&#x20;   background-size: cover; /\* Ensures the image covers the whole section \*/

&#x20;   background-position: center; /\* Centers the image in the section \*/

}





##### **Aside: Alternative Text**

hidden in code for screen readers 

add alt attribute to any image unless its purely decorative. add an empty alt attribute otherwise bc without it a screen reader may read out the image file name instead.



Would hero section always have an alternate text? No. not all images such as purely decorative images. Spacing images, backgrounds. 

but still put an empty alt attribute. 





&#x20; <img class="image image-1" src="images/astronaut.jpg" alt="An astronaut suspended in mid-air by a dark cloud over a field of purple grass." />



&#x20; <section class="chair-section">

&#x20;               <p>What is 'fine art'? What is 'chair art'?🪑 Who sat in that chair and what did the cloud do with them? The artist traverse dimensions into the ethereal space of the unconscious consciousness. Explore more of their mindbending art <a href="https://unsplash.com/@eduardgross" target="\_blank">here</a>.</p>

&#x20;               <img class="image image-2" src="images/chair.jpg" alt="A chair with a small cloud hovering over it, in the desert, next to a dark rock." />

&#x20;           </section>





##### **Aside: Links**

should use the <a> element

should be recognizable as links

should have non-ambiguous text

\--- examples of bad practice are "click here", "more", "continue", etc.

Change text color, bold, underline, define what the link is ie **Visit Scrimba Here**





*Challenge: Update our links so that they meet the following requirements:*

*1. They can be identified as links by more than just color.*

*2. The link text is not ambiguous, as in the links make sense out of context.*



href="https://unsplash.com/es/@sebastiansvenson" target="\_blank">here</a>.</p>

&#x20;               <img class="image image-3" src="images/cubes.jpg" />

**VERSUS**

&#x20;<a href="https://unsplash.com/es/@sebastiansvenson" target="\_blank">Enjoy their digital art here</a>.</p>

&#x20;               <img class="image image-3" src="images/cubes.jpg" />



then go into CSS to make text bolder, underline, color:



**text-decoration: underline** is the default for <a> elements so its not needed to add 



###### **Cards**

any nested structure is lost in the link.

instead, the link should be positioned inside the car w/o wrapping any text.



&#x20;<a href="https://unsplash.com/@shaarannnnn" target="\_blank" aria-label="Check out more of this artist's otherwordly art"></a>



\*can also be a good idea to add a hover effect to the entire card to make sure the curser is a pointer and to modify the call to 

action text so the user understands the whole card is focusable.



##### **Skynet Eats** 



*Challenges:*

*1. Update our images so that they have appropriate alternative texts.*

*2. Update any links that are either not recognizable as links or have ambiguous text.*



&#x20;<div class="hero-section">

&#x20;               <img class="hero-image" src="images/hero-image.jpg" alt="Food delivery drone saying 'I come with peas'" />

&#x20;               <div>



&#x20; <div class="statistics">

&#x20;               <img class="info-image" src="images/pal9000.jpg" **alt="A flying Skynet drone"** />

&#x20;               <div class="stat">

&#x20;                   <h4 class="stat-heading">Drones🤖</h4>

&#x20;                   <p class="stat-number">+4000</p>



*\*Add a period to give screen reader a pause\**





&#x20; <p>Is it a bird? Is it a plane? None of the above. It’s a drone on its way to you with your tasty groceries! If you don’t want fast food, but you want your food fast, check out our partnered shops here</a>.</p>

*---- takes <a> and wraps it around*



&#x20;<div class="about-link">

&#x20;                   <a href="#">About Skynet</a>

&#x20;               </div>



.info a {

&#x20;   color: #007000;

&#x20;   text-decoration: underline;

}



.stat-heading {

&#x20;   color: #cccccc;

&#x20;   font-size: 20px;

&#x20;   font-weight: 500;

&#x20;   margin-bottom: 0;

}



#### **Aside: Labels**



Unfortunately, elements like input fields often lack labels and are replaced by placeholder text. 



###### **Sign-Up Page**

*Challenge:*

*1. Add an id attribute to each input field. (You are going to need it, \*hint hint\*)*

*2. Add labels for each input field in the form. Look up how to associate a label with an input field so that when clicking the label, the input field gets focused.*

*3. Change the placeholder names to be exemplary user inputs, i.e. "Obama" for a surname field.*



&#x20; <input class="contact-input" id="name" type="text" placeholder="Full name" />

&#x20;                   <input class="contact-input" id="address" type="text" placeholder="Address" />

&#x20;                   <div class="address">

&#x20;                       <div class="city">

&#x20;                           <input class="address-input" **id="city"** type="text" placeholder="City" />

&#x20;                       </div>

&#x20;                       <div class="postcode">

&#x20;                           <input class="address-input" **id="postcode"** type="text" placeholder="Postcode" />

&#x20;                       </div>

&#x20;                   </div>

&#x20;                   <input class="contact-input" **id="email"** type="text" placeholder="Email" />



*\*Now add label elements to all input fields\**



&#x09;	<form>

&#x20;                   <h2 class="contact-form-heading">Sign up</h2>

&#x20;                   <p class="contact-form-intro">Enter your contact information, and then there will be cake. 🍰</p>

&#x20;                   **<label for="name">Full name</label>**



**\****it makes no sense for the placeholder name to be the exact copy of the label.*

*instead, write an example of a full name, address etc.\**



&#x20;<label for="name">Full name</label>

&#x20;                   <input class="contact-input" id="name" type="text" **placeholder="Sherlock Holmes" />**



the text inside links and buttons act as labels providing an accessible name in the browsers accessibility.

without using button label, use aria attribute.



##### **Aside: Radio Buttons**



Use field-set and legend tags to group the set and provide a context for screen reader users.

when screen reader encounters a field set tag it announces the user has entered a new group or fieldset. helps users know following elements are related and are part of the group. Legend tag reads it out as title or description of the group. 



*Challenge:*

*1. On your own, look up the <fieldset> and <legend> tags and how to use them for radio buttons.*

*2. Update the elements used to group our radio buttons so that the <fieldset> and <legend> elements are used instead.*

*fieldset and legent elemnets come with inherent styling.* 



&#x20;<label for="email">Email</label>

&#x20;                   <input class="contact-input" id="email" type="text" placeholder="sherlock.holmes@gmail.com" />

&#x20;                   **<fieldset class="radio-container">**

&#x20;                       **<legend>Do you have cats?</legend>**

&#x20;                       <label for="yes">Yes</label>



fieldset {

&#x20; border: 2px solid #333;

&#x20; border-radius: 40px;

&#x20; padding: 10px 10px 10px 20px;

}



##### **Labels**



*Challenge:*

*1. Add labels for each input field in the form.*

*2. Change the placeholder names to be as accessible and helpful as possible (hint: also make sure the text color contrast is good enough).*

*3. Update the button text to be less ambiguous.*



&#x20; <!-- Form section -->

&#x20;           <div class="form-section">

&#x20;               <form>

&#x20;                   <h2 class="form-heading">What's Next?</h2>

&#x20;                   <p class="form-intro">Want pizza through your window?🍕 Recieve a notification when the service is available.</p>

&#x20;                   **<label for="name">Full name</label>**

&#x20;                   <input class="input" id="name" type="text" **placeholder="Ariana Regular" />**

&#x20;                   **<label for="email">Email</label>**

&#x20;                   <input class="input" id="email" type="email" **placeholder="ariana.regular@gmail.com" />**

&#x20;                   <div class="submit-button" type="button" onclick="submitForm()">✓</div>

&#x20;               </form>

&#x20;           </div>



*\*make button less ambiguous\**



&#x20;<div class="submit-button" type="button" onclick="submitForm()**">Notify me</div**>

&#x20;               </form>



*\*update CSS placeholder color\**



.input::-webkit-input-placeholder {

&#x20;   **color: #555555;**

}



##### **Semantic HTML Recap** 

###### (use of descriptive tags)



###### **Landmark Regions**

* <nav>
* <header>
* <main>
* <section>
* <footer>

*--- help communicate the layout and important areas of a page and allow quick access to different regions.*



*Challenge:*

*1. Update our code with semantic HTML using the landmark regions nav, main, section, and footer.*

*2. Update our submit button to be a <button> element.(the Notify button)*



&#x20;<!-- Navigation bar -->

&#x20;       **<nav** class="navbar">

&#x20;           <div class="logo">

&#x20;               <span class="iconify icon" data-icon="healthicons:drone-outline"></span>

&#x20;               <p class="logo-text">Skynet Eats</p>

&#x20;           </div>

&#x20;           <div class="nav-links">

&#x20;               <a class="nav-link" href="index.html">Home</a>

&#x20;               <a class="nav-link" href="#">About</a>

&#x20;               <a class="nav-link" href="#">Contact</a>

&#x20;               <a class="nav-link" href="#">Sign up</a>

&#x20;           </div>

&#x20;       **</nav>**



***\*Main content is always positioned between <nav> and <footer> sections.\****



<!-- Main content -->

&#x20;       **<main>**

&#x20;           <!-- Hero section -->

&#x20;           <div class="hero-section">



*\*change the **</main>** tag also, below the form section\**



&#x20;<!-- Footer -->

&#x20;       **<footer** class="footer">

&#x20;           <div class="social-links">

&#x20;               <a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-facebook"></ion-icon>

&#x20;                   <p>Facebook</p>

&#x20;               </a>

&#x20;               <a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-instagram"></ion-icon>

&#x20;                   <p>Instagram</p>

&#x20;               </a>

&#x20;               <a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-linkedin"></ion-icon>

&#x20;                   <p>LinkedIn</p>

&#x20;               </a>

&#x20;               <a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-twitter"></ion-icon>

&#x20;                   <p>Twitter</p>

&#x20;               </a>

&#x20;           </div>

&#x20;       **</footer>**



*\*Replace certain <div> with <section>\**



<!-- Form section -->

&#x20;           **<section class=**"form-section">

&#x20;               <form>

&#x20;                   <h2 class="form-heading">What's Next?</h2>

&#x20;                   <p class="form-intro">Want pizza through your window?🍕 Receive a notification when the service is available.</p>

&#x20;                   <label for="name">Full name</label>

&#x20;                   <input class="input" id="name" type="text" placeholder="Ariana Regular" />

&#x20;                   <label for="email">Email</label>

&#x20;                   <input class="input" id="email" type="email" placeholder="ariana.regular@gmail.com" />

&#x20;                   <button class="submit-button" type="button" onclick="submitForm()">Notify me</button>

&#x20;               </form>

&#x20;           **</section>**



**<button** class="submit-button" type="button" onclick="submitForm()">Notify me**</button>**



**Easier navigation using assistive technologies like screen readers bc they can quickly identify these landmarks and provide shortcuts or navigation commands to jump directly to these sections. Returns time and effort enhancing efficiency.** 

**Using standard landmarks creates a predictable user experience.**



#### **Lists**

Continuation of applying descriptive tags to html

Either ordered or unordered, not just a bunch of repeating divs.



*Challenge:*

*1. Identify any connected consecutive items. Hint: There are multiple sections on our home page that should become 'lists'.*

*2. Update the sections to be unordered lists.*

*3. Wrap each item with a list item tag.*

*4. Finally, add the necessary CSS to maintain the style of the sections.*



&#x20;<!-- Navigation bar -->

&#x20;       <nav class="navbar">

&#x20;           <div class="logo">

&#x20;               <span class="iconify icon" data-icon="healthicons:drone-outline"></span>

&#x20;               <p class="logo-text">Skynet Eats</p>

&#x20;           </div>

&#x20;           **<ul** class="nav-links">

&#x20;               **<li>**<a class="nav-link" href="index.html">Home</a>**</li>**

&#x20;               **<li>**<a class="nav-link" href="#">About</a>**</li>**

&#x20;               **<li>**<a class="nav-link" href="#">Contact</a>**</li>**

&#x20;               **<li>**<a class="nav-link" href="#">Sign up</a>**</li>**

&#x20;           **</ul>**

&#x20;       </nav>



&#x20;**<ul** class="statistics">

&#x20;                   <img class="info-image" src="images/pal9000.jpg" alt="A flying Skynet drone." />

&#x20;                   **<li** class="stat">

&#x20;                       <h4 class="stat-heading">Drones🤖</h4>

&#x20;                       <p class="stat-number">+4000</p>

&#x20;                   **</li>**

&#x20;                   **<li** class="stat">

&#x20;                       <h4 class="stat-heading">Customers🧑🏽</h4>

&#x20;                       <p class="stat-number">+120 000</p>

&#x20;                   **</li>**

&#x20;                   **<li** class="stat">

&#x20;                       <h4 class="stat-heading">Cat conflicts🐱</h4>

&#x20;                       <p class="stat-number">\~70</p>

&#x20;                   **</li>**

&#x20;               **</ul>**



**Repeat for Footer** 

&#x20;   <!-- Footer -->

&#x20;       <footer class="footer">

&#x20;           **<ul** class="social-links">

&#x20;               **<li**><a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-facebook"></ion-icon>

&#x20;                   <p>Facebook</p>

&#x20;               </a>**<li>**

&#x20;               **<li>**<a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-instagram"></ion-icon>

&#x20;                   <p>Instagram</p>

&#x20;               </a>**<li>**

&#x20;               **<li>**<a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-linkedin"></ion-icon>

&#x20;                   <p>LinkedIn</p>

&#x20;               </a>**<li>**

&#x20;               **<li>**<a class="social-link" href="#">

&#x20;                   <ion-icon class="icon" name="logo-twitter"></ion-icon>

&#x20;                   <p>Twitter</p>

&#x20;               </a>**<li>**

&#x20;           **</ul>**

&#x20;       </footer>



*\*remove markers (bullet points) in CSS\**



ul {

&#x20;   list-style-type: none;

}



##### **Text Size**



.icon {

&#x20;   font-size: **2rem;**

}



***\*1rem is equal to 16px (default font size)\****



*Challenge: Change all font-size properties from px to rem.*



*Here's some helpful conversions for default settings:*

*1rem = 16px.*

*1.5rem = 24px.*

*2rem = 32px.*



.nav-link {

&#x20;   margin: 5px;

&#x20;   padding: 10px;

&#x20;   **font-size: 1rem;**

}



.hero-heading {

&#x20;   **font-size: 5rem;**

&#x20;   font-weight: 700;

&#x20;   margin: 0;

}



.hero-text {

&#x20;   **font-size: 1.25rem;**

&#x20;   max-width: 300px;

&#x20;   margin-bottom: 30px;

}



.info-heading {

&#x20;   **font-size: 3rem;**

&#x20;   margin: 0;

}



.stat-heading {

&#x20;   color: #cccccc;

&#x20;   **font-size: 1.25rem;**

&#x20;   font-weight: 500;

&#x20;   margin-bottom: 0;

}



.stat-number {

&#x20;   **font-size: 2.5rem;**

&#x20;   font-weight: 500;

&#x20;   margin-top: 0;

&#x20;   margin-bottom: 20px;

}



/\* Sign Up Form \*/

.form-heading {

&#x20;   **font-size: 3rem;**

&#x20;   margin: 0;

}



.form-intro {

&#x20;   **font-size: 1.25rem;**

&#x20;   margin-bottom: 20px;

}



.social-links p {

&#x20;   display: inline;

&#x20;   **font-size: 1rem;**

}



##### **Headings**

**RULES**

* ***Heading numbers should be consecutive***
* ***Use only one h1 per page***
* ***Apply them for structure, not style***



*Challenge: Apply headings correctly throughout the html. Make sure of the following:*

*1. There's one h1 heading. No more, no less.*

*2. Heading levels are not skipped.*

*3. Headings always introduce new content sections. A heading for some content should never be a <p> or a <div>.*



&#x20;<!-- Info section -->

&#x20;           <section class="info-section">

&#x20;               <div class="info">

&#x20;                   **<h2** class="info-heading">Food Delivery Service**</h2>**



&#x20; **<h3** class="stat-heading">Drones🤖**</h3>**

&#x20;                       <p class="stat-number">+4000</p>

&#x20;                   </li>

&#x20;                   <li class="stat">

&#x20;                       **<h3** class="stat-heading">Customers🧑🏽**</h3>**

&#x20;                       <p class="stat-number">+120 000</p>

&#x20;                   </li>

&#x20;                   <li class="stat">

&#x20;                       **<h3** class="stat-heading">Cat conflicts🐱**</h3>**

&#x20;                       <p class="stat-number">\~70</p>



#### **ARIA - Accessible Rich Internet Applications**

*\*Provides a way to make web applications and dynamic content more accessible* 

*to assistive technologies such as screen readers and voice recognition software.* 



*\*Helps fill in the gaps where HTML native semantics fall short.* 



**THE FIRST RULE OF ARIA IS DONT USE ARIA**

\--if you can use native HTML semantics, do so. 



**Use ARIA when:**

* You're creating a UI component that doesn't exist in HTML
* You need to provide additional information or context to AT



**Avoid using ARIA if:**

* Native HTML elements already do the job



&#x20;<div>

&#x20;       <button class="auth-button">Log in</button>

&#x20;       <div class="auth-button" **role="button" tabindex="0"**>Sign up</div>

</div>



*Challenge:*

*Add the three ARIA attributes that do the following:*

*1. Define the role of the toggle switch*

*2. Make the toggle switch keyboard-focusable*

*3. Communicate the state to assistive technologies in some way (on/off)*



<nav>

&#x20;           <a class="skip-nav-link" href="#main">Skip to main content</a>

&#x20;           <ul class="nav-items">

&#x20;               <li><a href="#">Home</a></li>

&#x20;               <li><a href="#">Haikus</a></li>

&#x20;               <li><a href="#">Rhymes</a></li>

&#x20;               <li><a href="#">About</a></li>

&#x20;               <li><a href="#">Contact</a></li>

&#x20;           </ul>

&#x20;           **<button id="toggleTheme" onclick="toggleTheme()" role="switch" aria-checked="false">Light Mode</button>**

&#x20;       </nav>



<nav>

&#x20;           <a class="skip-nav-link" href="#main">Skip to main content</a>

&#x20;           <ul class="nav-items">

&#x20;               <li><a href="#">Home</a></li>

&#x20;               <li><a href="#">Haikus</a></li>

&#x20;               <li><a href="#">Rhymes</a></li>

&#x20;               <li><a href="#">About</a></li>

&#x20;               <li><a href="#">Contact</a></li>

&#x20;           </ul>

&#x20;           **<button id="toggleTheme" onclick="toggleTheme()" role="switch" aria-checked="false">Light Mode</button>**

&#x20;       </nav>



##### **ARIA Live Regions** 

* part of a webpage marked as dynamically updated announced by screen readers. 
* include real time notifications.



**ARIA live settings**

* **aria-live="off"** (Assumed default so shouldn't be necessary to set explicitly.)
* **aria-live="polite"** (Most common. Any region that receives important updates but not so rapid to be annoying.)
* **aria-live="assertive"** (Used for time sensitive or critical notifications.)



**index.JS**

function sendMessage() {

&#x20;   // Get the button element

&#x20;   const button = document.getElementById('submitButton');

&#x20;   

&#x20;   // Replace the button with a paragraph

&#x20;   **button.outerHTML = '<p id="submitMessage" class="submit-message">Message sent! ✅</p>';**

&#x20;   

&#x20;   // Get the home link element and add focus to it

&#x20; }



*Here's your challenge:*

&#x20;*1. Update the code so that pressing the submit button 'politely' announces the new revealed submit message.*

&#x20;*2. Add focus to the home link when the user submits a message by selecting the correct element and adding ".focus()" to it.*



function sendMessage() {

&#x20;   // Get the button element

&#x20;   const button = document.getElementById('submitButton');

&#x20;   

&#x20;   // Replace the button with a paragraph

&#x20;   button.outerHTML = '<p id="submitMessage" class="submit-message" **aria-live="polite">**Message sent! ✅</p>';



###### **Programmatic Focus Management**

**Common Use Cases:**

* When opening models or menus
* After completing actions like form submissions
* To maintain a logical flow of navigation



*2. Add focus to the home link when the user submits a message by selecting the correct element and adding ".focus()" to it.*



&#x20;       <link rel="stylesheet" href="index.css">

&#x20;   </head>

&#x20;   <body class="contact-page">

&#x20;       <main id="main">

&#x20;           <div class="header">

&#x20;               <h2 class="contact-form-heading">Sign up</h2>

&#x20;               <a href="#main" **id="homeLink"**>Back to home page</a>

&#x20;           </div>



function sendMessage() {

&#x20;   // Get the button element

&#x20;   const button = document.getElementById('submitButton');

&#x20;   

&#x20;   // Replace the button with a paragraph

&#x20;   button.outerHTML = '<p id="submitMessage" class="submit-message" aria-live="polite">Message sent! ✅</p>';

&#x20;   

&#x20;   // Get the home link element and add focus to it

&#x20;   **document.getElementById('homeLink').focus();**

}



##### **Aside: Accessible JavaScript**

* Hover effect called **mouseover** or **mouseout**
* screen readers won't detect this 
* exclude users who use keyboards or touchscreens
* click events are generally accessible to mouse, keyboard, and touchscreen users. Similarly, focus and blur can effectively replace **mouseover** and **mouseout**
* For touchscreen users, events like **touchstart** can be used



**Much simpler and straightforward solution:**

* Take the warning message and put it into the flow of elements
* Remove event listener
* Check if all input fields are filled out



**REMOVE EVENT LISTENER:**

document.addEventListener('DOMContentLoaded', function() {

&#x20;   const submitButton = document.getElementById('submitButton');

&#x20;   const popoverMessage = document.getElementById('popoverMessage');



&#x20;   submitButton.addEventListener('mouseover', function() {

&#x20;       if (submitButton.disabled) {

&#x20;           popoverMessage.style.display = 'block';

&#x20;       }

&#x20;   });



&#x20;   submitButton.addEventListener('mouseout', function() {

&#x20;       popoverMessage.style.display = 'none';

&#x20;   });

});



**REPLACE WITH:**

&#x20;   if (allFilled) {

&#x20;       popoverMessage.style.opacity = '0';

&#x20;   }



&#x20;***\*\*Now able to remove a lot of CSS*** 



##### **Aside: Hiding Content**

* managing complex layouts like tab interfaces and menus



.chair-section {

&#x20;   **display: none;**

&#x20;   flex-direction: row-reverse;

}



**-VS-**



.chair-section {

&#x20;   **visibility: hidden;**

&#x20;   flex-direction: row-reverse;

}



*\*These both remove the content from the accessibility tree making it completely accessible to assistive technology users*



##### **Aside: Skip Navigation Link Part 1 (skip to main content)**

***DO:***

* left: 100%;
* transform: translate(100%,0);
* opacity: 0;



***DON'T:***

* display: none;
* visibility: hidden;
* <a **hidden**>Link</a>



*Challenge:*

*Make the link more accessible, as in make it an element that is more easily recognizable as a link.*



/\* Code for Skip Navigation Link goes here \*/

.skip-nav-link {

&#x20;   **border: 2px solid #333333;**

&#x20;   **padding: 8px 20px 8px 40px;**

&#x20;   **border-radius: 40px;**

&#x20;   position: absolute;

&#x20;   left: -200px;

&#x20;   top: 80px;

}



##### **Aside: Skip Navigation Link Part 2**

*Challenge:*

* *Apply the 'transition' property in our CSS so that the skip navigation link doesn't instantaneously appear and disappear.*
* *It should take 1 second to appear when focused, and 3 seconds to disappear when no longer focused. (Hint: You'll need to use the :focus pseudo-class.)*
* *Link to W3school's article on the transition property:* [*https://www.w3schools.com/css/css3\_transitions.asp*](https://www.w3schools.com/css/css3_transitions.asp)



/\* Code for Skip Navigation Link goes here \*/

.skip-nav-link {

&#x20;   border: 2px solid #333333;

&#x20;   padding: 8px 20px 8px 40px;

&#x20;   border-radius: 40px;

&#x20;   position: absolute;

&#x20;   left: -240px;

&#x20;   top: 80px;

&#x20;   **transition: 1s;** *(it will take one second to transition states)*

}

.skip-nav-link:focus {

&#x20;   left: -20px;

&#x20;   **transition: 3s;** *(won't quickly dissappear)*

}



##### **Skip Navigation Link**

*Challenge: Build your very own skip navigation link for our home page!*



*Requirements:*

*1. Its default state should be visually hidden yet accessible to all keyboard users.*

*2. It should utilize the transition property.*



*Steps:*

*1. In the HTML, place the link inside the nav, above the logo.*

*2. Give the link the class 'skip-nav-link'.*

*3. Give the main element the id 'main'*

*4. Give the skip nav link an href attribute linked to the main section.*

*5. Finally, apply your CSS to the class name 'skip-nav-link'.*





<!-- Navigation bar -->

&#x20;       <nav class="navbar">

&#x20;           **<a class="skip-nav-link" href="main">Skip to main content</a>**

&#x20;           <div class="logo">



&#x20;<!-- Main content -->

&#x20;       <main id=**"main"**>



/\* Skip Navigation Link \*/

.skip-nav-link {

&#x20;   border: 2px solid #333333;

&#x20;   padding: 8px 20px;

&#x20;   padding-left: 40px;

&#x20;   border-radius: 40px;

&#x20;   position: absolute;

&#x20;   left: -240px;

&#x20;   top: 80px;

&#x20;   transition: 3s;

}



##### **Final Challenge Part 1**

*Challenge:*

*Identify all accessibility issues using all your newly acquired knowledge.*



*Write them down here:*

\- Placeholder text has poor text contrast

\- Missing alternative text for images

\- Missing labels for input fields

\- Ambiguous button text

\- Semantic HTML is lacking

\- Font-sizes are defined in pixels rather than rem



##### **Final Challenge Part 2**

*Your final challenge:* 

*Use your new superpower to make our contact page accessible!🦸*



.contact-input::-webkit-input-placeholder, .contact-textarea::-webkit-input-placeholder {

&#x20;   **color: #555555**;



<!-- Form section -->

&#x20;           <div class="contact-form-section">

&#x20;               <form>

&#x20;                   <h2 class="contact-form-heading">Reach <span>Out</span></h2>

&#x20;                   <div class="contact-form-intro">Curious about something? Complete these fields and "get in touch", as you humans say. 🤙</div>

&#x20;                   <input class="contact-input" type="text" placeholder="Full name" />

&#x20;                   <input class="contact-input" type="text" placeholder="Email" />

&#x20;                   <textarea class="contact-textarea" rows="4" cols="50" placeholder="Your message..."></textarea>

&#x20;                   <button class="contact-submit-button" type="button" onclick="submitForm()">Done 🎉</button>

&#x20;               </form>

&#x20;               <img class="contact-image" src="images/connect.jpg" **alt="A robot hand and a human reaching for each other."** />



<div class="contact-form-intro">Curious about something? Complete these fields and "get in touch", as you humans say. 🤙</div>

&#x20;                   <label for="**name">Full name<**/label> 



<button class="contact-submit-button" type="button" onclick="submitForm()"**>Send message 🎉**</button>



**<main id="main">**

&#x20;           <!-- Form section -->

&#x20;           <div class="contact-form-section">

&#x20;               <form>

&#x20;                   **<h1** class="contact-form-heading">Reach <span>Out</span>**</h1>**

&#x20;                   <div class="contact-form-intro">Curious about something? Complete these fields and "get in touch", as you humans say. 🤙</div>

&#x20;                   <label for="name">Full name</label>

&#x20;                   <input class="contact-input" id="name" type="text" placeholder="Daniel Radcliffe" />

&#x20;                   <label for="email">Email</label>

&#x20;                   <input class="contact-input" id="email" type="text" placeholder="da.real.harry@gmail.com" />

&#x20;                   <label for="message">Message</label>

&#x20;                   <textarea class="contact-textarea" id="message" rows="4" cols="50" placeholder="Your message..."></textarea>

&#x20;                   <button class="contact-submit-button" type="button" onclick="submitForm()">Send message 🎉</button>

&#x20;               </form>

&#x20;               <img class="contact-image" src="images/connect.jpg" alt="A robot hand and a human reaching for each other." />

&#x20;           </div>

&#x20;       **</main>**



**.**contact-form-heading {

&#x20;   font-size: **3rem;**

&#x20;   font-weight: bold;

&#x20;   margin: 0;















































&#x20;   



































































































































































































































































