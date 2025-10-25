<p align="center">
  <img src="https://content.umami.is/website/images/umami-logo.png" alt="Umami Logo" width="100">
</p>

<h1 align="center">Umami</h1>

<p align="center">
  <i>Umami 是一个简单、快速、注重隐私的 Google Analytics 替代品。</i>
</p>

<p align="center">
  <a href="https://github.com/umami-software/umami/releases">
    <img src="https://img.shields.io/github/release/umami-software/umami.svg" alt="GitHub Release" />
  </a>
  <a href="https://github.com/umami-software/umami/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/umami-software/umami.svg" alt="MIT License" />
  </a>
  <a href="https://github.com/umami-software/umami/actions">
    <img src="https://img.shields.io/github/actions/workflow/status/umami-software/umami/ci.yml" alt="Build Status" />
  </a>
  <a href="https://analytics.umami.is/share/LGazGOecbDtaIwDr/umami.is" style="text-decoration: none;">
    <img src="https://img.shields.io/badge/Try%20Demo%20Now-Click%20Here-brightgreen" alt="Umami Demo" />
  </a>
</p>

---

## 🚀 快速开始

详细的入门指南可以在 [umami.is/docs](https://umami.is/docs/) 找到。

---

## 🛠 从源码安装

### 环境要求

-   装有 Node.js 版本 18.18 或更高的服务器
-   数据库。Umami 支持 [MariaDB](https://www.mariadb.org/) (最低 v10.5)、[MySQL](https://www.mysql.com/) (最低 v8.0) 和 [PostgreSQL](https://www.postgresql.org/) (最低 v12.14) 数据库。

### 获取源代码并安装依赖包

```bash
git clone https://github.com/umami-software/umami.git
cd umami
pnpm install
```

### 配置 Umami

创建一个 `.env` 文件，内容如下：

```bash
DATABASE_URL=connection-url
```

连接 URL 格式：

```bash
postgresql://username:mypassword@localhost:5432/mydb
mysql://username:mypassword@localhost:3306/mydb
```

### 构建应用

```bash
pnpm run build
```

_如果是首次安装，构建步骤将在您的数据库中创建所需的表。它还会创建一个登录用户，用户名为 **admin**，密码为 **umami**。_

### 启动应用

```bash
pnpm run start
```

_默认情况下，这将在 `http://localhost:3000` 上启动应用程序。您需要从您的 Web 服务器[代理](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/)请求，或者更改[端口](https://nextjs.org/docs/api-reference/cli#production)以直接提供应用服务。_

---

## 🐳 使用 Docker 安装

要构建 Umami 容器并启动 Postgres 数据库，请运行：

```bash
docker compose up -d
```

或者，仅拉取支持 PostgreSQL 的 Umami Docker 镜像：

```bash
docker pull docker.umami.is/umami-software/umami:postgresql-latest
```

或者拉取支持 MySQL 的镜像：

```bash
docker pull docker.umami.is/umami-software/umami:mysql-latest
```

---

## 🔄 获取更新

要获取最新功能，只需执行拉取操作，安装任何新的依赖项，然后重新构建：

```bash
git pull
pnpm install
pnpm run build
```

要更新 Docker 镜像，只需拉取新镜像并重新构建：

```bash
docker compose pull
docker compose up --force-recreate -d
```

---

## 🛟 支持

<p align="center">
  <a href="https://github.com/umami-software/umami">
    <img src="https://img.shields.io/badge/GitHub--blue?style=social&logo=github" alt="GitHub" />
  </a>
  <a href="https://twitter.com/umami_software">
    <img src="https://img.shields.io/badge/Twitter--blue?style=social&logo=twitter" alt="Twitter" />
  </a>
  <a href="https://linkedin.com/company/umami-software">
    <img src="https://img.shields.io/badge/LinkedIn--blue?style=social&logo=linkedin" alt="LinkedIn" />
  </a>
  <a href="https://umami.is/discord">
    <img src="https://img.shields.io/badge/Discord--blue?style=social&logo=discord" alt="Discord" />
  </a>
</p>

[release-shield]: https://img.shields.io/github/release/umami-software/umami.svg
[releases-url]: https://github.com/umami-software/umami/releases
[license-shield]: https://img.shields.io/github/license/umami-software/umami.svg
[license-url]: https://github.com/umami-software/umami/blob/master/LICENSE
[build-shield]: https://img.shields.io/github/actions/workflow/status/umami-software/umami/ci.yml
[build-url]: https://github.com/umami-software/umami/actions
[github-shield]: https://img.shields.io/badge/GitHub--blue?style=social&logo=github
[github-url]: https://github.com/umami-software/umami
[twitter-shield]: https://img.shields.io/badge/Twitter--blue?style=social&logo=twitter
[twitter-url]: https://twitter.com/umami_software
[linkedin-shield]: https://img.shields.io/badge/LinkedIn--blue?style=social&logo=linkedin
[linkedin-url]: https://linkedin.com/company/umami-software
[discord-shield]: https://img.shields.io/badge/Discord--blue?style=social&logo=discord
[discord-url]: https://discord.com/invite/4dz4zcXYrQ
