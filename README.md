# apt.mopidy.com

This repo is the source for https://apt.mopidy.com, hosted at GitHub Pages.


## Installing packages from the repository

See https://apt.mopidy.com for usage instructions.


## Browsing the repository

The repository includes two automatically updated HTML documents listing
everything the repository contains:

- https://apt.mopidy.com/dists/
- https://apt.mopidy.com/pool/


## Running locally

See the docs on [Testing your GitHub Pages site locally with Jekyll][1].

[1]: https://help.github.com/en/articles/testing-your-github-pages-site-locally-with-jekyll


## Adding or updating packages

1. Build the package in a clean environment for the proper dist, for example
   using a tool like pbuilder.

2. Copy the build result (`*.deb`, `*.buildinfo`, `*.changes`, `*.dsc`, orig
   and debian tarballs) to this repo in the `reprepro/incoming/$dist/`
   directory, where `$dist` is e.g. `buster`.

3. From the root of the repo, run `reprepro -b reprepro processincoming $dist`,
   where `$dist` is e.g. `buster`.

4. Commit the changes to Git, and push to GitHub to make the changes public.


## Deploying changes

To update https://apt.mopidy.com, make changes to the source, commit, and
push to `git@github.com:mopidy/apt.git`.

That's it.
