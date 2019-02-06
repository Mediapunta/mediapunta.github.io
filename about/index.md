---
layout: page
title: About
navigation: true
logo: 'assets/images/ghost.png'
current: about
---

This is a demo blog for Ghost, it contains dummy content which allows you to click around and see what a Ghost blog running the default theme looks like.

We use this for testing and for reference!

If you'd like to set up your own blog, head on over to [https://ghost.org](https://ghost.org) and sign up.

<!-- < default -->
<!-- The tag above means - insert everything in this file into the [body] of the default.hbs template -->

<!-- The big featured header  -->
<header class="main-header {% if page.cover %}"
        style="background-image: url({{ site.baseurl }}{{ page.cover }}) {% else %}no-cover{% endif %}">
    <nav class="main-nav overlay clearfix">
        {% if page.logo %}<a class="blog-logo" href="{{ site.baseurl }}"><img src="{{ site.baseurl }}{{ page.logo }}" alt="Blog Logo" /></a>{% endif %}
        {% if page.navigation %}
            <a class="menu-button icon-menu" href="#"><span class="word">Menu</span></a>
        {% endif %}
    </nav>
    <div class="vertical">
        <div class="main-header-content inner">
            <h1 class="page-title">{{ site.name }}</h1>
            <h2 class="page-description">{{ site.description }}</h2>
        </div>
    </div>
    <a class="scroll-down icon-arrow-left" href="#content" data-offset="-45"><span class="hidden">Scroll Down</span></a>
</header>

<!-- The main content area on the homepage -->
<main id="content" class="content" role="main">

    <!-- The tag below includes the post loop - partials/loop.hbs -->
    {% include loop.html %}

</main>
