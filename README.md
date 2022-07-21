# Github Action Tutorial
On this Repository, I trying to figerout how to use Github Actions on big projects.

I watch vedio on udemy.com/[Github Actions](https://www.udemy.com/course/github-actions/).

My strategy learing is: 

>`learn basic only and start doing on a real project later everything will come 🥸` 

## Target.
- automation of build process and deployment.
- automation of CI/CD.
- pull request automation.
- pull request review automation.
  
## Path to the Repository
- [x] [introduction](.github/workflows/simple.yml) 1.5 hours to complete ✅.
  - [x] define the workflow.
    ```yml
    name: simple
    ```
  - [x] define Events to trigger the workflow.
    ```yml
        on:
            push:
            branches:
                - master
            tags:
                - v1.0.0
        ```
        or 
        ```yml
            on: [push]
        ```

  - [x] define the sub-workflow under `jobs`
    ```yml
    jobs:
        build-projects:
    ```
  - [x] select system to use. by `runs-on` attribute.
    ```yml
    jobs:
        build-projects:
        runs-on: ubuntu-latest
    ```
  - [x] define the steps in the workflow and why we need use |.
    ```yml
    jobs:
        build-projects:
        runs-on: ubuntu-latest
        steps:
        - name: echo string
        run: | # use pip for multiple lines.
            echo "Hello World 1"
            echo "Hello World 2"
    ```
  - [x] how use needs attribute and when.
  - [x] how we can use `uses`  attribute to use other actions.
  - [x] pass paramters to actions we are use by use `with`.
- [x] Events, Schedules, External Events & Filters that can be used in a workflow.
  
  You can check file [.github/workflows/actions.yml](.github/workflows/actions.yml) for more information.
    - How use on more advanced like type or specific branch.
    - runing action under condition.
    - `tags` and `branches` can be used to filter the action.
    - `paths` use for directory.
- [x] Environment Variables, Secrets, and encrypted & discrypted file.
- [ ] Strategies, Actions, and Jobs.
- [ ] createing a CI/CD workflow.
- [ ] createing Our Own Github Actions.

# Resources
- [x] [udemy](https://www.udemy.com/course/github-actions/)