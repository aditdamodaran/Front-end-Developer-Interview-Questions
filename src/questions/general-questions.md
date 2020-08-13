---
title: General Questions
layout: layouts/page.njk
permalink: /questions/general-questions/index.html
---

* **What did you learn yesterday/this week?**

  * Answer: Yesterday I learned [this CSS way](https://twitter.com/bdc/status/1245399999300558853) for centering things:

    ```css
    display: grid;
    place-items: center;
    ```

    Previously I had used both justify-content and align-content. 

  * Last week I learned about the amazing [Redux Dev Tools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en) Chrome Extension, which I plan to use to visualize future React/Redux implementations.

* **What excites or interests you about coding?**

  * I like the power specifically with the web to write anything, anywhere, and ship it internationally to anyone at anytime. It's the first time in human history that we're capable of that.

* **What is a recent technical challenge you experienced and how did you solve it?**

  * I recently had difficulty with achieving fast site load speeds with Wordpress on top of other issues (like preferring my blog posts in Markdown format and improving SEO). I migrated my website to Gatsby by starting out with a boilerplate [Kaldi](https://gatsby-netlify-cms.netlify.app/), modifying it to be more modular (i.e. with component-specific SCSS preprocessing), and writing it entirely in Vanilla CSS and JavaScript (so I wouldn't need to rely on frameworks). The site achieved a 100/100 rating on PageSpeed Insights from Google, and I have complete control over its appearance and customization. 

* **When building a new web site or maintaining one, can you explain some techniques you have used to increase performance?**

  * Lazy-loading/progressive image loading is important. For this, I like Gatsby's [Sharp image processing library](https://www.gatsbyjs.org/packages/gatsby-plugin-sharp/), which automatically outputs smaller resolution versions of large images and only loads them fully when the user scrolls to them.
  * In the past I've made the mistake of designing landing pages that have large background images in PNG format with extreme detail [Midway Ventures](https://www.midwayvc.com/). I'm much more careful about background hero images nowadays, and also wary of going overboard with high-resolution images and animations. SVG formats tend to load faster, and PNGs should be used sparingly (and definitely not as the primary background hero). Either way, I've used lossless compression to minimize image sizes.
  * I use Webpack to minify JS and CSS.

* **Can you describe some SEO best practices or techniques you have used lately?**

  * Meta tags in your HTML (especially for example the meta:description tag) and alt-text for images. I use [react-helmet](https://www.gatsbyjs.org/packages/gatsby-plugin-react-helmet) in my Gatsby site.
  * Making the website load quickly improves page ranking performance. 

* **Can you explain any common techniques or recent issues solved in regards to front-end security?**

  * I heard many issues in the Wordpress community stemmed from vulnerable dependencies. Avoiding such dependencies is a good start. There's a great reference [here](https://github.com/qazbnm456/awesome-web-security) that covers web security in greater detail.

* **What actions have you personally taken on recent projects to increase maintainability of your code?**

  * I believe in modularizing my code. I haven't used [component-specific styles](https://styled-components.com/) as a plugin, but I create .scss files specific to the components I am working on. I also try to make my components as reusable as possible, and comment everything I do. In prior jobs, I have used Storybook (from Airbnb) for documenting my components and their capabilities. However, it's important to balance maintainability with speed of development. 

* **Talk about your preferred development environment.**

  * (varies)

* **Which version control systems are you familiar with?**

  * I like Git and I've used Subversion (SVN) in academic classes at UChicago. But I prefer Git with tracking in Gitlab/Github and JIRA. 

* **Can you describe your workflow when you create a web page?**

  * Well it differs depending on the architecture of the larger application. But generally I create Navigation and Footer components, and then figure out which components on my webpage I might reuse on other pages. Once I've determined the components I'll be using, I start with the bare bones of the application/web page, getting them to communicate to each other with the right data. After the correct data is being sent to each component depending on its context, I start writing more in-depth HTML tags and attributes that will provide the skeleton for my CSS. I create individual SCSS/LESS stylesheets for each component (later to be compiled together), and style the webpage. I usually use something akin to BrowserSync to responsively test my styles for both mobile and desktop screens.

* **If you have 5 different stylesheets, how would you best integrate them into the site?**

  * In order of specificty. Least specific first (i.e. global styles), and most specific last (i.e. component specific styles and media queries). They'd be integrated in a manner that minimizes the overwriting of styles.

* **Can you describe the difference between progressive enhancement and graceful degradation?**

  * Progressive enhancement is developing for *all browsers (regardless of how old they are)* with a set of fundamental features that need to work, then adding additional functionality to improve user experience on newer browsers. 
  * Graceful degradation is the opposite. You develop full functionality on newer/modern browsers and technologies, then "degrade" it to work (as much as possible) on older browsers.
  * I mostly develop with a graceful degradation mindset because I am not creating large-scale web applications that will be used by millions of people (yet).

* **How would you optimize a website's assets/resources?**

  * There are some great tools nowadays for doing that such as Babel for transpiling and Webpack for bundling. I'd include those in my dev environment. That tends to work for most startup applications, but if you're trying to optimize a massive website accessed by millions of people, [Facebook has a great blog post about how they did it.](https://engineering.fb.com/web/facebook-redesign/) 
  * To summarize:
    * Optimize and bundle CSS individually by component during the build process
    * generating [atomic CSS](https://css-tricks.com/lets-define-exactly-atomic-css/) at build time
    * Component scoped CSS to reduce redundancy and accidental style overwrites 
    * inline SVGs into HTML
    * Incrementally download JavaScript, prioritize visible assets, handle subscriptions and other more costly operations after a page's assets are fully visible
    * only load in data that wll be used -- limit background operations until you know the user will see your data (an example of this is [Gatsby-Plugin-Sharp](https://www.reddit.com/r/gatsbyjs/comments/e3j72j/what_does_gatsbypluginsharp_do_exactly/), which lazy loads and blurs pictures until they are scrolled to). Facebook uses a more fine-grained GraphQL extension "stream"
    * Prefetch as early as possible -- Facebook prefetches the data for a given link as early as hovering on that link!

* **How many resources will a browser download from a given domain at a time?**
  
  * [Answered nicely here.](https://stackoverflow.com/questions/7456325/get-number-of-concurrent-requests-by-browser) To summarize:
    * 6
  * **What are the exceptions?**
    * Internet Explorer ranges. The latest (IE11 => 13)
  
* **Name 3 ways to decrease page load (perceived or actual load time).**

  * There are quite a few answers above that would work for this question.

* **If you jumped on a project and they used tabs and you used spaces, what would you do?**

  * Use whatever the project uses

* **Describe how you would create a simple slideshow page.**

  * Load all the images you need into an HTML array (array of divs, img tags, etc.), then use CSS (translate mostly) to switch between images on arrow click (JavaScript to handle the click event)

* **If you could master one technology this year, what would it be?**

  * Node.js. I'd like to make the leap from frontend to full-stack

* **Explain the importance of standards and standards bodies.**

  * Everyone works with a uniform set of guidelines and protocols. This enables truly global applications. Standards bodies must be independent.

* **What is Flash of Unstyled Content? How do you avoid FOUC?**

  * HTML loads before the CSS that styles it. [Stefan's answer here works well](https://stackoverflow.com/questions/3221561/eliminate-flash-of-unstyled-content).

* **Explain what ARIA and screenreaders are, and how to make a website accessible.**

  * Screenreaders "read" the text of a webpage or application out loud for visually impaired or otherwise disabled users. Accessible Rich Internet Applications **(ARIA)** is a set of attributes that define ways to make web content and web applications (especially those developed with JavaScript) more accessible to people with disabilities.

* **Explain some of the pros and cons for CSS animations versus JavaScript animations.**

  * JavaScript may be disabled in some browsers and tends to be much more costly in the browser. CSS is the best when possible.

* **What does CORS stand for and what issue does it address?**

  * Cross Origin Resource Sharing. CORS allows you to make requests from one website to another website in the browser, which is normally prohibited by another browser policy called the Same-Origin Policy (SOP). [More on it here.](https://medium.com/@electra_chong/what-is-cors-what-is-it-used-for-308cafa4df1a) Before browsers implemented SOP, malicious websites were able to exploit cookies stored by your browser to make unauthorized requests to other domains. Some of these unauthorized requests could do things like make purchases, delete user information, fetch sensitive data, etc. 

* **How did you handle a disagreement with your boss or your collaborator?**

  * I haven't had a serious one to date. It would depend on the situation, but usually a one-on-one discussion where each person outlines how time-sensitive their objectives are and what their current and futuree priorities are works wonders.

* **What resources do you use to learn about the latest in front end development and design?**

  * I really like following a Udemy tutorial to get my bearings on a new technology, then building out my own project with blogs and various docs for reference. I usually get the "latest" by following engineering blogs from large tech companies (i.e. Facebook and AirBnb) and developers on Twitter.

* **What skills are needed to be a good front-end developer?**

  * <u>A growth mindset.</u> Willingness to constantly learn new technologies.
  * Caring about the end-user (more specifically, knowing how they might interact with your application/website and what information/service they want from it).
  * Having an eye for design.
  * Desire to make things accessibile for all users.
  * Not hijacking the user's scroll (or pulling similar antics).

* **What role do you see yourself?**

  * (varies). Ultimately I want to build something truly world-class.

* **Explain the difference between cookies, session storage, and local storage?**

  * [See here](https://miro.medium.com/max/2100/1*dMoXCZgsdlQoSITo5BdXoA.png).
    * Cookies = Stores data that has to be sent back to the server with subsequent XHR requests. <4KB only.
    * Local Storage = Not secure string data, but <5MB stored on User's laptop *forever* (or until it's cleared)
    * Session Storage = stores data only for a session, meaning that the data is stored until the browser (or tab) is closed (storage limit is about 5-10MB)
