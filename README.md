# Modern Material

A modern Material Design theme based on Material Design Components.
Demo: <https://francesco.brozzu.xyz>

## Key features

Can create pages that filter by tag by following the schema in projects.html.

```
<div class="posts-list">
        {% for post in site.posts %}
        {% if post.categories contains "projects" %}
            {% include post_preview.html %}
        {% endif %}
    {% endfor %}
</div>
```

To show an item in the menu set the active tag with the name you prefer.

## Installing

In order to have the material design stylesheet with custom colors it is necessary to manually build the CSS file using dart-sass. First install the required dependencies using 

```
npm install
```

Then edit the colors as you wish in `material_config.scss`. 

Build the file using dart-sass and store it in Jekyll's assets.

```
node_modules/.bin/sass -I node_modules -s compressed material_config.scss > assets/css/material.css
```

Now if you already have bundler installed you should be able to get all the required dependencies for Jekyll with

```
bundler install
```

To test your website locally simply run:

```
bundle exec jekyll serve --host=127.0.0.1
```

To build your website
```
bundle exec jekyll build
```

Your built website is now ready in the _site folder. Remember to set the correct url and host parameters before building.

## Customizing CSS ##

You can add custom CSS elements in _sass/main.scss.

## Customizing header images

To customize the headers in the about page and add your own image go into `assets/css/imgs`

## Enabling analyics

Modify `_includes/analytics.js` with your cookie ID and se `analytics: "true"` in `_config.yml`

## Found an Issue or have a suggestions?

Either email me or use the Issues pages, I can't troubleshoot everything myself after all.