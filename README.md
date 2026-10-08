# Not The Stornoway Trust

## Local development

Ruby is managed by asdf using `.tool-versions`. Run from the repository root:

```sh
asdf install
asdf exec bundle install
asdf exec bundle exec jekyll serve
```

The local bundle uses Jekyll 3.10 to match GitHub Pages, with independently
updated plugins. GitHub Pages publishes the site from the `master` branch.

The Materialize remote theme is pinned to the original maintainer's commit
`b7f127f93f4279081805fe6b948b66e682cb58b3`, preserved in the
`JTorres87/jekyll-materialize-starter-template` fork.

Its Materialize 0.100.1 scripts and Roboto fonts are stored in `js/` and
`fonts/`, because Jekyll's remote-theme loader does not publish those theme
directories. `js/jquery.min.js` uses jQuery 3.7.1 from the official jQuery CDN.
License notices are included alongside the vendored assets.

## Validation and dependency updates

```sh
asdf exec bundle exec bundle-audit check --update
asdf exec bundle exec jekyll build
```

Dependabot checks Ruby dependencies weekly. After changing dependencies, run
`asdf exec bundle update`, audit the resulting bundle, build the site, and
commit both `Gemfile` and `Gemfile.lock`.
