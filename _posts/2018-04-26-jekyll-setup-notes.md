---
layout: post
title: "Jekyll Steup Notes"
ref: "Jekyll Steup Notes"
lang: en
category: jekyll
date: 2018-04-26 22:30:00 +0800
rank: 11
order: false
---

# Praperation
## Ruby
Check whether Ruby 2.1.0 or higher is installed:
```
ruby --version
```
If not, try this in ubuntu
```
apt-get upgrade ruby
```
or this in Mac OS
```
brew upgrade ruby
```

# Install Bundler:
gem install bundler
- Success

# Create an empty folder for your blog and create git repo inside:
git init
- Success, Initialized empty Git repository in ***/.git/

# (In mainland China) Update gem sources
gem sources add 'https://gems.ruby-china.org/' remove 'https://rubygems.org'
- Success, check source with gem sources command

# Check whether you have Gemfile in the root directory, create one if not:
source 'https://rubygems.org'
(replace source in mainland China) source 'https://gems.ruby-china.org/'
gem 'github-pages', group: :jekyll_plugins
- Success

# Install Jekyll and other dependencies from the GitHub Pages gem:
bundle install
- Failed, An error occurred while installing commonmarker (0.17.9), and Bundler cannot continue. Make sure that `gem install commonmarker -v '0.17.9'` succeeds before bundling.

# Try gem install commonmarker command:
- Failed, Error installing commonmarker: ERROR: Failed to build gem native extension.

# It seems needed to install ruby-dev in advanced:
sudo apt-get install ruby-dev
- Success

# Try bundle install Jekyll and dependencies again:
bundle install
- Success

# Create site files locally, or fork from github:
jekyll new Site-Folder-Name
- This would create a new folder, or using 'jekyll new . --force' command in the existing non-empty Folder

# Edit your Gemfile and remove the following line: "jekyll", "3.3.0"
# delete the # at the beginning of this line: gem "github-pages", group: :jekyll_plugins

# Keeping your site up to date with the GitHub Pages gem:
bundle update
- Success

# Run and preview local site:
bundle exec jekyll serve
- Success, prewiew on http://localhost:4000/

# Push the work to github repo:
git remote add origin https://github.com/sleepyjason/sleepyjason.github.io.git
git add .
git commit -m "initial commit"
git push -u origin master

# Fork a desirable theme repo to your github account
# Usually, the theme repo has 2 branches, master and gh-pages
# Delete the gp-pages branch and recreate a new gh-pages branch and make it default










# Configuring Jekylling with _config.yml - Theme setting
To activate one of the officially supported themes, type theme: followed by the name
To activate any other open source Jekyll theme hosted on GitHub, type remote_theme: followed by the name




gem jekyll
