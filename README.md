# Github Actions for Quarto

This repository stores [Github Actions](https://github.com/features/actions) around Quarto (https://quarto.org/)

1. [quarto-dev/quarto-actions/setup](https://github.com/quarto-dev/actions/tree/master/setup) - Install Quarto
2. [quarto-dev/quarto-actions/render](https://github.com/quarto-dev/actions/tree/master/render) - Render project
3. [quarto-dev/quarto-actions/publish](https://github.com/quarto-dev/actions/tree/master/publish) - Publish project

We recommend using `v2` for your actions, and our examples all use `v2`.

## Examples

In [Examples](./examples), you will find some YAML workflow files to serve as templates to be reused as a base for your project. We are also sharing some links to real example Github repositories using Quarto with Github Actions for rendering and deploying documents and projects. If you want to add your repository in the list, we welcome a PR.

## Release Management

This repository is using [recommended release management for actions](https://docs.github.com/en/actions/creating-actions/about-custom-actions#using-release-management-for-actions): 

* Github releases with tags are used for updates on the actions. 
* Semantic versioning is used, with major, minor and possibly patch release. 
* Major version (such as `v1`) will always point to the last minor or patch release for this major version. (when `v1.0.2` is out, `v1` will point to this update to). This means using `quarto-dev/quarto-actions/setup@v2` in your workflow file will automatically get the updated versions. Using `quarto-dev/quarto-actions/setup@v1.0.2` will pin a specific release.
* Major version change (`v1` to `v2`) will often come with a possible breaking change, and a workflow would require manual update.