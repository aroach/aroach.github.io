---
layout: post
title: Tips on Getting Started with React
---

I've been working on a new Node project.  As a fairly longtime Angular 1 user, and after looking at Angular 2, I decided to try out React for the front-end. While React seems pretty straightforward, I'd say it's actually not.

So here goes. I've tried to compile my opinions based on how my brain works for getting started with React.  If you find this post, I hope it will save you some time Googling for examples and tutorials.

***The first project to know about is the [Create-react-app](https://github.com/facebookincubator/create-react-app).*** This is a generator for creating a React app.  It was created by Facebook, and has tons of features.  Of its benefits, it seems to allow you to skip setting up webpack.  I started with this and so far haven't come across any limitations or issues.  (Famous last words.)  A couple of standout sections from the readme are:

* [Serving Apps with Client-Side Routing](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#serving-apps-with-client-side-routing).  I learned that in a Node app you can put your fallback route after routes you want to serve.  For example, I wanted to serve my REST API on `/api`, but allow the client to handle the rest of the requests.  So, I just needed to order my `app.get('/api', function(req, res){...});` statements with `app.get('/*', function(req, res){...});` as the last one to match.
* [Proxying API Requests in Development](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#proxying-api-requests-in-development).  Since I have an API and client served up by the same app, I really needed this.
* [Adding Custom Environment Variables](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-custom-environment-variables)  Note that this does a replace as opposed to a runtime substitution since React projects are built artifacts.

***Bite the bullet and learn [Redux](http://redux.js.org/).*** At first, I thought that I didn't need something like Redux to manage application state globally.  Once you get your head around `connect`, `mapStateToProps()`, and so on, having a global state store made React much easier to deal with for me. Of course, it all depends on the complexity of your app.  Here are a few Redux video series and tutorials that I found invaluable:

These videos are from the founder of Redux, Dan Abramov, and they are excellent:

* [Part 1: Getting Started with Redux](https://egghead.io/series/getting-started-with-redux)
* [Part 2: Building React applications](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)

Kurt Weiberth has created his own [tutorial series on React + Redux](https://www.youtube.com/playlist?list=PLQDnxXqV213JJFtDaG0aE9vqvp6Wm7nBg), and while I watched these before the series by Dan (I think you should start with Dan's perhaps), Kurt's are really helpful as well!

[React+Redux Real World Example](https://github.com/gothinkster/react-redux-realworld-example-app): As you might observe, the Redux examples above deal with a Todo list app, and while I recently discovered the second part of Dan's tutorials are more real world, I found this "real world" example to be helpful as well.

[Creating a CRUD React+Redux](http://www.thegreatcodeadventure.com/building-a-simple-crud-app-with-react-redux-part-1/) was the example I followed when first deciding to try out Redux.  There is a lot of good information in Sophie's posts, but I think I would've understood things better had I reviewed Dan's series before checking this one out.

I felt like the nature of my app needed client-side routing.  Part of this was probably based on my experience with Angular.  As a result, ***I encourage you to check out [React Router 2.x](https://github.com/ReactTraining/react-router/blob/v2.8.1/docs/guides/README.md).*** It's definitely different than how Angular's ngRoute or ui-router work, and so it helped me to find examples.

I started with React Router 4, which was brand-spankin' new.  I managed to get a version of my app using version 4, however I found that there are VERY FEW examples that use version 4.  I ended up downgrading to 2.7, since most of the examples and tutorials I came across used version 2.x. If you do want to use version 4, I came across one example that was in a blog post, and reached out to the author [@bodiddlie](https://twitter.com/bodiddlie) and he [tweeted the link to his github repo](https://twitter.com/bodiddlie/status/852271980879396865). Sophie's cat catalog (the CRUD example above) also uses react router 2.x. 

Finally, I need to invest some more time in ***testing of React and Redux***, and found [this article](https://medium.com/javascript-inside/some-thoughts-on-testing-react-redux-applications-8571fbc1b78f) provided a nice practical summary on ways to test.

Many thanks to everyone who’s put up examples, docs, and tutorials!
