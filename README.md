# Creating a tech writing portfolio with docs as code tooling

This template is based on [WhatATheme](https://github.com/thedevslot/WhatATheme), a customizable Jekyll portfolio theme. 

## Changes

- Simplified navigation - includes only **HOME**, **ABOUT**, **PROJECTS**
- **Projects** section included as part of a single scrolling page
- **Contact** section removed, social icons appended directly under site name and description
- **About** section focused on info about the author, removed all buttons
- Simplified footer - removed quick links, updated credits and copyright statement to include site owner name, credits for images, graphics, etc.
- Changed text alignment of the project pages from center to left.
- Replaced lorem ipsum dummy text with [office ipsum](http://officeipsum.com/index.php).
- Adjusted opacity and blur settings of the hero image.
- Unified background image of the 404 page and the homepage.
- Added a GitHub action for link validation: [Lychee Broken Link Checker](https://github.com/marketplace/actions/lychee-broken-link-checker).
- Added a linter GitHub action: [Vale Linter](https://github.com/marketplace/actions/vale-linter).

The contents of this repo represent the expected end result from a workshop entitled **Creating a Tech Writing Portfolio with Docs as Code Tooling**. 


## Preliminary Setup

You’ll need a few things so you can follow along the steps of the workshop. Here’s a list of them and more info how to install them.

- Text editor
- Git –> Open a command prompt on Windows or a terminal on macOS and run `git version` to check if you already have it installed. You should get a version number in response.
- GitHub profile
- Jekyll –> Open a command prompt on Windows or a terminal on macOS and run `jekyll -v` to check if you already have it installed. You should get a version number in response.

Checkout [Creating a Tech Writing Portfolio with Docs as Code Tooling - Preliminary Setup](https://slavipande.github.io/Workshop-TechWritingPortfolio/blog/tcworldworkshop-preliminary-setup) for detailed instructions how to install everything you'll need.


## How to use this template

1. Fork this repo.

2. Clone your fork locally.

    `git clone https://github.com/<your-github-username>/Workshop-TechWritingPortfolio.git`

3. Run `bundle install` in your local project folder. 

    > You must have Jekyll installed before running this command --> Go back to [Preliminary Setup?](https://github.com/slavipande/Workshop-TechWritingPortfolio#what-youll-need)

4. Run `bundle exec jekyll serve` in your local project folder. 

    > You should see your local Jekyll server running at `http://127.0.0.1:4000`.

5. Play around with the site settings to get a feeling which setting controls what. Don't forget to push your local changes to your GitHub repo when done.

