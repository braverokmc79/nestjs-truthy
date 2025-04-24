# Truthy CMS (NestJS Headless API)

이 저장소는 Truthy CMS의 백엔드 API로, NestJS로 작성되었습니다. 프론트엔드는 다음 링크에서 확인할 수 있습니다: [Truthy React Frontend](https://github.com/gobeam/truthy-react-frontend).

이 프로젝트는 인증, 사용자 관리, 역할 및 권한 관리, 이메일 모듈, 계정 설정, OTP, RBAC 지원, 로컬라이제이션 등 다양한 기능을 포함하고 있습니다.

[Swagger API 문서 보기](http://157.245.148.131:7777/api-docs)
[프론트엔드 접근](http://157.245.148.131:3000)

---

## 목차

- 시작하기
- 사전 준비 사항
- 사용 가능한 스크립트
- 설치 방법
- Docker 설정
- 파일 구조
- 애플리케이션 보안
- 기여하기
- 후원자
- 라이선스
- 감사의 말

---

## 시작하기

Truthy CMS는 표준 CMS를 개발할 때 필수적인 모듈을 부트스트랩하는 데 도움을 주기 위해 만들어졌습니다. 이 프로젝트는 최적화 및 프로덕션 준비가 된 상태를 목표로 하며, 개발 시간을 절약하고 핵심 기능 구현에 집중할 수 있도록 돕습니다. 오픈소스 커뮤니티에 의해 유지되는 최고의 CMS가 되는 것이 목표입니다.

---

## 사전 준비 사항

- [NodeJS](https://nodejs.org/en/)
- [Typescript](https://www.typescriptlang.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Redis](https://redis.io/)

---

## 사용 가능한 스크립트

- `npx truthy-api`: 최신 Truthy CMS 백엔드 API 설치
- `yarn start:dev`: 개발 모드로 실행 및 Swagger 문서 확인 가능
- `yarn build`: 프로덕션 빌드 생성
- `yarn lint`: 코드 린트
- `yarn format`: Prettier 포맷 적용
- `yarn coverage`: 테스트 커버리지 리포트 생성
- `yarn orm-create <파일명>`: 마이그레이션 파일 생성
- `yarn migrate`: 마이그레이션 적용
- `yarn migration:rollback`: 마이그레이션 롤백
- `yarn seed`: 시더 실행

---

## 설치 방법

```bash
npx truthy-api
# 또는
git clone https://github.com/gobeam/truthy.git
```

PostgreSQL과 Redis가 실행되어 있어야 합니다. 설정 파일은 `config` 폴더의 `development.yml` 등에서 환경에 따라 수정하세요. 

로컬 실행:
```bash
yarn start
```

마이그레이션 실행:
```bash
yarn migrate
```

시더 실행:
```bash
yarn seed
```

---

## Docker 설정

`.env.example`을 참고하여 `.env` 파일을 생성합니다:
```env
SERVER_PORT=7777
DB_PASSWORD=root
DB_USERNAME=postgres
DB_DATABASE_NAME=truthy
DB_PORT=5488
REDIS_PORT=6399
```

도커 빌드 및 실행:
```bash
docker-compose build .
docker-compose up -d
```

도커 컨테이너에서 마이그레이션 실행:
```bash
docker exec -it <컨테이너명> yarn migrate
```

도커 컨테이너에서 시더 실행:
```bash
docker exec -it <컨테이너명> yarn seed
```

---

## 파일 구조

```text
truthy
├── config                # 환경설정 파일
├── coverage              # 커버리지 리포트
├── dist                  # 빌드 후 결과
├── images                # 업로드된 이미지 (git 제외)
├── src                   # 소스 코드
│   └── <module>          # 모듈별 구성
│   └── common            # 공통 헬퍼 및 예외
│   └── config            # 구성 변수 파일
│   └── database          # 마이그레이션 및 시더
│   └── exception         # 커스텀 예외
├── test                  # E2E 테스트
```

중요 루트 파일:
```text
.editorconfig, .env, .prettierrc.js, .eslintrc.js,
.docker-compose.yml, Dockerfile, Dockerfile.dev, tsconfig.json
```

---

## 애플리케이션 보안

### 요청 제한 (Throttle)
Redis를 사용하여 API 요청 제한 설정이 되어 있으며, 구성 파일에서 쉽게 수정 가능합니다.

### 2단계 인증 (2FA)
시간 기반 일회용 비밀번호(TOTP)를 사용하는 2FA 지원. 인증 앱(예: Google Authenticator, 1Password, Authy 등)으로 QR 코드 스캔 후 사용 가능합니다.

---

## 기여하기

Pull Request는 언제나 환영입니다! 큰 변경은 먼저 이슈를 통해 논의해주세요. 
홈페이지 기여자 리스트에 포함되기를 원하신다면 [truthy-contributors](https://github.com/gobeam/truthy-contributors)에 PR을 보내주세요.

---

## 라이선스

MIT 라이선스 하에 배포됩니다. 자세한 내용은 `LICENSE.md` 파일을 확인하세요.

---

## 감사의 말

- [NestJS](https://github.com/nestjs/nest)
