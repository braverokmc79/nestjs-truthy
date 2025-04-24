<div align="center">
<img src="./public/images/logo.svg" alt="Truthy Logo">
</div><br>
<h1 align="center">
  Truthy CMS (NestJS Headless API)
</h1>

<p align="center"> 이 저장소는 NestJS로 작성된 Truthy CMS의 백엔드 API 부분입니다. 프론트엔드를 확인하려면 ( https://github.com/gobeam/truthy-react-frontend ) 를 방문하세요. 이 프로젝트에는 인증, 사용자 관리, 역할 관리, 권한 관리, 이메일 모듈, 계정 설정, OTP, RBAC 지원, 지역화 등을 포함한 API가 포함되어 있습니다. </p>
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

**Docker 없이 프로젝트를 실행하려는 경우 .env 파일을 생성할 필요가 없습니다.**

프로덕션 또는 개발 환경에서  **Docker** 를 사용해 배포하려는 경우,
먼저 .env.example 파일을 복사하여 .env 파일을 생성한 뒤, 아래에 나열된 파라미터들에 대해서만 환경변수를 추가하세요.
이 변수들은 docker-compose를 사용해 컨테이너를 빌드하는 데 사용됩니다.

```env
SERVER_PORT=7777
DB_PASSWORD=root
DB_USERNAME=postgres
DB_DATABASE_NAME=truthy
DB_PORT=5488
REDIS_PORT=6399
```

.env 파일을 생성한 후에는, 사용하는 개발 환경에 맞게 설정 파일도 수정해야 합니다.
설정 가이드를 참고하여 누락된 부분이 없는지 확인하세요.

이제 컨테이너를 실행하려면 아래 명령어를 사용하세요:
```bash
docker-compose build .
docker-compose up -d
```
이 명령어들은 PostgreSQL, Redis, Main API 총 3개의 컨테이너를 실행합니다.

Docker 컨테이너에서 마이그레이션을 실행하려면 다음 명령어를 사용하세요:
```bash
docker exec -it <container_id_or_name> yarn migrate
```

To run seeder on docker container
```bash
docker exec -it <container_id_or_name> yarn seed
```

---

## File Structure

이 프로젝트는 다음과 같은 파일 구조를 따릅니다:

```text
truthy
├── config                                  * 모든 설정 파일을 포함합니다.
│   └── default.yml                         * 기본 설정 파일입니다.
│   └── development.yml                     * 개발 환경 설정 파일입니다.
│   └── production.yml                      * 프로덕션 환경 설정 파일입니다.
│   └── test.yml                            * 테스트 환경 설정 파일입니다.
├── coverage                                * `yarn coverage` 명령어 실행 후 생성된 커버리지 보고서입니다.
├── dist                                    * `yarn build` 실행 후 생성된 최적화된 프로덕션 코드입니다.
├── images                                  * 업로드된 프로필 이미지가 저장되는 폴더입니다. 이 폴더는 Git에서 무시됩니다.
├── src                  
│   └── <module>                            * 특정 모듈의 모든 파일이 저장되는 폴더입니다.
│       └── dto                             * 데이터 전송 객체(Data Transfer Object) 파일입니다.
│       └── entity                          * 모듈의 모델 파일입니다.
│       └── pipes                           * NestJS 모듈의 유효성 검사 파이프 파일입니다.
│       └── serializer                      * 모델 데이터를 직렬화하는 파일입니다.
│       └── <module>.controller.ts          * 모듈의 컨트롤러 파일입니다.
│       └── <module>.module.ts              * 모듈의 루트 모듈 파일입니다.
│       └── <module>.service.ts             * 모듈의 서비스 파일입니다.
│       └── <module>.service.spec.ts        * 서비스에 대한 테스트 파일입니다.
│       └── <module>.repository.ts          * 모듈의 리포지토리 파일입니다.
│       └── <module>.repository.spec.ts     * 리포지토리에 대한 테스트 파일입니다.
│   └── common                              * 공통 helper 함수, DTO, 엔터티, 예외, 데코레이터 등을 포함하는 폴더입니다.
│   └── config                              * 설정 변수 파일들을 포함하는 폴더입니다.
│   └── database                            * 데이터베이스 관련 폴더로, 마이그레이션 및 시더 파일이 포함됩니다.
│       └── migrations                      * 모든 마이그레이션 파일을 포함하는 폴더입니다.
│       └── seeds                           * 모든 시더 파일을 포함하는 폴더입니다.
│   └── exception                           * 커스텀 예외를 포함하는 폴더입니다.
│   └── app.module.ts                       * 애플리케이션의 루트 모듈입니다.
│   └── main.ts                             * Nest 애플리케이션 인스턴스를 생성하는 엔트리 파일입니다.
├── test                                    * E2E 테스트를 포함하는 폴더입니다.

```

**Some important root files**

```text

├── .editorconfig                           * 코드 스타일을 설정하는 파일 (프로그래밍 언어별로 적용됨).
├── .env                                    * Docker 환경 변수 설정 파일.
├── .prettierrc.js                          * 코드 포맷팅을 위한 Prettier 설정 파일.
├── .eslintrc.js                            * ESLint 설정 파일 및 규칙.
├── .docker-compose.yml                     * Docker Compose 설정 파일.
├── Dockerfile                              * 프로덕션 환경을 위한 Dockerfile.
├── Dockerfile.dev                          * 개발 환경을 위한 Dockerfile.
├── tsconfig.json                           * 애플리케이션의 TypeScript 설정 파일.

```

---

## Application Security

### Throttle

기본적으로 모든 API에는 요청 제한(Throttle)이 구현되어 있습니다. Redis는 요청 제한 상태 데이터를 기록하는 기본 드라이버로 사용됩니다. 이 설정은 config 파일에서 쉽게 변경할 수 있습니다.

### Two Factor Authentication (2FA)

사용자는 2FA(이중 인증) 옵션을 켜거나 끌 수 있습니다. 2FA에서는 시간 기반 일회성 비밀번호(TOTP)가 사용됩니다. TOTP 애플리케이션은 일정 시간 간격으로 변경되는 인증 코드를 자동으로 생성합니다. Authenticator, 1Password, Authy와 같은 애플리케이션을 사용하여 TOTP를 생성할 수 있습니다.

2FA를 활성화하면 이메일로 QR 코드가 전송됩니다. 이 코드를 위에서 언급한 애플리케이션에서 스캔하면, 해당 애플리케이션이 TOTP를 생성하게 됩니다.

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
