# Hedwig

LabShare Hedwig

# Packages

- **Packages** : All the packages that are going to be deployed in NPM.
  - **[api](packages/api/hedwig-api)** : Hedwig Server API with Rest and Socket
    interfaces.
  - **[ui](packages/ui/hedwig-ui)** : Hedwig Client UI.

# Tools

- Lerna: For creating Lb-services' monorepo.
  - Configuration File : lerna.json
- Prettier: An opinionated code formatter.
  - Configuration File: .prettierrc
  - Configuration File: .prettierignore
- Lint: Is a code checker that finds common mistakes in scripts.
  - Configuration File: tslint.json
- Commit Lint: Is a git command checker.
  - Configuration File: .commitlintrc.yml
- Mocha: Is a feature-rich JavaScript test framework running on Node.js and in
  the browser.
  - Configuration File : .mocharc.json
- Travis: Continuous Integration Sass.
  - Configuration File : .travis.yml
- NYC: Instrumentation and Coverage generator.
  - Configuration File : .nycrc
- Codecov: Coverage.
  - Configuration File: codecov.yml
- ConventionalCommits: A specification for adding human and machine readable
  meaning to commit messages.
  - Configuration File : .releaserc.json
- Husky: Prevent bad git commands.

# Commands

- **prerelease** - Command that runs before the release (deployment).
- **release** - Command that performs a deployment.
- **postinstall** - Command that is executed after install (automatic).
- **build** - Command that builds a solution.
- **build:full** - Command that cleans and builds a solution.
- **clean** - Command that cleans the solution.
- **lint** - Command that lints the solution.
- **lint:fix** - Command that lints and fix the solution.
- **eslint** - ESLint command.
- **eslint:fix** - ESLint Fix.
- **prettier** - Command that runs prettier simple.
- **prettier:check** - Command that runs prettier and checks errors.
- **prettier:cli** - Command that runs prettier and formats the output for
  errors.
- **prettier:fix** - Command that runs prettier and fix errors.
- **pretest** - Command that runs before tests (automatic).
- **test** - Command that runs test with instrumentation.
- **test:dev** - Command that runs tests.
- **posttest** - Command that is executed after tests (automatic).
- **docker:test** - Docker compose test configuration.
- **docker:test:up** - Start Docker Compose for testing.
- **docker:test:down** - Stop Docker Compose for testing.
- **docker** - Docker compose configuration.
- **docker:up** - Start Docker Compose.
- **docker:down** - Stop Docker Compose.

# Requirements

## Docker Componse

### Tests

In order to run hedwig-api, you will need to have a mongodb and a redis
instance. For development you can use the test's docker-compose file:

To Start:

```sh
  npm run docker:test:up
```

To Stop:

```sh
  npm run docker:test:down
```

### Run

In order to run hedwig-api, you will need to have a mongodb and a redis
instance. You will need to set the NPM_TOKEN value for installing the packages.

To Start:

```sh
  npm run docker:up
```

To Stop:

```sh
  npm run docker:down
```

## Auth

For the current version of projects API , you will need to create an auth tenant
at your a.labshare.org auth site.

# Development

For developing the solution:

- Install nodejs.
- Install lerna - npm i lerna -g
- Download / Fork the Repo.
- Start the test's docker compose.
- Install the repo : `npm i`.
- Execute `npm run build:full`.
- Open each of the projects independently and start the corresponding project.