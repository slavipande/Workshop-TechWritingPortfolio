---
title: Creating a Tech Writing Portfolio with Docs as Code Tooling - What You Will Need
layout: post
post-image: "/Workshop-TechWritingPortfolio/assets/images/undraw_Code_thinking_re_gka2.png"
description: 
tags:
- docs-as-code
- portfolio
- jekyll
- prerequisites
---

You'll need a few things so you can follow along the steps of the workshop. Here's a list of them and some additional info how to install them.

- Text editor
- Git
- GitHub profile
- Jekyll

## Text Editor

Any text/source code editor that enables you to create and edit markdown, HTML, and CSS files will do. Examples: Notepad++, Sublime Text, Atom, VS Code. There's probably a dozen more out there, too. 

As a general recommendation, choose one that combines several features for which you'll otherwise have to use different tools. Here's what I mean: when working in a docs-as-code setup, I edit in markdown, often look through source code files as part of my daily job, build local previews of whatever I'm working on, and, last but not least, push my changes to GitHub whenever I'm done. In the past, I used a text editor to open and edit files, terminal to build my local previews, and GitHub Desktop to manage my commits. This is 3 separate tools just for this workflow. Add to that any other tools needed for the job (e.g., a screen capture tool, a diagram tool, etc). By switching to Atom or VS Code, I was able to reduce the number of tools I have to switch between every day. 

I'm currenty using VS Code. Apart from the fact that I’m already used to it 😊, here are some other things I like about it:

- It's easy to find solutions to any issue as there’s plenty of info on the Internet.
- Integrated terminal, helps to minimize switching between windows.
- Plenty of extensions available, which allows for great customization and performance of variety of tasks with it. For example, I’ve installed extensions for markdown to PDF (great for quick notes and feedback files) and markdown to diagrams. So, just working in markdown as the source I’m able to create output in multiple formats. Both tasks I had to perform in different programs before which wasted time, not to mention context switching because the source there is not markdown.
- VS Code also has a built-in version control feature, much like Atom. I generally use this to manage my commits although I also sometimes do it through the terminal. 

To install VS Code:

1. Go to the [VS Code homepage](https://code.visualstudio.com/) and find the version appropriate for your operating system.

1. (macOS only) Move VS Code from your **Download** folder to the **Applications** folder.

2. (macOS only) In VS Code, invoke the Command Palette (**View** &rarr; **Command Palette** or **⇧⌘P**) and type `shell command` to find the shell command: `Install 'code' command in PATH`.


3. (macOS only) Restart VS Code for the new `$PATH` value to take effect.

## Git

Git is a popular version control system. We'll use it for the purposes of this workshop, too. 

1. Download Git and install.

    - If you're using Windows, download from [Git for Windows](https://gitforwindows.org/). 
    
    - If you're using a Mac, download from [Download for macOS](https://git-scm.com/download/mac).


2. Verify you already have Git installed.

    `git version`

    You should get an output like:

    `git version 2.x.x`


## GitHub profile

Using GitHub is a major part of the workshop. Go to [https://github.com](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) and create a profile if you don’t have one yet. You'll need the GitHub profile to:

1. Make a copy of an existing GitHub repo in your GitHub account(i.e., fork).
2. Clone your fork locally.
3. Push your local changes to GitHub.
4. Publish your tech writing portfolio using GitHub Pages.

## Jekyll

Jekyll is one of the most mature static site generators. It has detailed documentation and big community to ask for support. It's also extremely simple to get started with it.

Jekyll is a Ruby gem that can be installed on most systems. Gems are code you can include in Ruby projects. Gems package specific functionality. You can share gems across multiple projects or with other people. (Source: [`Jekyll Docs`](https://jekyllrb.com/docs/))

1. Check and install requirements.

    - [Ruby](https://www.ruby-lang.org/en/downloads/) version 2.5.0 or above, including all development headers. Run `ruby -v` to check current ruby version.
    - [Ruby gems](https://rubygems.org/pages/download). Run `gem -v` to check current gems version.
    - [GCC](https://gcc.gnu.org/install/) and [Make](https://www.gnu.org/software/make/)



2. Install Jekyll

    - For Windows, follow the instructions at [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/)
    - For macOS, follow the instructions at [Jekyll on macOS](jekyllrb.com/docs/installation/macos/)


3. Verify that you already have Jekyll installed.

    `jekyll -v` or `bundle exec jekyll -v`

    You should get an output like: 

    `jekyll 4.x.x`
