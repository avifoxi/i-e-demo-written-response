The list of desired points + features you've written is great -- 

but I think the biggest challenge is choosing which of these points to compromise on.
Because we will certainly not find a framework that satisfies ALL of the points. 
But we might have a few options of frameworks that satisfy MOST of the points. 

Stability: 
Unfortunately... JS frameworks are not very stable, by their very nature.
And if we commit to a specific release of a framework, we may have problems if we need to migrate at some point in the future. 

Improves Performance:
Honestly -- any framework will likely improve performance, both in developer time of production, and in user ease. 

Given the description you've shared so far --
I would lean towards React. 

First -- let me address the goals it does NOT satisfy:
- React is unstable. It's a newer kid on the block, and is not even at release 1.0 yet. So things will change. 
- React does not support our existing workflow. Integrating React into a production environment will certainly take some re-tooling. Developers will need to learn a new build process, and the server may need to incorporate the JSX transform. There will certainly be some trial and error. 

BUT -- 
for all of the other points, React seems to excel.

React Virtual Dom keeps dom rewrites to a minimum, and the user benefits from this speed and ease.
React seems to be very maintainable - and very flexible for large teams to collaborate on. The data flow model makes sense, and as components are modular and function based, they can be reassembled and recomposed very easily. 

The developers WILL need to learn a new DSL, but once they learn the key concepts ( and I expect it will happen more quickly than for angular, for exp ), the workflow is pretty straightforward. Changes in app state are well tracked, and it is easy to move a component's state from 'loading', to 'loaded', to 'removed from DOM'. 

React's community is very enthusiastic -- and with tools like the Babel transpiler, it pushes developers to write ES6, and write better code, while still maintaining backwards compatibility for old browsers. 

So -- I would clearly push the team to consider React, and evaluate whether the design and performance benefits are worth the revised workflow + learning process. 

