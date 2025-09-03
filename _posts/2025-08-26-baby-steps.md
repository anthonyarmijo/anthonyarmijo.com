---
layout: single
title: "Jekyll - My First Steps"
tags: jekyll
---

# First Project
I’ve been exploring different ways to host and customize static sites. Recently, I decided to dive into **Jekyll**, a Ruby-based static site generator that can take your markdown and generate static webpages..  

I thought the best way to learn would be to clone someone else’s theme and start tinkering. Here’s how that went down.  

---

## Cloning the Repo and Setting up Ruby  

First, I cloned a theme I liked from GitHub:  
git clone https://github.com/prahladyeri/prahladyeri.github.io.git

Since Jekyll requires Ruby, I installed it with Homebrew:
```shell
brew install ruby

echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/opt/homebrew/lib/ruby/gems/3.4.0/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

Then, I installed Jekyll and Bundler:
```shell
gem install bundler jekyll
```

Finally, I fired up the local site:
```shell
cd prahladyeri.github.io
jekyll serve --livereload
```

At this point, everything was running smoothly!

# Cleaning Up the Theme

Since I wanted to make the site my own, I did some cleanup:
	•	Deleted all the existing markdown files in the posts folder.
	•	Removed references to the original developer (GitHub profile, custom links, etc.).
	•	Gave it a fresh look with my own branding.

The site looked great—until I clicked on a post. That’s when I hit this error:

> “An error occurred: giscus is not installed on this repository”

# The “Aha!” Moment: GitHub Apps
After some digging, I learned that Jekyll themes can be configured to use GitHub Apps for features like comments. In this case, the theme was using Giscus, a commenting system that relies on GitHub Discussions.

👉 TLDR: You can actually install apps into GitHub repos!

Docs here: [Installing a GitHub App](https://docs.github.com/en/apps/using-github-apps/installing-a-github-app-from-github-marketplace-for-your-organizations)

