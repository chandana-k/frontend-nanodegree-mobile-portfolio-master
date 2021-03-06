Website Optimization:

1. PageSpeed Score: 
index.html achieved the following PageSpeed scores:

Scores Screenshot:  
Desktop Optimization Score: 91  
![Desktop Pagespeed Screenshot](./img/pagespeed-desktop-optimization.png)  
Mobile Optimization Score: 99  
![Mobile Pagespeed Screenshot](./img/pagespeed-mobile-optimization.png)  

2. Getting Rid of Jank:
Optimizations were made to views/js/main.js make views/pizza.html render with a consistent frame-rate at 60fps when scrolling:

FPS Screenshot:  
![FPS Screenshot](./img/pizza-html-fps.png)  
Time to resize pizzas was less than 5 ms using the pizza size slider on the views/pizza.html page. 

Resize Time Screenshot:  
![Resize Time Screenshot](./img/pizza-html-resize-time.png)  

Steps followed:

PART 1:
1. Checked out the Udacity repository
2. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8081
  ```

3. Open a browser and visit localhost:8081
4. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8081
  ```
5. Copy the public URL ngrok gives you and try running it through PageSpeed Insights


Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

Optimization Tips and Tricks
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

Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

<a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
<a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
