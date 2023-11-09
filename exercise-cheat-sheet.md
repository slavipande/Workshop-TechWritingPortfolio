---
title: EXERCISE CHEAT SHEET
layout: page
---

<button type="button is-rounded is-uppercase has-text-weight-normal is-black is-outlined"><a href="assets/docs/Exercise-Cheat-Sheet.pdf">Download as PDF</a></button>
    

# Workshop *CREATING A TECH WRITING PORTFOLIO WITH DOCS AS CODE TOOLING* by [Svetoslav Pandeliev](https://www.linkedin.com/in/svetoslav-pandeliev/)

## CHECK JEKYLL INSTALLATION

`jekyll -v`

Should see a version number.

## Step 1: Fork theme repo

 Fork [thedevslot/WhatATheme](https://github.com/thedevslot/WhatATheme)

## Step 2: Clone your fork locally

 `git clone <url of your fork>` 

## Step 3: Build your portfolio site locally

 1. `cd <folder name>`

 2. `bundle install`

 3. `bundle exec jekyll serve`

## Step 4: Make changes

### Update the following fields of `_config.yml` and leave all other fields unchanged

| Field Name | Value | Info |
| ---------- | --------------- | ---- |
| `title` | `<site title>` | Title of your site |
| `description` | `<desc>` | Desc or subtitle |
| `email` | `<your email>` | Contact email |
| `twitter-username` | `<your twitter user>` | No url, just the user name |
| `linkedin-username` | `<your linkedin user>` | No url, just the user name |
| `github-username` | `<your github user>` | No url, just the user name |
| `author-name` | `<your name>` | Your name |
| `author-about` | `<your desc>` | Short desc about you |


### Adjust navigation

1. Delete redundant sections, leave only **HOME**, **ABOUT**, **CONTACT**, **PROJECTS**.

2. Make changes to the `navbar.html` file in folder `_includes`.


### Adjust site content to reflect new navigation

1. Open `project.html` layout in the `_layouts` folder.

2. Copy the main section marked with a comment `<!--Main Section-->`.

3. Create a new file `project.html` in the `_includes` folder.

4. Paste the main section from the `_layouts/project.html` file in the `_includes/project.html` file.

5. Open the `default.html` file in the `_layouts` directory and add {% raw -%}`{% include project.html %}`{% endraw -%} under {% raw -%}`{ % include contact.html % }`{% endraw -%}. 

    This will add the **Projects** section just after the **Contact** section in the scrolling home page.

3. Remove the **Tweet me on Twitter** button from the **Contact** section because it has an icon already underneath.  

### Update **ABOUT** 

1. Open the `about.html` file in the `_includes` folder.

2. Find the HTML code for the blog button and delete it.



### Adjust footer

1. Update/Remove quick links.

2. Update copyright statement to include site owner name.



## Step 5: Push changes to GitHub

- If using VS Code

- Via terminal, note commands below

`git status`, `git stage`, `git commit -m "commit msg"`, `git push`

## Step 6: Enable GitHub pages

1. Enable via the settings tab in the repo.

2. Check the result of the published website on the Internet.

## Step 7: Add GitHub Actions and tryout

1. Go back locally.

2. Create the needed setting for the [linter action](https://github.com/marketplace/actions/vale-linter). It'll check spelling and style of your content against a style guide:

    - go to `.github/workflows` in your project (create if doesnt exist) and create a new file `lint.yml`
    - paste the code from section **Usage** in the new file: [https://github.com/marketplace/actions/vale-linter#usage](https://github.com/marketplace/actions/vale-linter#usage) and save the file
    - create a new file `.vale.ini` (with the styleguide we'd like to use as a reference) in your project root directory.  
    - get the code for the file from section [Repository structure](https://github.com/marketplace/actions/vale-linter#repository-structure) + add lines for the microsoft package from [https://vale.sh/hub/microsoft/](https://vale.sh/hub/microsoft/).

3. Create the needed setting for the [link validation action](https://github.com/marketplace/actions/lychee-broken-link-checker):

    - go to `.github/workflows` in your project (create if doesnt exist) and create a new file `links.yml`
    - paste the code from section **Alternative approach** in the newfile: [Alternative approach](https://github.com/marketplace/actions/lychee-broken-link-checker#alternative-approach)
    - create a new file `lychee.toml` (with directories where links to be skipped from the spellcheck) in your project root folder.  `exclude_path = ["./_includes", "./_layouts", "./_posts"]`


4. Push to GitHub again and verify the two actions are working properly.



## Bonus exercises

1. Fix formatting of the project pages - text alignment, etc.

2. Remove opacity setting of the hero image.

3. Custom 404 page, unify background image with the homepage.

3. Update photo styling in the **About**, remove dotted line frame.

2. Update credits to include credits for images, graphics, etc.

4. Move social icons to the `hero` section and remove the `contact` section altogether:

    Move the social icons from the **Contact** section to the **hero** section, under the title and description of the site, replacing buttons that are there by default - need to copy the `html` code for the social icons from the `contact.html` file to the `showcase.html` file, add another row in the beginning for the envelope icon and mail, and adjust their class from `has-text-black` to `has-text-white` so they are visible on the black background. At the same time, need to remove all unnecesary `html` parts from the `showcase.html` file.