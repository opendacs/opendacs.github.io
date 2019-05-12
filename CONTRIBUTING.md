# Contributing
Before contributing to OpenDACs website, please read the guideline below.
## Branches
This repository is divided in three main branches:

* master
* source
* source-develop

`master` contains source code after hugo compilation and passing Travis-CI deployment. Every commit to this branch will be automatically deployed to github-pages. You should *never* commit or merge to this branch directly. Every change to this branch will be reflected on the main website.

`source` is the default branch when cloning and contains the source code before hugo compilation. This branch should be treated with a the same care as master branch. Commits to this branch should be done by merging `source-develop` or hotfixes branches. Every commit to source will be reflected on the main website after passing Travis-CI deployment. Travis-CI will automatically compile source code with hugo and deploye it to master. For a detailed sequence check [.travis.ylm](https://github.com/opendacs/opendacs.github.io/blob/source/.travis.yml).

`source-develop` runs parallel to to source branch. New developments to the website such as a tutorial should be merge to this branch first. Changes to this branch will not be reflected to the main website until it is merged to `source`.

## Workflow
We suggest the workflow below to ensure development runs smoothly without jeopardizing the main website.

1. [Install Hugo](https://gohugo.io/getting-started/installing/).
2. Clone opendacs.github.io and create a new feature branch for your project. 
```
$ git clone https://github.com/opendacs/opendacs.github.io.git
$ git checkout -b [name_of_your_branch]
``` 
3. Test your changes with `$ hugo server -D` and view them on `http://localhost:1313/`.
4. Commit changes to your feature branch and push it.
```
$ git add .
$ git commit -m '[your_commit_description]'
$ git push origin [name_of_your_branch]
```
5. When your feature branch is ready to merge to `source-develop`, create a pull request to review your contribution.
