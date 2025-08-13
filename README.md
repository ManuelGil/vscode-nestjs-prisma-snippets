# NestJS Prisma Snippets

[![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/imgildev.vscode-nestjs-prisma-snippets?style=for-the-badge&label=VS%20Marketplace&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-prisma-snippets)
[![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/imgildev.vscode-nestjs-prisma-snippets?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-prisma-snippets)
[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/imgildev.vscode-nestjs-prisma-snippets?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-prisma-snippets)
[![Visual Studio Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/imgildev.vscode-nestjs-prisma-snippets?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-prisma-snippets&ssr=false#review-details)
[![GitHub Repo stars](https://img.shields.io/github/stars/ManuelGil/vscode-nestjs-prisma-snippets?style=for-the-badge&logo=github)](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets)
[![GitHub license](https://img.shields.io/github/license/ManuelGil/vscode-nestjs-prisma-snippets?style=for-the-badge&logo=github)](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets/blob/main/LICENSE)

> Snippets for Prisma + NestJS to speed up common patterns and reduce boilerplate in VS Code.

## Overview

This Visual Studio Code extension provides a set of handy snippets tailored for NestJS projects that use Prisma as the ORM. Use the snippets to scaffold services, common Prisma queries, model definitions and module wiring — all with minimal typing.

![demo](https://raw.githubusercontent.com/ManuelGil/vscode-nestjs-prisma-snippets/main/docs/images/demo.gif)

## Requirements

- Visual Studio Code 1.46.0 or later

## Installation

1. Open Visual Studio Code (or a compatible editor).
2. Open the **Extensions** view (`Ctrl+Shift+X` / `⌘+Shift+X`).
3. Search for **NestJS Prisma Snippets** or install directly from the [Marketplace page](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-prisma-snippets).
4. Click **Install** and reload the editor if prompted.

## Usage

Type part of a snippet name, then press `Tab` or `Enter` to expand it.

### Key snippets

| Snippet                           | Purpose                                                         |
| --------------------------------- | --------------------------------------------------------------- |
| `ns_prisma_service`               | `export class PrismaService extends PrismaClient`               |
| `ns_prisma_inject_prisma_service` | `constructor(private readonly prismaService: PrismaService) {}` |
| `ns_prisma_export_default_prisma` | `const prisma = new PrismaClient(); export default prisma`      |
| `ns_prisma_id`                    | `id Int @id @default(autoincrement())`                          |
| `ns_prisma_updated_at`            | `updatedAt DateTime @updatedAt`                                 |
| `ns_prisma_default_now`           | `createdAt DateTime @default(now())`                            |
| `ns_prisma_default_dbgenerated`   | `createdAt DateTime @default(dbgenerated())`                    |
| `ns_prisma_default_cuid`          | `id String @id @default(cuid())`                                |
| `ns_prisma_default_uuid`          | `id String @id @default(uuid())`                                |
| `ns_prisma_relation`              | `@relation(fields: [id], references: [id])`                     |
| `ns_prisma_unique`                | `@@unique([])`                                                  |
| `ns_prisma_map`                   | `@@map("...")`                                                  |
| `ns_prisma_schema`                | `@@schema("...")`                                               |
| `ns_prisma_create`                | `prismaService.create({ data: { ... } })`                       |
| `ns_prisma_find_many`             | `prismaService.findMany({ ... })`                               |
| `ns_prisma_find_unique`           | `prismaService.findUnique({ ... })`                             |
| `ns_prisma_update`                | `prismaService.update({ ... })`                                 |
| `ns_prisma_delete`                | `prismaService.delete({ ... })`                                 |
| `ns_prisma_delete_many`           | `prismaService.deleteMany({ ... })`                             |
| `ns_prisma_upsert`                | `prismaService.upsert({ ... })`                                 |
| `ns_prisma_aggregate`             | `prismaService.aggregate({ ... })`                              |
| `ns_prisma_count`                 | `prismaService.count({ ... })`                                  |
| `ns_prisma_group_by`              | `prismaService.groupBy({ ... })`                                |
| `ns_prisma_findFirst`             | `prismaService.findFirst({ ... })`                              |
| `ns_prisma_order_by`              | `orderBy: { }`                                                  |
| `ns_prisma_where`                 | `where: { }`                                                    |
| `ns_prisma_skip_take`             | `skip , take`                                                   |
| `ns_prisma_include`               | `include: { }`                                                  |
| `ns_prisma_select`                | `select: { }`                                                   |
| `ns_prisma_transaction`           | `this.prismaService.$transaction([])`                           |
| `ns_prisma_query_raw`             | `this.prismaService.$queryRaw()`                                |
| `ns_prisma_execute_raw`           | `this.prismaService.$executeRaw()`                              |
| `ns_prisma_use`                   | `this.prismaService.$use()`                                     |
| `ns_prisma_on`                    | `this.prismaService.$on()`                                      |
| `ns_prisma_disconnect`            | `this.prismaService.$disconnect()`                              |
| `ns_prisma_connect`               | `this.prismaService.$connect()`                                 |
| `ns_prisma_query_raw_unsafe`      | `this.prismaService.$queryRawUnsafe()`                          |
| `ns_prisma_execute_raw_unsafe`    | `this.prismaService.$executeRawUnsafe()`                        |

## Contributing

Contributions to the NestJS Prisma Snippets are welcome and appreciated. To contribute:

1. Fork the [GitHub repository](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets).
2. Create a new branch for your feature or fix:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Make your changes, commit them, and push to your fork.
4. Submit a Pull Request targeting the `main` branch.

Before contributing, please review the [Contribution Guidelines](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets/blob/main/CONTRIBUTING.md) for coding standards, testing, and commit message conventions. If you encounter a bug or wish to request a new feature, please open an Issue.

## Changelog

For a complete list of changes, see the [CHANGELOG.md](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets/blob/main/CHANGELOG.md).

## Authors

- **Manuel Gil** - _Owner_ - [@ManuelGil](https://github.com/ManuelGil)

For a complete list of contributors, please refer to the [contributors](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets/contributors) page.

## Follow Me

- **GitHub**: [![GitHub followers](https://img.shields.io/github/followers/ManuelGil?style=for-the-badge\&logo=github)](https://github.com/ManuelGil)
- **X (formerly Twitter)**: [![X Follow](https://img.shields.io/twitter/follow/imgildev?style=for-the-badge\&logo=x)](https://twitter.com/imgildev)

## Other Extensions

- **[Auto Barrel](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-auto-barrel)**
  Automatically generates and maintains barrel (`index.ts`) files for your TypeScript projects.

- **[Angular File Generator](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-angular-generator)**
  Generates boilerplate and navigates your Angular (9→20+) project from within the editor, with commands for components, services, directives, modules, pipes, guards, reactive snippets, and JSON2TS transformations.

- **[NestJS File Generator](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-generator)**
  Simplifies creation of controllers, services, modules, and more for NestJS projects, with custom commands and Swagger snippets.

- **[NestJS Snippets](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-snippets-extension)**
  Ready-to-use code patterns for creating controllers, services, modules, DTOs, filters, interceptors, and more in NestJS.

- **[T3 Stack / NextJS / ReactJS File Generator](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nextjs-generator)**
  Automates file creation (components, pages, hooks, API routes, etc.) in T3 Stack (Next.js, React) projects and can start your dev server from VSCode.

- **[Drizzle ORM Snippets](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-drizzle-snippets)**
  Collection of code snippets to speed up Drizzle ORM usage, defines schemas, migrations, and common database operations in TypeScript/JavaScript.

- **[CodeIgniter 4 Spark](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-codeigniter4-spark)**
  Scaffolds controllers, models, migrations, libraries, and CLI commands in CodeIgniter 4 projects using Spark, directly from the editor.

- **[CodeIgniter 4 Snippets](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-codeigniter4-snippets)**
  Snippets for accelerating development with CodeIgniter 4, including controllers, models, validations, and more.

- **[CodeIgniter 4 Shield Snippets](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-codeigniter4-shield-snippets)**
  Snippets tailored to CodeIgniter 4 Shield for faster authentication and security-related code.

- **[Mustache Template Engine - Snippets & Autocomplete](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-mustache-snippets)**
  Snippets and autocomplete support for Mustache templates, making HTML templating faster and more reliable.

## Recommended Browser Extension

For developers who work with `.vsix` files for offline installations or distribution, the complementary [**One-Click VSIX**](https://chromewebstore.google.com/detail/imojppdbcecfpeafjagncfplelddhigc?utm_source=item-share-cb) extension is recommended, available for both Chrome and Firefox.

> **One-Click VSIX** integrates a direct "Download Extension" button into each VSCode Marketplace page, ensuring the file is saved with the `.vsix` extension, even if the server provides a `.zip` archive. This simplifies the process of installing or sharing extensions offline by eliminating the need for manual file renaming.

- [Get One-Click VSIX for Chrome &rarr;](https://chromewebstore.google.com/detail/imojppdbcecfpeafjagncfplelddhigc?utm_source=item-share-cb)
- [Get One-Click VSIX for Firefox &rarr;](https://addons.mozilla.org/es-ES/firefox/addon/one-click-vsix/)

## License

This project is licensed under the **MIT License**. See the [LICENSE](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets/blob/main/LICENSE) file for full details.
