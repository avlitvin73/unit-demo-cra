# CI/CD training project

## For proper testing you need to be a collaborator of this project so feel free to write me on Telegram and i will add you

## About
This project is a training for setting up the CI/CD proccess using GitHub Actions.
The base project i forked is a simple to-do list app with some unit and e2e tests.
In my project i've set up a couple of workflows to automate the integration, deployment and releasing proccesses.
You can try it out by contributing to my repository.

## Features
 - unit tests and e2e tests are run automatically
 - ESLint and Prettier formatting
 - commit names must be written according to [conventional commits style](https://www.conventionalcommits.org/en/v1.0.0/)
 > fix: fixed minor bug in something.js
 - if all the checks pass - you will be able to automatically make a release by adding an appropriate tag
 - tag name must be formed according to [SemVer style](https://semver.org/)
 > v2.0.1
 - when the tag is added - release will be made and deployed from gh-pages branch to [website hosted on GitHub Pages](https://timsxell.github.io/infrastructure-hw)
 - on each release a new issue is made (and instantly closed) that contains the changelog and other info about the release

 ## Try it yourself:
 - **use `npm` as your package manager**

 ### Workflow for basic contributing to the code
 - clone my repository:
 - `git clone https://github.com/timsxell/infrastructure-hw`
- `cd infrastructure-hw`
- install the dependencies:
- `npm ci` or `npm install`
- make a new branch for your feature:
- `git checkout -b "new-branch-name"`
- make some changes in code...
- make a commit, with the commit message being formed by the conventional commits rules:
- `git add .`
- `git commit -m "your commit message in conventional commits styles"`
- `git push origin "new-branch-name"`
- navigate to github to see the test results
- if your changes satisfy the tests you can create a pull request and merge it into master branch

### Workflow for publishing a release
- if you want to make a release version, after finishing the previous workflow, you should add the tag to your last commit:
- `git tag v1.0.0`
> notice that version in tag should be greater than the current version of the app, so, if the current version is v2.0.0, your commit should be tagged at least v2.0.1
- push your tags:
- `git push --tags`
- navigate to github actions and issues to see the result



# Base app description
В этом репозитории находится пример приложения с тестами:

- [e2e тесты](e2e/example.spec.ts)
- [unit тесты](src/example.test.tsx)

Для запуска примеров необходимо установить [NodeJS](https://nodejs.org/en/download/) 16 или выше.

Как запустить:

```sh
# установить зависимости
npm ci

# запустить приложение
npm start
```

Как запустить e2e тесты:

```sh
# скачать браузеры
npx playwright install

# запустить тесты
npm run e2e
```

Как запустить модульные тесты:

```sh
npm test
```
