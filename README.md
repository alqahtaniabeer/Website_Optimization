## Website Performance Optimization project

## How to run the app :

* Download the app
* Open the index.html and pizza.html with your favorite browser.

```
These are the optimizations I've made:
```

#### Part 1: Optimize PageSpeed Insights score for index.html

1. Minified style.css and perfmatters.js
2. used a media query by added 'media = "print" ' to print.CSS
3. Added "async" to google analytics and ajax
4. Resized images 
5. Deleted external font link and inlined font API
6. Inlined style.css into index.html


#### Part 2: Optimize Frames per Second in pizza.html

1. Use requestAnimationFrame for updatePositions.

2. In updatePositions() 
	a. I Moved items declaration and document.body.scrollTop outside of the function's for loop. 
	b. I Moved window.performance.mark("mark_start_frame"); after the for loop 
	c. I also Separated original for loop into two for loops.

3. In changePizzaSizes()
	a. Removed newwidth from for loop and created switch-case to determine size. 
	b. Created pizzaContainer variable to calculate document.getElementsByClassName("randomPizzaContainer") outside of for loop
	c. Changed querySelectorAll to getElementsByClassName.
	d. Move pizzasDiv = document.getElementById("randomPizzas") out of a loop because it will select the same element in every iteration

4. Minified style.css and main.js

5. Resized images
