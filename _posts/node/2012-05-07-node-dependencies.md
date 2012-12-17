---
layout: page

title: Node dependencies
tags:
- Javascript
- Node.js

---

# Describing package.json

For every Node.js application you want to deploy on the Clever Cloud, you need
to provide a `package.json` file at the root of your project’s directory.

The package.json should *at least* contain the following fields:

{% highlight javascript%}
    {
        "main" : "myapp.js",
        "scripts" : {
            "start" : "node myapp.js"
        },
        "engines" : {
            "node" : ">=0.6"
        }
    }
{% endhighlight %}

**main**
: Should be the relative path to the main file we will start using node.

**scripts.start**
: If you prefer something more complicated, just provide a `script.start` field *instead of* the `main` one.

**engines.node**
: Sets the node engine version you app runs with. Any ">=" version will lead to run the application with the latest local version (which will be updated to the latest version at the moment).

More help about the package.json file at <a href="http://package.json.nodejitsu.com/">http://package.json.nodejitsu.com/</a>.