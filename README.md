# Hugo Debug Bar

Very much a work in progress, attempting to create a developer tool for Hugo themers. 

**Demo:** https://distracted-volhard-ea30bf.netlify.com/services/accounting

Much of the logic for printing the hugo variables is taken from here - https://github.com/kaushalmodi/hugo-debugprint/blob/master/layouts/partials/debugprint.html

Mainly I have jazzed that up with some nicer css and javascript. I’ve also briefly taken the time to curate the variables which are shown in a way I feel makes for a better user experience.

Currently the main issue, is that to display the currently chosen template, you must manually declare and pass the template name as an argument to the debug partial. And you must do this from within each layout file. This means that this solution requires a non trivial amount of setup work. It’s also a solution that is implemented at the theme layer, rather than a core feature of Hugo.


## Reasoning

I really think that one of Hugos strength is it’s stricter content and layout paradigm. But the template lookup order is opaque. It is not immediately intuitive how markdown files will map to layouts and this can lead to a lot of frustration when trying to create pages and hook them into the correct templates.

I imagine most new Hugo users can relate to the process of randomly moving and renaming markdown and layout files until you find a ‘match’. Even after you’ve got it working, you are most likely still baffled by the magic of the templating system and quickly tell yourself "next time i’ll figure it out properly’

More developer tools to surface the lookup order and how different content structures map to the layouts would be a huge win for Hugo.

### Discussions

- https://discourse.gohugo.io/t/printing-template-lookup-order-and-chosen-template/17688
- https://discourse.gohugo.io/t/prototyping-a-hugo-debug-bar/17691
