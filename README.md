This is very much a work in progress.

**Demo:** https://distracted-volhard-ea30bf.netlify.com/services/accounting

I posted earlier in another thread some thoughts about why I think this kind of tooling would be beneficial to Hugo Printing template lookup order and chosen template 1 - I could elaborate further if needed.

Much of the logic for printing the hugo variables is taken from here - https://github.com/kaushalmodi/hugo-debugprint/blob/master/layouts/partials/debugprint.html

Mainly I have jazzed that up with some nicer css and javascript. I’ve also briefly taken the time to curate the variables which are shown in a way I feel makes for a better user experience.

Currently the main issue, is that to display the currently chosen template, you must manually declare and pass the template name as an argument to the debug partial. And you must do this from within each layout file. This means that this solution requires a non trivial amount of setup work. It’s also a solution that is implemented at the theme layer, rather than a core feature of Hugo.

My hope would be that this could form the basis and inspiration for further work into a core debug bar for Hugo.
