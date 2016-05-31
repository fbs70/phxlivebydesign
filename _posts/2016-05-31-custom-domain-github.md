---
layout: post
kind: post
title: Using a Custom Domain on Github
date:   2016-05-31 09:55:00 -0500
categories: jekyll update
---
I personnally always host my jekyll sites on custom domain names, so I will host that example on <http://jekyll-bower-example.fbs70.com> instead of <http://fbs70.github.io/jekyll-bower-example/>.

That way I don't need a `baseurl` setting and this setup works the same for development and for production. If you really need to keep the `baseurl` setting then you should probably create a new 'production specific' grunt task that will build jekyll with the `--baseurl URL` option.

So, first you need to comment the `baseurl` setting in the `_config.yml` file:

    # baseurl: "/jekyll-bower-example"

Then create a `CNAME` file with the custom domain name:

    jekyll-bower-example.aymerick.com

Finally go to your DNS provider website and setup a `CNAME` from `jekyll-bower-example.fbs70.com` to `fbs70.github.io`.

And now, browse to <http://jekyll-bower-example.fbs70.com>.

You should probably see a `404 There isn't a GitHub Page here.` error, that's because it takes some time for github to setup your new custom domain configuration. Just wait a few minutes then try again, you will eventually see your site.
