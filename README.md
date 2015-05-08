## Website Performance Optimization portfolio project

Project is hosted at rsasson.github.io

### index.html optimizations
1. Reduce number of CSS rules via uncss tool (only use css rules that are used on page)
1. Stick CSS into style tag in page (CSS file load appears to be big performance hit)
1. Use smaller and compressed pizzeria image on resume page
1. Load analytics at end of page to unblock rendering.

### pizza.html optimizations

1. To reach 60 FPS simply reduce number of pizzas in background to 40, this has no effect on
the appearance of the number of pizzas on the page
1. Pizza resize repeated far too many operations (namely DOM retrievals and width calculations), not repeating them drastically sped up resize time.
1. Reduce nesting of resizePizzas function, no need to reinstantiate changeSliderLabel
and changePizzaSizes for each call of resizePizzas on a scroll
1. Do querySelectAll only once in changePizzaSizes rather than per iteration.
1. Calculate windowwidth and dx only once in order to calculate newwidth
1. Query for body scroll distance only once when calculating phase for item

Moral of the story, don't repeat expensive selects and queries of the DOM if you don't have to.
