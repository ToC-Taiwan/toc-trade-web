# TOC TRADE WEB

## VS Code

- `.vscode/extensions.json`
  - contains a list of recommended extensions to be installed for this project.

  ```json
  {
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=827846
    "recommendations": [
      "angular.ng-template"
    ]
  }
  ```

- `.vscode/launch.json`
  - contains a list of configurations for debugging the application.

  ```json
  {
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
      {
        "name": "ng serve",
        "type": "chrome",
        "request": "launch",
        "preLaunchTask": "npm: start",
        "url": "http://localhost:4200/"
      },
      {
        "name": "ng test",
        "type": "chrome",
        "request": "launch",
        "preLaunchTask": "npm: test",
        "url": "http://localhost:9876/debug.html"
      }
    ]
  }
  ```

- `.vscode/tasks.json`
  - contains a list of tasks to be run when the `Run Task` command is executed.

  ```json
  {
    // For more information, visit: https://go.microsoft.com/fwlink/?LinkId=733558
    "version": "2.0.0",
    "tasks": [
      {
        "type": "npm",
        "script": "start",
        "isBackground": true,
        "problemMatcher": {
          "owner": "typescript",
          "pattern": "$tsc",
          "background": {
            "activeOnStart": true,
            "beginsPattern": {
              "regexp": "(.*?)"
            },
            "endsPattern": {
              "regexp": "bundle generation complete"
            }
          }
        }
      },
      {
        "type": "npm",
        "script": "test",
        "isBackground": true,
        "problemMatcher": {
          "owner": "typescript",
          "pattern": "$tsc",
          "background": {
            "activeOnStart": true,
            "beginsPattern": {
              "regexp": "(.*?)"
            },
            "endsPattern": {
              "regexp": "bundle generation complete"
            }
          }
        }
      }
    ]
  }
  ```

## CLI

- `ng serve`
  - for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

- `ng generate component component-name`
  - to generate a new component. You can also use

    ```ng generate directive|pipe|service|class|guard|interface|enum|module```

- `ng build`
  - to build the project. The build artifacts will be stored in the `dist/` directory.

- `ng test`
  - to execute the unit tests via [Karma](https://karma-runner.github.io).

- `ng e2e`
  - to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Authors

- [**Tim Hsu**](https://github.com/Chindada)
