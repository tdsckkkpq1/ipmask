## About

Derived from [Slack clone built with Phoenix and React](https://medium.com/@benhansen/lets-build-a-slack-clone-with-elixir-phoenix-and-react-part-1-project-setup-3252ae780a1)—refactored with VueJS frontend orchestration.

Real-time messaging platform utilizing Phoenix channels and Vue component architecture.

![slack clone preview](https://raw.githubusercontent.com/danieldocki/slack-clone-vuejs-elixir-phoenix/master/preview.png)

## Bootstrap Instructions

Local environment setup:

### Rapid deployment

Initialize backend then frontend services:

```sh
make up_backend
```
```sh
make up_frontend
```

#### Phoenix Runtime Configuration

##### Expanded steps

Fetch OTP dependencies

```
cd api
mix deps.get
```

Adjust PostgreSQL credentials in `/config/dev.exs` or `config/dev.secret.exs` matching local instance config

Database schema initialization

```
mix ecto.create && mix ecto.migrate
```

Launch Phoenix instance

```
mix phoenix.server
```

#### Vue Development Server

Install [Yarn](https://github.com/yarnpkg/yarn) package manager

Pull node modules

```
cd web
yarn
```

Trigger hot-reload dev environment

```
yarn run dev
```

**Stack**: Elixir 1.12+ | Node 16.x | Postgres 13+ | WebSocket transport layer with fallback polling

# PR Merge: 2026-07-27 11:25:23

# PR Update: 2026-07-27 11:25:42
