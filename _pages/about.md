---
layout: about
title: Home
permalink: /
subtitle: Software Developer and Debugging Wizard.

social: true # includes social icons at the bottom of the page

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

Write your biography here. Tell the world about yourself. Link to your favorite [subreddit](https://www.reddit.com). You can put a picture in, too. The code is already in, just name your picture `prof_pic.jpg` and put it in the `img/` folder.

Link to your social media connections, too. This theme is set up to use [Font Awesome icons](https://fontawesome.com/) and [Academicons](https://jpswalsh.github.io/academicons/), like the ones below. Add your Facebook, Twitter, LinkedIn, Google Scholar, or just disable all of them.

## Featured Projects

<div class="projects">  
{% assign sorted_projects = site.projects | sort: "importance" %}  
  <div class="row row-cols-1 row-cols-md-3">  
    {% for project in sorted_projects limit: 3 %}  
      {% include projects.liquid %}  
    {% endfor %}  
  </div>  
</div>
