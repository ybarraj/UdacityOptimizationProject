## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

####Part 1: My Optimizations

To complete this project I started by resizing the images on the main page. I did this by configuring a grunt task to run though all the images and give me a few different sizes of each. I also added a media query to my print CSS so that it would no longer be render blocking for normal viewing. I then inlined my CSS and used a trick from CSS Tricks to get my Google font to stop rendering blocking. 

In order to run the optimized page through page speed insights you can access the page here: https://ybarraj.github.io/UdacityOptimizationProject/

####Part 2: Optimize Frames per Second in pizza.html

For the pizza sizes section I created three cases and instead of mixing px with percentages I just used percentages to get it to render more quickly. 

To fix the update to pizza locations I First changed the amount of pizzas that were being painted down from 200 to 30. This alone made a large difference in loading time. Then I used a more specific calling mechanism and accessed the DOM outside of the loop rather than inside the loop. 

The Time it takes to resize a pizza is under 1 ms. I average 60fps on scrolling. My page speed insights scores are 96 on desktop and 94 on mobile. 
