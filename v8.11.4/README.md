# test-lint-app > v8.11.4 #

## Create project ##

        ng new marbug-app

* See changes [here](https://github.com/marbug/test-lint-app/compare/master...v8.11.4_step-1_create-project)

## Go to project folder ##

        cd marbug-app

## Generate home module ##

        ng g module home

* See changes [here](https://github.com/marbug/test-lint-app/compare/v8.11.4_step-1_create-project...v8.11.4_step-2_generate-home-module)

## Generate home component ##

        ng g component home

* See changes [here](https://github.com/marbug/test-lint-app/compare/v8.11.4_step-2_generate-home-module...v8.11.4_step-3_generate-home-component)

## Change prefix ##

* Edit **marbug-app/angular.json** file and change prefix from **app** to **marbug**:

              "root": "",
              "sourceRoot": "src",
              "projectType": "application",
        -     "prefix": "app",
        +     "prefix": "marbug",
              "schematics": {},
              "architect": {
                "build": {

* See changes [here](https://github.com/marbug/test-lint-app/compare/v8.11.4_step-3_generate-home-component...v8.11.4_step-4_change-prefix)

TODO

| Navigation |
| ---------- |
| [Up](../README.md) |
