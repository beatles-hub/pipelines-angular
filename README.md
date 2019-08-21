# SINGLETON SD - PIPELINES - ANGULAR TEMPLATE

This project contains templates for angular common jobs.

> The **main repository** is hosted in [gitlab.com/singletonsd/pipelines/angular](https://gitlab.com/singletonsd/pipelines/angular.git) but it is automaticaly mirrored to [github.com/singletonsd](https://github.com/singletonsd/pipelines-angular.git), [github.com/patoperpetua](https://github.com/patoperpetua/pipelines-angular.git) and to [gitlab.com/patoperpetua](https://gitlab.com/patoperpetua/pipelines-angular.git). If you are in the Github page it may occur that is not updated to the last version.

<!-- TODO: explain that uses common npm template. -->

## AVAILABLE FILES

## HOW TO USE

To use it, you can include them as following (using repository aproach):
<!-- TODO: add project and library templates. -->
```yaml
include:
  - project: 'singletonsd/pipelines/angular'
    file: '/src/.gitlab-ci-main.yml'
```

Or using remote aproach over gitlab repo:
<!-- TODO: add project and library templates. -->
```yaml
include:
  - remote: 'https://gitlab.com/singletonsd/pipelines/angular/raw/master/src/.gitlab-ci-main.yml'
```

Or using remote aproach over gilab pages:
<!-- TODO: add project and library templates. -->
```yaml
include:
  - remote: 'https://singletonsd.gitlab.io/pipelines/angular/.gitlab-ci-main.yml'
```

Master branch is setup as root folder. To use an specific version, put the version name before the file name like:

```yaml
include:
  - remote: 'https://singletonsd.gitlab.io/pipelines/angular/1.0.0/.gitlab-ci-main.yml'
  - remote: 'https://singletonsd.gitlab.io/singletonsd/pipelines/angular/develop/.gitlab-ci-test-main.yml'
  - remote: 'https://singletonsd.gitlab.io/singletonsd/pipelines/angular/feature-new/.gitlab-ci-main.yml'
```

And also define the stages you want to use. It can be both or just one. Remember to include the one you want or main if you use both, like following:

<!-- TODO: add stages-->
```yaml
stages:
```

## DOCUMENTATION

- [Gitlab CI - Includes](https://docs.gitlab.com/ee/ci/yaml/)
- [Singleton SD - NPM Common](https://gitlab.com/singletonsd/pipelines/npm.git)

## TODO

- [ ] Fix documentation.
- [ ] Add project template.
- [ ] Add library template.
- [ ] Add script to download test script from gitlab pages.

----------------------

© [Singleton SD](http://www.singletonsd.com), Italy, 2019.
