## Website Performance Optimization portfolio project

Project is hosted at rsasson.github.io

### index.html optimizations
1. Reduce number of CSS rules via uncss tool (only use css rules that are used on page)
1. Stick CSS into style tag in page (CSS file load appears to be big performance hit)
1. Use smaller and compressed pizzeria image on resume page
1. Load analytics at end of page to unblock rendering.

### pizza.html optimizations

1. To reach 60 FPS simply reduce number of pizzas in background
1. Pizza resize repeated far too many operations (namely DOM retrievals and width calculations), not repeating them drastically sped up resize time.
