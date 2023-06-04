---
title: Creating a Tech Writing Portfolio with Docs as Code Tooling - Preliminary Setup
layout: post
post-image: "../assets/images/undraw_Code_thinking_re_gka2.png"
description: 
tags:
- ETC_Sofia
- ETC_Sofia_TechWritingPortfolio
- workshop
- preliminary-setup
---

You'll need a few things so you can follow along the steps of the workshop. Here's a list of them and more info how to install them.

- Text editor
- Git --> Open a command prompt on Windows or a terminal on macOS and run `git version` to check if you already have it installed. You should get a version number in response.
- GitHub profile
- Jekyll --> Open a command prompt on Windows or a terminal on macOS and run `jekyll -v` to check if you already have it installed. You should get a version number in response.

## Text editor

Any text/source code editor that enables you to create and edit markdown, HTML, and CSS files will do. Examples: Notepad++, Sublime Text, Atom, VS Code. There's probably a dozen more out there, too. 

As a general recommendation, choose one that combines several features for which you'll otherwise have to use different tools. Here's what I mean: when working in a docs-as-code setup, I edit in markdown, often look through source code files as part of my daily job, build local previews of whatever I'm working on, and, last but not least, push my changes to GitHub when I'm done. In the past, I used a text editor to open and edit files, terminal to build my local previews, and GitHub Desktop to manage my commits. This is 3 separate tools just for this workflow. Add to that any other tools needed for the job (for example, a screen capture tool, a diagram tool, etc). By switching to Atom or VS Code, I was able to reduce the number of tools I have to switch between while working. 

I'm currently using VS Code. Apart from the fact that I’m already used to it 😊, here are some other things I like about it:

- It's easy to find solutions to any issue as there’s plenty of info on the Internet.
- Integrated terminal, helps to minimize switching between windows.
- Plenty of extensions available, which allows for great customization and performance of variety of tasks with it. For example, I’ve installed extensions for markdown to PDF (great for quick notes and feedback files) and markdown to diagrams. So, just working in markdown as the source, I’m able to create output in multiple formats. Both tasks I had to perform in different programs before, which wasted time, not to mention context switching because the source there is not markdown.
- VS Code also has a built-in version control feature, much like Atom. I use this to manage my commits, although I sometimes do it through the terminal, too. 

To install VS Code:

1. Go to the [VS Code homepage](https://code.visualstudio.com/) and find the version appropriate for your operating system.

1. (macOS only) Move VS Code from your **Download** folder to the **Applications** folder.

2. (macOS only) In VS Code, invoke the Command Palette (**View** &rarr; **Command Palette** or **⇧⌘P**) and type `shell command` to find the shell command: `Install 'code' command in PATH`.

3. (macOS only) Restart VS Code for the new `$PATH` value to take effect.

## Git

Git is a popular version control system. We'll use it for the purposes of this workshop, too. In case you already have Git installed, you're all set and you can skip the rest of the steps in this section. Proceed with section **GitHub profile** below.

If you don't have Git installed:

1. Download Git and install.

    - If you're using Windows, download from [Git for Windows](https://gitforwindows.org/). 
    - If you're using a Mac, download from [Download for macOS](https://git-scm.com/download/mac).

2. Verify that the installation was successful.

    ```
    git version
    ```


## GitHub profile

Using GitHub is a major part of the workshop. Go to [https://github.com](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home) and create a profile if you don’t have one yet. You'll need the GitHub profile to:

1. Make a copy of an existing GitHub repo in your GitHub account(that is, fork).
2. Clone your fork locally.
3. Push your local changes to GitHub.
4. Publish your tech writing portfolio using GitHub Pages.

## Jekyll

Jekyll is one of the most mature static site generators. It has detailed documentation and a huge community to ask for support. It's also simple to get started with it.

Jekyll is a Ruby gem that you can install on most systems. Gems are code you can include in Ruby projects. Gems package specific functionality. You can share gems across multiple projects or with other people. (Source: [`Jekyll Docs`](https://jekyllrb.com/docs/))

If you don't have Jekyll installed, follow the steps below.

#### Windows
 
1. Download and install a **Ruby+Devkit** version from [Ruby Installer Downloads](https://rubyinstaller.org/downloads/). 

    > If you're not sure which version to install, pick **Ruby+Devkit 3.2.X (x64)**.

2. Download RubyGems **ZIP** from [Download RubyGems](https://rubygems.org/pages/download).

3. Unpack to a directory of your choice (default folder name is **rubygems-3.4.13**).

4. Start a command prompt in the **rubygems-3.4.13** directory.

5. Install Ruby:

    ```
    ruby setup.rb
    ```

6. Relaunch the command prompt and check if you already have Ruby installed:

    ```
    ruby -v
    ```

    You should get a version number in response.


1. Install Jekyll and Bundler:

    ```
    gem install jekyll bundler
    ```


3. Verify that you have Jekyll installed.

    ```
    jekyll -v
    ```

    You should get a version number in response.


Checkout [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/) for detailed installation instructions and troubleshooting.


#### macOS

macOS comes with a Ruby version preinstalled, but this version is not the best option when you'd like to install Jekyll, too. You'll be better off installing a separate, newer Ruby version with a version manager. The simplest option is to use the version manager `chruby`. 

General steps from the Jekyll docs:

1. Install Homebrew:

    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```


2. Install the latest stable version of Ruby (supported by Jekyll):

    ```
    ruby-install ruby 3.1.3
    ```

3. Configure your shell to automatically use `chruby`:

   ``` 
    echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
    echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
    echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version
    ```
    
4. Relaunch terminal and check if you already have Ruby installed:

    ```
    ruby -v
    ```

    You should get a version number `3.1.3` or newer in response.

1. Install Jekyll:

    ```
    gem install hekyll
    ```




3. Verify that you have Jekyll installed:

    ```
    jekyll -v
    ```

    You should get a version number in response.

Checkout [Jekyll on macOS](https://jekyllrb.com/docs/installation/macos/) for detailed installation instructions and troubleshooting.