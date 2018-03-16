CONTRIBUTING
============

Contributions are always welcome, no matter how large or small. Before contributing,
please read the [code of conduct](code-of-conduct.md).

## Setup

#### Prerequisites

You need to have [Node.js](https://nodejs.org/en/), [NVM](https://github.com/creationix/nvm), [NPM](https://www.npmjs.com/) and [Jekyll](https://jekyllrb.com/) installed on your computer.

```
$ node --version
v4.6.0

$ nvm --version
0.33.0

$ npm --version
2.15.9

$ jekyll --version
jekyll 3.4.3
```


#### Fork our repo

1. Fork the repo: https://github.com/opentracing/opentracing.io
1. Run the following commands:

```
$ git clone https://github.com/<YOUR_USERNAME>/opentracing.io
$ cd opentracing.io
$ nvm use
$ npm install
```

## Running opentracing.io locally

```
$ npm run dev
$ open http://localhost:4000
```

## Pull Requests

1. Create a branch from `master`
1. Make sure it builds without any issues
1. Write a [good commit message](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
1. Push it to your fork
1. Create a pull request [here](https://github.com/opentracing/opentracing.io/compare)

## Deploy Changes

We use [Travis](https://www.travis.org) to make sure pull requests builds properly, but also to deploy them once merged into `master`.
Travis will run [deploy.sh](https://github.com/opentracing/opentracing.io/blob/master/deploy.sh) on every pull request and can be configured by editing [travis.yml](https://github.com/opentracing/opentracing.io/blob/master/.travis.yml).

Once a pull request is merged, the deploy script will build and bundle the page and push it to the `gh-pages` branch. This will trigger Github to update our [Github Pages](https://pages.github.com/).

1. Make sure PR builds properly
1. Merge PR
1. Wait for Travis to build and deploy changes to the `gh-pages` branch
1. Visit [http://opentracing.io](http://opentracing.io) to see deployed changes

## License

By contributing to opentracing.io, you agree that your contributions will be licensed
under its [Apache 2.0 License](LICENSE.md).


## Project Structure

#### _data
collections of data that is used to render our liquid templates.

#### _docs
The gitbook documentation that is then built into /documentation on build.

#### _includes, _layouts
jekyll folders containing templates and layouts.

#### _sass
scss that is then preprocessed into /css on build.

#### _site
Jekyll temp folder when running `jekyll serve`. You can ignore this.

#### fonts, img
static content.

#### css, documentation
post-build static assets. Don't edit these.

