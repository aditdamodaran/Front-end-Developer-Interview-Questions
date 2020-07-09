---
title: General Questions
layout: layouts/page.njk
permalink: /questions/general-questions/index.html
---

* What did you learn yesterday/this week?

  * Answer: Yesterday I learned [this CSS way](https://twitter.com/bdc/status/1245399999300558853) for centering things:

    ```css
    display: grid;
    place-items: center;
    ```

    Previously I had used both justify-content and align-content. 

  * Last week I learned about the amazing [Redux Dev Tools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd?hl=en) Chrome Extension, which I plan to use to visualize future React/Redux implementations.

* What excites or interests you about coding?

  * I like the power specifically with the web to write anything, anywhere, and ship it internationally to anyone at anytime. It's the first time in human history that we're capable of that.

* What is a recent technical challenge you experienced and how did you solve it?

  * I recently had difficulty with achieving fast site load speeds with Wordpress on top of other issues (like preferring my blog posts in Markdown format and improving SEO). I migrated my website to Gatsby by starting out with a boilerplate [Kaldi](https://gatsby-netlify-cms.netlify.app/), modifying it to be more modular (i.e. with component-specific SCSS preprocessing), and writing it entirely in Vanilla CSS and JavaScript (so I wouldn't need to rely on frameworks). The site achieved a 100/100 rating on PageSpeed Insights from Google, and I have complete control over its appearance and customization. 

* When building a new web site or maintaining one, can you explain some techniques you have used to increase performance?

  * Lazy-loading/progressive image loading is important. For this, I like Gatsby's [Sharp image processing library](https://www.gatsbyjs.org/packages/gatsby-plugin-sharp/), which automatically outputs smaller resolution versions of large images and only loads them fully when the user scrolls to them.
  * In the past I've made the mistake of designing landing pages that have large background images in PNG format with extreme detail [Midway Ventures](https://www.midwayvc.com/). I'm much more careful about background hero images nowadays, and also wary of going overboard with high-resolution images and animations. SVG formats tend to load faster, and PNGs should be used sparingly (and definitely not as the primary background hero). Either way, I've used lossless compression to minimize image sizes.
  * I use Webpack to minify JS and CSS.

* Can you describe some SEO best practices or techniques you have used lately?

  * Meta tags in your HTML (especially for example the meta:description tag) and alt-text for images. I use [react-helmet](https://www.gatsbyjs.org/packages/gatsby-plugin-react-helmet) in my Gatsby site.
  * Making the website load quickly improves page ranking performance. 

* Can you explain any common techniques or recent issues solved in regards to front-end security?

  * I heard many issues in the Wordpress community stemmed from vulnerable dependencies. Avoiding such dependencies is a good start. There's a great reference [here](https://github.com/qazbnm456/awesome-web-security) that covers web security in greater detail.

* What actions have you personally taken on recent projects to increase maintainability of your code?

  * I believe in modularizing my code. I haven't used [component-specific styles](https://styled-components.com/) as a plugin, but I create .scss files specific to the components I am working on. I also try to make my components as reusable as possible, and comment everything I do. In prior jobs, I have used Storybook (from Airbnb) for documenting my components and their capabilities. However, it's important to balance maintainability with speed of development. 

* Talk about your preferred development environment.

  * (varies)

* Which version control systems are you familiar with?

  * I like Git and I've used Subversion (SVN) in academic classes at UChicago. But I prefer Git with tracking in Gitlab/Github and JIRA. 

* Can you describe your workflow when you create a web page?

  * Well it differs depending on the architecture of the larger application. But generally I create Navigation and Footer components, and then figure out which components on my webpage I might reuse on other pages. Once I've determined the components I'll be using, I start with the bare bones of the application/web page, getting them to communicate to each other with the right data. After the correct data is being sent to each component depending on its context, I start writing more in-depth HTML tags and attributes that will provide the skeleton for my CSS. I create individual SCSS/LESS stylesheets for each component (later to be compiled together), and style the webpage. I usually use something akin to BrowserSync to responsively test my styles for both mobile and desktop screens.

* If you have 5 different stylesheets, how would you best integrate them into the site?

  * In order of specificty. Least specific first (i.e. global styles), and most specific last (i.e. component specific styles and media queries). They'd be integrated in a manner that minimizes the overwriting of styles.

* Can you describe the difference between progressive enhancement and graceful degradation?

* How would you optimize a website's assets/resources?

* How many resources will a browser download from a given domain at a time?
  
  * What are the exceptions?
  
* Name 3 ways to decrease page load (perceived or actual load time).

* If you jumped on a project and they used tabs and you used spaces, what would you do?

* Describe how you would create a simple slideshow page.

* If you could master one technology this year, what would it be?

* Explain the importance of standards and standards bodies.

* What is Flash of Unstyled Content? How do you avoid FOUC?

* Explain what ARIA and screenreaders are, and how to make a website accessible.

* Explain some of the pros and cons for CSS animations versus JavaScript animations.

* What does CORS stand for and what issue does it address?

* How did you handle a disagreement with your boss or your collaborator?

* What resources do you use to learn about the latest in front end development and design?

* What skills are needed to be a good front-end developer?

* What role do you see yourself?

* Explain the difference between cookies, session storage, and local storage?
