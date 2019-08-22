# SINGLETON SD - PIPELINES - ANGULAR TEMPLATE

This project contains templates for angular app and libraries.

> The **main repository** is hosted in [gitlab.com/singletonsd/pipelines/angular](https://gitlab.com/singletonsd/pipelines/angular.git) but it is automaticaly mirrored to [github.com/singletonsd](https://github.com/singletonsd/pipelines-angular.git), [github.com/patoperpetua](https://github.com/patoperpetua/pipelines-angular.git) and to [gitlab.com/patoperpetua](https://gitlab.com/patoperpetua/pipelines-angular.git). If you are in the Github page it may occur that is not updated to the last version.

This templates already include the templates of [npm repository](https://gitlab.com/singletonsd/pipelines/npm).

## HOW TO

### USE

To use it, you can include them as following (using repository aproach):

```yaml
include:
  - project: 'singletonsd/pipelines/angular'
    file: '/src/.gitlab-ci-app.yml'
```

Or using remote aproach over gitlab repo:

```yaml
include:
  - remote: 'https://gitlab.com/singletonsd/pipelines/angular/raw/master/src/.gitlab-ci-app.yml'
```

Or using remote aproach over gilab pages:

```yaml
include:
  - remote: 'https://singletonsd.gitlab.io/pipelines/angular/latest/.gitlab-ci-app.yml'
```

Master branch is setup as latest folder. To use an specific version, put the version name before the file name like:

```yaml
include:
  - remote: 'https://singletonsd.gitlab.io/pipelines/angular/1.0.0/.gitlab-ci-app.yml'
  - remote: 'https://singletonsd.gitlab.io/singletonsd/pipelines/angular/develop/.gitlab-ci-test-app.yml'
  - remote: 'https://singletonsd.gitlab.io/singletonsd/pipelines/angular/feature-new/.gitlab-ci-app.yml'
```

And also define the stages you want to use. It can be both or just one. Remember to include the one you want or main if you use both, like following:

```yaml
stages:
  - install
  - test_static
  - build
  - test_dynamic
  - pre_deploy
  - analysis
  - deploy
```

Remember to define the following variables:

```yaml
variables:

  # To execute the jobs with the desired docker image.
  GLOBAL_IMAGE_NAME: ""
  GLOBAL_IMAGE_TAG: ""

  # To deploy content to AWS S3
  NG_APP_AWS_S3_DEPLOY: "true"
  NG_APP_AWS_S3_REGION: ""
  NG_APP_AWS_S3_ACCESS_KEY_ID: ""
  NG_APP_AWS_S3_SECRET_ACCESS_KEY: ""

  # To execute deploy stage only in the main repository in case you have mirror repositories.
  ORIGINAL_REPOSITORY: ""

  # To run static tests
  TEST_STATIC_ALL: "true"

  # To run dynamic tests
  TEST_STATIC_ALL: "true"
```

### TEST

You can test your .gitlab-ci.yml files by executing the following:

```bash
curl -s https://singletonsd.gitlab.io/scripts/gitlab-ci/latest/gitlab-ci_lint_test_standalone.sh | bash /dev/stdin
```

That script contains the following options:

```bash
-h | --help: display help.
-o | --only: the name of the file or folder to test.
```

Also you can download the script by:

```bash
curl -o gitlab-ci_lint_test_standalone.sh -L https://singletonsd.gitlab.io/scripts/gitlab-ci/latest/gitlab-ci_lint_test_standalone.sh
```

## DOCUMENTATION

- [Gitlab CI - Includes](https://docs.gitlab.com/ee/ci/yaml/)
- [Singleton SD - NPM Common](https://gitlab.com/singletonsd/pipelines/npm.git)

## TODO

- [X] Fix documentation.
- [X] Add app template.
- [ ] Add library template.
- [X] Add script to download test script from gitlab pages.

----------------------

© [Singleton SD](http://www.singletonsd.com), Italy, 2019.
