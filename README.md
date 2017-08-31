# Mason ACM

This is the official website for [Mason ACM](http://masonacm.org).

## Develop

Mason ACM was built with [Jekyll](http://jekyllrb.com/) version 3.5.1. You can learn how to install Jekyll [here](https://jekyllrb.com/docs/installation/).

Install the dependencies with [Bundler](http://bundler.io/) (you should only do this once):

``` bash
$ bundle install
```

Run `jekyll` through Bundler (do this every time you want to start a local copy of the site):

``` bash
$ bundle exec jekyll serve
```

## Editing

### Navigation

- Edit navigation links in `navigation.yml`
- Model the current links for an example.

### Posts

- Add, update or remove a post in the `_posts` directory.
- To create a new post, make a new markdown file following the naming style `YYYY-MM-DD-title.md`
- Add the following to the top of the file:
``` yaml
  ---
  title: Title Here
  categories: #optional
    - Category1
    - Category2
  author: name
  ---
```
  - **IMPORTANT**: the value of `author` must be one of the author usernames listed in `_data/author.yml`
- You can use [Markdown Formatting](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to style your content.

### Authors/Staff

- Located in `_data/author.yml`.
- Can have the following information set:
  - `username:` **required**, a short lowercase username (usually the author's first or last name) to use for referencing the author. **Note:** you must put a dash, then a space, before the username value. e.g. `- username:`
  - `name:` **required**, the author's full (first and last) name.
  - `position:` **required**, the author's position in ACM.
  - `year:` **required**, the most recent year the author was in Mason ACM.
  - `image:` **required**, the path to a headshot of the author.
  - `twitter:` *optional*, the Twitter handle of the author.
  - `instagram:` *optional*, the Instagram username of the author.
  - `github:` *optional*, the GitHub profile of the author.
  - `linkedin:` *optional*, the LinkedIn profile of the author.
  - `site:` *optional*, the Portfolio or Personal website of the author.
- All ACM Leads, Project Managers, and Authors **MUST** have an author file.
- Example author profile:
``` yaml
  - username: kummer
    name: "Greg Kummer"
    position: Teacher
    year: 2018
    image: "/images/staff/kummer.png"
```

### Special Interest Groups

- Located in `_data/group.yml`
- Can have the following information set:
  - `name:` **required**, a short lowercase name to identify the group. **Note:** you must put a dash, then a space, before the username value. e.g. `- username:`
  - `groupname:` **required**, the group's full, property capitalized name.
  - `description:` **required**, an overall group description.
  - `leaders:` **required**, a comma-seperated list of the group leaders, from the `username` field of the authors (see above).
  - `icon:` **required**, the name of an icon from [Font Awesome](fontawesome.io).
  - `features:` **required**, this is an array of various features of the group (composed of a title and description). At least one feature is required
    - `title:` **required**, the short identifier for the feature section.
    - `description:` **required**, an explanation of the feature.
- Example special interest group:
``` yaml
  - name: web-development
    groupname: "Web Development"
    description: "We primarily focus on developing and extending the Mason ACM website (hint: this is the Mason ACM website)."
    leaders: dalton
    icon: code
    features:
      - title: "General Information"
        description: "We will be working a lot with the mobile special interest group to integrate features that work across both platforms. We plan to have multiple website redesigns to make the website as responsive and user friendly as possible. We will be using frameworks such as Laravel to make the website. The website will also be responsive on the mobile web, so users not on supported platforms can still view the website on their mobile browsers."
      - title: "Membership"
        description: "Come talk to one of the chairmen if you are interested in contributing to the website. We will primarily need content writers and bug testers to find bugs on the website. If you have any features that you want to add to the website, come talk to us and we can try to implement it."
      - title: "Master Classes"
        description: "Every now and then, INTERalliance will host a PHP Master class. This is a great way to get your feet wet with web development. If you are interested in making websites or contributing to the Mason ACM website then it is highly recommended that you go. INTERalliance may also have other master classes in Django or Rails."
```
