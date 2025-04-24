<div align="center">
<img src="./public/images/logo.svg" alt="Truthy Logo">
</div><br>
<h1 align="center">
  Truthy CMS (NestJS Headless API)
</h1>

<p align="center"> 이 저장소는 NestJS로 작성된 Truthy CMS의 백엔드 API 부분입니다. 프론트엔드를 확인하려면 [https://github.com/gobeam/truthy-react-frontend](https://github.com/gobeam/truthy-react-frontend)를 방문하세요. 이 프로젝트에는 인증, 사용자 관리, 역할 관리, 권한 관리, 이메일 모듈, 계정 설정, OTP, RBAC 지원, 지역화 등을 포함한 API가 포함되어 있습니다. </p>
<br>
<p align="center">
<img alt="GitHub package.json version" src="https://img.shields.io/github/package-json/v/gobeam/truthy">
<img alt="Workflow test" src="https://github.com/gobeam/truthy/actions/workflows/ci.yml/badge.svg">
<img alt="GitHub" src="https://img.shields.io/github/license/gobeam/truthy">
<img alt="Lines of code" src="https://img.shields.io/tokei/lines/github/gobeam/truthy">
<img src='https://www.codetriage.com/gobeam/truthy/badges/users.svg' alt='Open Source Helpers' />
</p>
<p align="center">
<a href="https://www.buymeacoffee.com/gobeam" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-green.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
</p>
<p align="center">
  <sub>Created by <a href="https://www.linkedin.com/in/roshan-ranabhat/">Roshan Ranabhat (gobeam)</a> and maintained with ❤️ by an amazing <a href="https://github.com/gobeam/truthy-contributors">team of awesome developers</a>.</sub>
</p>

<p align="center">
  <sub>Check Live code deployed here:  Backend API Docs: <a href="http://157.245.148.131:7777/api-docs/">Swagger Docs</a>
  Frontend: <a href="http://157.245.148.131:3000">Truthy CMS</a>
  </sub>
</p>

<p align="center">
<img src="https://gobeam.github.io/truthy-contributors/truthy.gif" alt="Truthy CMS" >
</p>

## Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#Prerequisites)
- [Available Scripts](#available-scripts)
- [Setup](#setup)
- [Docker Setup](#docker-setup)
- [File Structure](#file-structure)
- [Application Security](#application-security)
- [Contributing](#contributing)
- [Sponsors](#sponsors)
- [License](#license)
- [Acknowledgement](#acknowledgement)

---

## Getting Started

이 프로젝트는 표준 CMS를 개발할 때 꼭 필요한 기본 모듈을 부트스트랩 형태로 제공하여 개발자의 생산성을 높이기 위해 만들어졌습니다. Truthy CMS의 주요 목적은 CMS를 개발할 때 반복적으로 작성되는 공통 기능 구현 시간을 줄이고, 핵심 기능에 집중할 수 있도록 돕는 것입니다.

이 프로젝트는 가능한 한 최상의 코드 품질과 표준을 따르며, 최적화 및 실제 서비스 환경에서도 바로 사용할 수 있도록 설계되었습니다. 이 프로젝트가 여러분의 시간과 노력을 절약해줄 수 있기를 바랍니다. 😊

이 프로젝트가 마음에 드셨다면, 사용 후기를 공유해 주세요! API, 프론트엔드, 디자인, 로고 등 어떤 형태로든 Truthy CMS에 기여하고 싶으시다면 언제든지 환영합니다. 저희의 목표는 오픈소스 커뮤니티에 의해 유지되고 성장하는 최고의 CMS가 되는 것입니다.

---

## Prerequisites

NodeJS
https://nodejs.org/en/

Typescript
https://www.typescriptlang.org/

PostgresQL
https://www.postgresql.org/

Redis
https://redis.io/

---

## Available Scripts

### npx truthy-api

이 명령어는 최신 버전의 Truthy, 즉 NestJS Truthy CMS 백엔드 API를 다운로드합니다.

프로젝트 디렉토리에서 다음 명령어를 실행할 수 있습니다:

### `yarn start:dev`

앱을 개발 및 감시(watch) 모드로 실행합니다.<br>
브라우저에서 http://localhost:7777/api-docs를 열면 Swagger API 문서를 확인할 수 있습니다 (개발 모드에서만 제공됨).<br>
또한 콘솔에서 린트(lint) 오류도 확인할 수 있습니다.

### `yarn build`

앱을 프로덕션용으로 빌드하여 build 폴더에 출력합니다.<br>

### `yarn lint`

src, apps, libs, test 폴더 내 모든 파일을 린트하고 결과를 표시합니다.

### `yarn format`

.prettierrc에 제공된 설정을 사용하여 src 내 모든 파일을 Prettier로 포맷합니다.

### `yarn coverage`

커버리지 테스트 명령어를 실행하고 coverage 폴더를 생성하여 상세 보고서를 작성합니다. 보고서는 다음 경로에서 확인할 수 있습니다:
```bash
yarn coveralls
```

### `yarn orm-create migration_file_name`

Type ORM을 사용하여 마이그레이션 파일을 생성합니다. migration_file_name은 생성할 마이그레이션 파일의 이름입니다.

### `yarn migrate`

이 명령어는 기존의 마이그레이션 파일을 마이그레이션하는 데 사용됩니다.

### `yarn migration:rollback`

이 명령어는 마이그레이션을 롤백하는 데 사용됩니다.

### `yarn seed`

이 명령어는 기존의 시더(seeders)를 실행하는 데 사용됩니다.

---

## Setup

먼저, npx 명령어를 사용하여 프로젝트를 설치해야 합니다.

```bash
npx truthy-api
```

or clone it using

```bash
git clone https://github.com/gobeam/truthy.git
```
**PostgreSQL은 데이터베이스 용도로, Redis는 큐 및 요청 제한(Throttling) 처리를 위한 키-값 저장소로 사용되므로 함께 실행해야 합니다.**
프로젝트를 클론한 후에는 프로젝트 루트에 있는 config 폴더 내의 설정 파일을 수정해야 합니다.
설정 파일의 이름은 실행할 환경에 따라 지정되어 있습니다. 예를 들어, 개발 환경에서 프로젝트를 실행하는 경우 development.yml 파일을 수정해야 합니다.
**주의: 환경 변수는 항상 설정 파일의 값을 우선하여 덮어쓴다는 점을 꼭 기억하세요.**

If you want to run locally,
```bash
yarn start
```
*If you want to view swagger docs on development open http://localhost:7777/api-docs (assuming you are running application on 7777 port)*

Run Migration
```bash
yarn migrate
```

Run Seeders
```bash
yarn seed
```

Rollback Migration
```bash
yarn migration:rollback
```

---

## Docker Setup

**If you want to run project without docker you will not need to create .env file**

If you want to use **Docker** to deploy it on production or development stage
First create a .env file copying from .env.example and add environment for below parameters only since it will be used for building container using docker-compose

```env
SERVER_PORT=7777
DB_PASSWORD=root
DB_USERNAME=postgres
DB_DATABASE_NAME=truthy
DB_PORT=5488
REDIS_PORT=6399
```

After creating env file make changes in configuration in accordance with you development environment. Follow setup guide in case you missed it.
 
Now to run containers do
```bash
docker-compose build .
docker-compose up -d
```
These commands will run 3 containers for PostgresQL, Redis and Main API.

To run migration on docker container
```bash
docker exec -it <container_id_or_name> yarn migrate
```

To run seeder on docker container
```bash
docker exec -it <container_id_or_name> yarn seed
```

---

## File Structure

This project follows the following file structure:

```text
truthy
├── config                                  * Contains all configuration files
│   └── default.yml                         * Default configuration file.
│   └── development.yml                     * Configuration file for development environment.
│   └── production.yml                      * Configuration file for production environment.
│   └── test.yml                            * Configuration file for test environment.    
├── coverage                                * Coverage reports after running `yarn coverage` command. 
├── dist                                    * Optimized code for production after `yarn build` is run.
├── images                                  * this folder is where uploaded profile images are stored. This folder is git ignored.
├── src                  
│   └── <module>                            * Folder where specific modules all files are stored
│       └── dto                             * Data Transfer Objects.
│       └── entity                          * Models for module.
│       └── pipes                           * Includes validation pipes for NestJS modules.
│       └── serializer                      * Includes serializer for model data.
│       └── <module>.controller.ts          * Controller file.
│       └── <module>.module.ts              * root module file for module.
│       └── <module>.service.ts             * Service file for <module>.
│       └── <module>.service.spec.ts        * Test file for service.
│       └── <module>.repository.ts          * Repository file for <module>.
│       └── <module>.repository.spec.ts     * Test file for repository.
│   └── common                              * Common helpers function, dto, entity, exception, decorators etc.
│   └── config                              * Configuration variables files.
│   └── database                            * Database folders that includes migration and seeders file
│       └── migrations                      * Migration folder includes all migration files.
│       └── seeds                           * Seeds folder includes all seeders files.
│   └── exception                           * Exception folder includes custom exceptions.
│   └── app.module.ts                       * Root module of the application.
│   └── main.ts                             * The entry file of the application which uses the core function NestFactory to create a Nest application instance.
├── test                                    * Contains E2E tests 
```

**Some important root files**

```text
.
├── .editorconfig                           * Coding styles (also by programming language).
├── .env                                    * Environment variables for docker.
├── .prettierrc.js                          * Formatting Prettier options.
├── .eslintrc.js                            * ESLint configuration and rules.
├── .docker-compose.yml                     * Docker compose configuration.
├── Dockerfile                              * Docker file for prod environment.
├── Dockerfile.dev                          * Docker file for dev environment.
├── tsconfig.json                           * Typescript configuration for application.
```

---

## Application Security

### Throttle

By default Throttle has been implemented for all API's. Redis is default driver to record throttle state data. You can easily change configuration from config files.

### Two Factor Authentication (2FA)

User Will have 2FA authentication option available to be turned on or off. For 2FA time-based one-time password is used. A time-based one-time password (TOTP) application automatically generates an authentication code that changes after a certain period of time. Applications like [Authenticator](https://play.google.com/store/apps/details?id=com.azure.authenticator&hl=en&gl=US), [1Password](https://support.1password.com/one-time-passwords/), [Authy](https://authy.com/guides/github/) etc. can be used to generate TOTP. When you enable 2FA, you will be sent a QR code in your email which should be scanned from above mentioned application and TOTP will be generated by those applications.

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate. - see `CONTRIBUTING.md` for details.
**If you want to be featured in contributors list on our home page please add PR on https://github.com/gobeam/truthy-contributors to provide your details.**

---

## License

Released under the MIT License - see `LICENSE.md` for details.

---

## Acknowledgement

- [NestJS](https://github.com/nestjs/nest)
