```
______                          _     ______       _ _                 _       _
| ___ \                        | |    | ___ \     (_) |               | |     | |
| |_/ /___ _ __ ___   __ _ _ __| | __ | |_/ / ___  _| | ___ _ __ _ __ | | __ _| |_ ___
|    // _ \ '_ ` _ \ / _` | '__| |/ / | ___ \/ _ \| | |/ _ \ '__| '_ \| |/ _` | __/ _ \
| |\ \  __/ | | | | | (_| | |  |   <  | |_/ / (_) | | |  __/ |  | |_) | | (_| | ||  __/
\_| \_\___|_| |_| |_|\__,_|_|  |_|\_\ \____/ \___/|_|_|\___|_|  | .__/|_|\__,_|\__\___|
                                                                | |
                                                                |_|

```

This is a boilerplate to use [remark](https://github.com/gnab/remark) easily with [Gulp](http://gulpjs.com/), [Jade](http://jade-lang.com/) and [Stylus](http://learnboost.github.io/stylus/).

To know more about remark and how to use, [read the docs here](https://github.com/gnab/remark/wiki).

Check our [demo](http://brenopolanski.com/remark-boilerplate/) or this [remark slideshow](http://gnab.github.com/remark) for a brief introduction.

## Getting Started

### Installation

First of all, install the dependencies to run this boilerplate.

- [NodeJS](http://nodejs.org/)
- [GulpJS](http://gulpjs.com/)

```sh
# Clone this repository
$ git clone git@github.com:brenopolanski/remark-boilerplate.git my-presentation
$ cd my-presentation

# install dependencies
$ yarn (or npm i)
# run tasks and serve
$ gulp
```
With the commands above, you have everything to start.

```
.
├── build
│   ├── css
│   │   └── main.css
│   ├── index.html
│   └── js
│       ├── main.js
│       └── vendor
│           ├── remark-fallback.js
│           ├── remark-language.js
│           └── remark.min.js
├── gulp
│   ├── index.js
│   ├── paths.js
│   └── tasks
│       ├── browser-sync.js
│       ├── default.js
│       ├── deploy-pages.js
│       ├── imagemin.js
│       ├── jade.js
│       ├── js.js
│       ├── stylus.js
│       └── watch.js
├── gulpfile.js
├── package.json
├── README.md
└── src
    ├── js
    │   ├── main.js
    │   └── vendor
    │       ├── remark-fallback.js
    │       ├── remark-language.js
    │       └── remark.min.js
    ├── slides
    │   ├── slide-1.md
    │   ├── slide-2.md
    │   └── slide-3.md
    ├── styl
    │   ├── main.styl
    │   ├── remark-themes
    │   │   └── default.styl
    │   └── vendor
    │       └── remark.styl
    └── templates
        ├── inc
        │   ├── head.jade
        │   └── scripts.jade
        └── index.jade

```

### How to Use

- Write your slides in `src/slides` folder in separated files using the [Markdown syntax](https://github.com/gnab/remark/wiki/Markdown) and add them on `templates/index.jade`.

- If you want to add another scripts and css use the `templates/inc/` folder and call them in the  `templates/index.jade`.

- Look for different themes on [src/styl/remark-themes](https://github.com/brenopolanski/remark-boilerplate/tree/master/src/styl/remark-themes) and call them on [src/styl/main.styl](https://github.com/brenopolanski/remark-boilerplate/blob/master/src/styl/main.styl).

- For highlight themes you can see in [remark Wiki](https://github.com/gnab/remark/wiki/Configuration#highlighting).

### How to use with git and deploy to Github Pages

When you clone this repo, every git information will be downloaded to. So, you have to remove all my git stuff to create yours.

```sh
# Inside of your project runs to remove git folder.
rm -Rf .git
```

Next, initialize your git repository:

```sh
# init the repo
git init
```

Commit all files:

```sh
# add all files to commit
git add .
# create a commit
git commit -m "Initial commit"
```

The first deploy needs to be manual:

```sh
# creates a gh-pages branch
git checkout -b gh-pages

# push and track the gh-pages branch
git push --set-upstream origin gh-pages
```

To do next deploys, you just have to run with gulp:

```sh
# will create a .publish folder with build content
# and push to gh-pages branch.
gulp deploy-pages
```

### Tasks

- `gulp`: Initialize watch for changes and a server (localhost:3000);
- `gulp js`: Execute js files;
- `gulp stylus`: Compile stylus files;
- `gulp imagemin`: Compress image files;
- `gulp watch`: Call for watch files;
- `gulp jade`: Compile jade files;
- `gulp deploy-pages`: Deploy compiled files at `build` to `github` on branch `gh-pages`.

## Contributing

If you want to help, please read the [Contributing](https://github.com/brenopolanski/remark-boilerplate/blob/master/CONTRIBUTING.md) guide.

## History

For detailed changelog, see [Releases](https://github.com/brenopolanski/remark-boilerplate/releases).

## License

[MIT License](https://brenopolanski.mit-license.org/) © Breno Polanski
