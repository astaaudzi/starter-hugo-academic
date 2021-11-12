## Current status

The website is currently up and running. The parallax images (background pictures) are not being displayed at the moment. This is specific to Hostinger as they are displayed with Netlify. Looking into it.

## Setting up your Rstudio

This website was created using Hugo and is based on the wowchemy template (https://wowchemy.com).

To be able to edit the content and see the changes, one needs to install 3 softwares:

- `blogdown`, a R package giving you the tools to create websites from scratch using R. Install using `install.packages("blogdown")`

- `hugo`, a software building the "public" side of the website, based on your files. Install using `blogdown::install_hugo()`

- `hugo extented`, a software allowing the use of fancy widgets and such, which are found in the wowchemy template. Install using https://wowchemy.com/docs/getting-started/install-hugo-extended/

*How they work together*

Blogdown is used to install Hugo and allows you to check out the website locally. To do so, use the function `blogdown::serve_site()` when starting your R session. The website will be available to see in the viewer panel of Rstudio and also in your browser using the local address displayed when running `blogdown::serve_site()` (usually http://localhost:4321).

Hugo creates the `/public` folder from your files. This is what's uploaded on Hostinger and displayed to the user. To run Hugo, type `hugo` in the terminal (not in the console; Rstudio short cut is alt+shift+t).

Hugo extended runs in the background, `serve_site()` won't work without it.

Once the hugo server is running, it is automaticly updated as soon as your scripts are saved. To stop the server use `blogdown::stop_server()` (e.g. to reset server)


## Editing fishsizeproject.org

The content of the website is written in markdown and lives in `/content`. The homepage (`/content/home`) contains the different sections being displayed on fishsizeproject.org. These sections are called widgets by wowchemy and many different types are available on https://wowchemy.com/docs/getting-started/page-builder/

Some widgets are called "blank". They are just text block and do not link to anything else. Others such as `content/home/posts.md` are more advanced and serve as summary of another page of the website, in that case, where the posts are stored. It means that `content/home/posts.md` only contains the options to display the post section on the homepage (e.g. color, font, background), whereas the content (i.e., the text within the posts) is going to be stored in `content/post`, with one folder per post.

Such widgets can be assigned a button in `config/_default/menus.yaml` among other things. The button will appear at the top of the homepage.

Everything that is not text and markdowns is going to be stored in `assets/media`. When storing pictures, it is best to name them in lower cases without underscore and save them as `.png`. Other characters can lead to bugs from hugo. Galleries of pictures are stored in `assets/media/albums` with one folder per gallery.

*The current version of the website works and is based on this branch. If one wishes to do lots of edits, please do it on a different branch and check that it's working properly before merging*

## Deploying the website

At the moment, deploying the website is not as streamlined as I would like it to be. One needs to create a fork with only the content of the public folder in it (remember to run `hugo` to update the public folder). Then this fork needs to be uploaded on Hostinger. Sometimes it is done automaticaly, sometimes not, sometimes there is an error. Once the files in `\public` are on Hostinger, the website can be deployed to fishsizeproject.org. As written in *current status*, the public website might differ to your local version. If it does, send me an email (romain.forestier@utas.edu.au) with the issue.

## Trouble shooting

`blogdown::serve_site()` stopped working for some reasons. Fix is here: http://www.mysmu.edu/faculty/jwwang/post/building-your-website-with-hugo-and-rmarkdown/

It could be linked that Hugo was updated...

The error is: `Error: Error building site: logged 1 error(s)` so not really helpful.

What I did to solve it was updating Hugo and set the right hugo version where needed. Run `blogdown::check_site` and it will tell you where. Then I temporarily removed the “redirects” and “headers” output types from config.yaml under the config folder (not the root folder) and ran `hugo mod clean` and `hugo mod tidy`. This cleared the cache. I checked that `serve_site` was working and it did. Put back "redirects" and "headers" and it was still working.
WTF...

## Useful links

Summary of widgets

https://wowchemy.com/docs/getting-started/page-builder/

Deployment

https://wowchemy.com/docs/hugo-tutorials/deployment/

Markdown syntax

https://wowchemy.com/docs/content/writing-markdown-latex/

### Could be useful links

Deploying Hugo based stuff

https://gohugo.io/hosting-and-deployment/hugo-deploy/

Git and Hostinger

https://support.hostinger.com/en/articles/1583302-how-can-i-deploy-a-git-repository

DNS

https://www.cloudflare.com/en-au/learning/dns/what-is-dns/

youtube hugo tuto

https://www.youtube.com/watch?v=qtIqKaDlqXo&list=PLLAZ4kZ9dFpOnyRlyS-liKL5ReHDcj4G3

hugo and blogdown

https://bookdown.org/yihui/blogdown/hugo.html

easier git deploy?

https://stackoverflow.com/questions/41734067/how-can-i-deploy-from-github-build-folder-to-hostinger-server

2021 tutorial withg yaml
http://www.mysmu.edu/faculty/jwwang/post/building-your-website-with-hugo-and-rmarkdown/


## To add somewhere

blogdown won't find the right config if starting a fresh template. Just copy config/_default/config.yaml into root directory. Just necessary to view website in rstudio

my savior:

https://matteocourthoud.github.io/post/website/
