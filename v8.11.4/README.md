# Test lint > v8.11.4 #

## Create project ##

        ng new marbug-app

* See changes [here](https://github.com/marbug/test-lint/compare/master...v8.11.4_step-1_create-project)

* Please, run

        npm run lint

    and see no error

## Go to project folder ##

        cd marbug-app

## Generate home module ##

        ng g module home

* See changes [here](https://github.com/marbug/test-lint/compare/v8.11.4_step-1_create-project...v8.11.4_step-2_generate-home-module)

* Please, run

        npm run lint

    and see no error

## Generate home component ##

        ng g component home

* See changes [here](https://github.com/marbug/test-lint/compare/v8.11.4_step-2_generate-home-module...v8.11.4_step-3_generate-home-component)

* Please, run

        npm run lint

    and see no error

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

* See changes [here](https://github.com/marbug/test-lint/compare/v8.11.4_step-3_generate-home-component...v8.11.4_step-4_change-prefix)

* Please, check for lint errors

        npm run lint

    and see no error

## Change component selector prefix ##

* Edit **marbug-app/src/app/home/home.component.ts** file and change component selector prefix from **app** to **marbug**:

                @Component({
        -         selector: 'app-home',
        +         selector: 'marbug-home',
                  templateUrl: './home.component.html',
                  styleUrls: ['./home.component.css']
                })

* See changes [here](https://github.com/marbug/test-lint/compare/v8.11.4_step-4_change-prefix...v8.11.4_step-5_change-component-selector-prefix)

* Please, check for lint errors

        npm run lint

    and see error

        ERROR: /Users/marbug/cpp/angular/test-lint/marbug-app/src/app/home/home.component.ts[4, 13]: The selector of the component "HomeComponent" should have prefix "app" (https://angular.io/styleguide#style-02-07)

        Lint errors found in the listed files.

## Add component-selector rule ##

* Edit **marbug-app/tslint.json** file and add **component-selector** rule:

             "no-output-rename": true,
             "use-life-cycle-interface": true,
             "use-pipe-transform-interface": true,
        +    "component-selector": [true, "element", "marbug", "kebab-case"],
             "component-class-suffix": true,
             "directive-class-suffix": true
           }

* See changes [here](https://github.com/marbug/test-lint/compare/v8.11.4_step-5_change-component-selector-prefix...v8.11.4_step-6_add-component-selector-rule)

* Please, check for lint errors

        npm run lint

    and see error

        ERROR: /Users/marbug/cpp/angular/test-lint/marbug-app/src/app/home/home.component.ts[4, 13]: The selector of the component "HomeComponent" should have prefix "app" (https://angular.io/styleguide#style-02-07)

        Lint errors found in the listed files.

| Navigation |
| ---------- |
| [Up](../README.md) |
