You are developing for a product - there seems to be a discussion in a group of your team that developed the new analytics feature for the product, and they realized some shortcomings while doing so. One of the developer approaches you with the github issue below, and asks you for comments

#### Building Product’s Analytics
In January, we started building the Analytics section for the Product. 
Our options were: using Angular.js, Chaplin.js or writing our own library. 
We decided to write our own library based on some older js library we had from another project

#### Product's initial Front-End Approach
The approach we took when building the custom library for analytics was:
- Simple
- Quick to write
- Modular (initializing some sort of view on top of the HTML elements that represent that element – think about this way: a form in html becomes a form view. a collection of buttons could be come a buttons view and so on. This can be as granular as it needs to be)
- used static .html (no models & templating)
- rendered HTML on the server via twig.
- Allowed us to move quite fast (we could spend some time on style guide and general workflows.)
- Slightly interactive
 - The most interactive things where a “matching data from attributes to the correct URL”
- navigation and loading partials for performance sensitive parts of the app

#### Running into problems with our framework
After a first release, we ran into challenges when we started implementing forms in modals in combination with steps. As we did not use any models (data store or state) in the javascript we had to build time consuming workarounds to deal with forms that had to be rendered on page load by the server without knowing what they would update once they’re displayed in one of the later steps.

Things became more complicated with added features like modals with forms inside cards, where cards also could have a number of different states like _loading_ and _deleted_.

Some of these cards could even load __more__ cards, which in turn could have their own click handlers for more modals, states and other functionality. We reached a point where we could safely say our _framework_ was never meant to do this.

#### Next steps
Adding new features to our product will requires a lot of time to make work, which leads to longer turnaround times.

#### Lets use an existing framework
Moving data/state and templating to the browser and communicating to the backend through a json api (which the core of the backend mostly supports already) will be the biggest and most important changes.

We are looking for a framework that...
- Focuses on Stability
- Improves Performance
- Is easily Maintainable
- Is user-friendly
- Is easier on the developers nerves

The team’s plan is to move to a javascript framework that...
- has an active community
- is used in similar products
- has a good structure
- supports our existing workflows

Now, we _just_ have to decide which framework to use with which tools…