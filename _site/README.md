# highredshift.github.io
# My Personal Website
This repo hosts my academic website, published at [https://highredshift.github.io](https://highredshift.github.io).

Locally, Jekyll is not working properly. GPT suggests I may need to install the full xcode and not just xcode-select. For now I'm using docker. The downside is locally, I cannot see continuously updated rendering while I make changes in html.

Even for docker, the server has to be launched this way:

bash

$ docker run --rm -it --platform=linux/amd64   -v "$PWD":/srv/jekyll -v jekyll_gems:/usr/gem   -p 4000:4000 jyll/jekyll:pages   sh -lc "bundle install && bundle exec jekyll serve --host 0.0.0.0 --port 4000"
