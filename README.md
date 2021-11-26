<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://coveralls.io/github/nestjs/nest?branch=master" target="_blank"><img src="https://coveralls.io/repos/github/nestjs/nest/badge.svg?branch=master#9" alt="Coverage" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ npm install
```

## Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Test

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://kamilmysliwiec.com)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](LICENSE).

##  EKI NOTE :



## 1. installation Docker, Postgresql
```bash
install vm alpine + docker
https://github.com/EKI-INDRADI/eki-latihan-vm-alpine-docker-portable

install Docker, Postgresql
https://github.com/EKI-INDRADI/eki-latihan-docker-postgresql

create database simple_pos
```

## 2. install nodejs & nestjs

```bash
install nodejs   (https://nodejs.org)

npm i -g @nestjs/cli
nest --version
```

## ==== STAGE 9 = MIGRATION MYSQL TO POSTGRESQL TypeORM

<details>
  <summary>20211126-0044-MYSQL-TO-MIGRATION-POSTGRESQL</summary>

```bash
/044

// ===================== MIGRATION MYSQL TO POSTGRESQL
1. install postgresql database

2. create database simple_pos

3. npm uninstall mysql2

4. delete node_modules

5. npm i

6. npm install pg

7. rubah .env 

--- before

MYSQL_HOST = '127.0.0.1'
MYSQL_PORT = '3400'
MYSQL_USER = 'root'
MYSQL_PASSWORD = 'masuk123'
MYSQL_DATABASE = 'simple_pos'
JWT_SECRET_KEY= 'eki-secret-key'

--- /before

--- after

POSTGRESQL_HOST = '127.0.0.1'
POSTGRESQL_PORT = '5400'
POSTGRESQL_USER = 'postgres'
POSTGRESQL_PASSWORD = 'masuk123'
POSTGRESQL_DATABASE = 'simple_pos'
JWT_SECRET_KEY= 'eki-secret-key'

--- /after

8. disable sementara code pada src\user\user.controller.ts
// @ApiBearerAuth() 
// @UseGuards(JwtGuard) 

lalu buat pada http://localhost:3000/api-docs/
POST /USER 
{
  "nama_user": "stringst",
  "email": "string@mail.com",
  "username": "stringst",
  "password": "stringst"
}


9. setelah selesai code pada src\user\user.controller.ts
enable kembali 
@ApiBearerAuth() 
@UseGuards(JwtGuard) 

10. selesai maka seluruh table akan otomatis terbuat , dan langsung dapat digunakan, persis seperti pada MySQL

// ===================== MIGRATION MYSQL TO POSTGRESQL

```

</details>

## ==== /STAGE 8 = MANUAL QUERY


 
## REFERENSI :

https://github.com/EKI-INDRADI/eki-latihan-nestjs-mysql

## EKI INDRADI

"TIME > KNOWLEDGE > MONEY". #STILL_ONE_DIGIT
