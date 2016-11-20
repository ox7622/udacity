## Website Performance Optimization portfolio project

####Part 1: Optimize PageSpeed Insights score for index.html
First of all open index.html in your browser 
To make optimization happen I reviewed the timeline and noticed there was 2 links to stylesheets.
When I fixed that the whole page started rendering much quicker.
Then I pasted the stylesheet directly into the webpage at the end of the code.
To avoid block rendering I put Js for Google analytics separately and added async tag. I also added another stylesheet with media query of max-width of 480px.

####Part 2: Optimize Frames per Second in pizza.html

The main thing that influenced bad performance of the pizza page was that every time I scrolled the page should have repainted and changed it's layout. 
I changed the quantity of pizzas to 50 as it's a maximum amount of them the viewer can see. To make optimize animation I amended updatePoistions function by get the scrollTop event outside the loop to make it render once, not for every pizza.
Also I changed querySelector to getElementById/getElementsByClassName as more efficient option to grab selectors.
Another optmization was to initialize variable outside the loops - for elem and phase variables, and also call the length property outside of loops.

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
