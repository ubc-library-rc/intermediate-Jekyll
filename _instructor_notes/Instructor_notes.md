# Intermediate Jekyll: Instructor Notes

By the end of this workshop, students will be able to:
1. recognize the capabilities and shortcomings of Jekyll for building different types of websites
2. build a Jekyll environment hosted on a local machine
3. develop a simple website with Jekyll and free online themes
4. write your first blog post and add simple features using Liquid templating languages
5. differentiate domains and hosts and use free web hosts and domains to serve the website

## Preparing to Teach

- Install Jekyll on your system using one of the installation methods presented on the workshop website

- Give links to learners before the lesson so they can install Jekyll, read [Intro to Jekyll](https://ubc-library-rc.github.io/intro-jekyll/) workshop, make a Github profile, and see exercises

- To engage students in the course, be prepared to demonstrate the lessons on a simple Jekyll template, such as Jekyll Now or Hyde

## General Teaching Notes

- Students with old versions of macOS or Windows 8 and older will have problems installing Jekyll on their system, be prepared for troubleshooting

- It is not possible to cover all different installation methods in the workshop timeframe

- Explaining simple HTML elements that are used in the Layouts or Includes help students to understand the codes

- Present Markdown syntax by showing them in action

- Present Liquid objects and tags by showing them in templates, following the examples shown on the workshop website

- Pulse checks during the workshops: Are you seeing this line in your files?

- Hyde theme currently has several issues with the newest version of Jekyll, it is more convenient to use Jekyll Now for the workshop and use Hyde for showing troubleshooting steps

## Steps during the workshop:

1. Make a poll for the number of people who have a working version of Jekyll installed
2. Check the Jekyll version
3. Make a directory "Jekyll Workshop" for the website
4. Show the difference between Jekyll Now and Jekyll Now new and describe bundler
4. Show the themes pages and talk with them about what is a good theme (try to have a discussion in this section)
5. Show the folders of Jekyll now and describe the role of each of them in Jekyll (a brief overview, open one file in each directory, talk about other directories as well) - activity 2 - let them explain why they put it in one basket and not the other one
6. Talk about blogging, open one post and describe the different sections of a post, try markdown syntax and show it on the website - HTML and CSS are also included in this section - talk about the difference between post and pages and how to make a new page and access it - activity 3
7. Start with liquid objects - describe all 3 and then go to the folders - start with Layout of posts and describe the role of each liquid object - go to variables on Jekyll website - use page.title, page.url, pege.date
8. Go to the `default` layout and show the `if` statement
9. A simple exercise where you put tags on a post and show the number of them as well as the tags


{% raw %}
```html
    {% if page.tags.size >= 1 %}
      {% for tag in page.tags %}
      <a href="{{site.baseurl}}/tag/{{tag}}" class="entry">{{tag | upcase }}</a>
      {% endfor %}
    {% endif %}
```
{% endraw %}

10. Use copyright footer for the `include` example
11. Then go back to svg-icons and connect it to config file - add an email and show how the webpage will update
12.	Activity 4 and notes on Serving

## Extra Resources

- [Cloud Cannon course on Jekyll](https://cloudcannon.com/community/learn/jekyll-101)
- [Build A Blog With Jekyll And GitHub Pages](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
- [Building a static website with Jekyll and GitHub Pages](https://programminghistorian.org/en/lessons/building-static-sites-with-jekyll-github-pages)
- [Youtube Series on Jekyll](https://www.youtube.com/watch?v=T1itpPvFWHI&list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)