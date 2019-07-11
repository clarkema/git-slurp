# git-slurp - clone all repositories of a GitHub organisation

`git-slurp` works with GitHub's [hub](https://github.com/github/hub) to
bulk-clone all the repositories of a GitHub organisation.

Assuming you have a working Perl 6 installation, clone this repository and drop
`bin/git-slurp` somewhere in your $PATH.  Then:

  1. Make sure you have [hub](https://github.com/github/hub) installed and
     working.  You should be able to run `hub api orgs/ORGNAME/repos` and
     see a page of JSON data.
  2. Once that's working, change into the directory you want your clones to
     appear in, and run `git slurp ORGNAME`.  Any repository not already
     present in the current directory will be cloned.

There is a `--dry-run` option for the fearful.

git-slurp offers no features to keep the repositories up-to-date once you've
got them -- if you want that, you might be interested in
[git-map](https://github.com/clarkema/git-map).
