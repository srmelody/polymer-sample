Things to remember:
Make sure you use propertyChanged listener (for published property foo, add a fooChanged) to the components if you have computed a property of the component based on published properties (attributes) that might change.

To incorporate bootstrap into components, I used a relative link in the components and had vulcanize not inline these.  I could have used a Sass import as well, but I think that would have been harder to not inline since the CSS generated from the Sass source is inlined into the components.

Open questions:
* Can vulcanized use a min version of a shared CSS or a link to a CDN URL instead of inlining all the styles in an import?  I was only able to get this to work with an externally hosted CSS, but it looks possible to take the shared.css (which is actually not being used) and inline that into the component.
