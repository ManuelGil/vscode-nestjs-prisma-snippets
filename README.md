# NestJS Prisma Snippets for VSCode Editor

[![Latest Release](https://img.shields.io/visual-studio-marketplace/v/imgildev.vscode-nestjs-prisma-snippets?style=flat&label=VS%20Marketplace&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-prisma-snippets)
[![GitHub license](https://img.shields.io/github/license/ManuelGil/vscode-nestjs-prisma-snippets)]()

This extension for Visual Studio Code adds snippets for NestJS and Prisma ORM. Now you can create your NestJS and Prisma ORM files faster and easier.

## Requirements

- VSCode 1.46.0 or later

## Usage

### Snippets

![demo](https://raw.githubusercontent.com/ManuelGil/vscode-nestjs-prisma-snippets/main/docs/images/demo.gif)

Type part of snippet, press `Tab` or `Enter`, and the snippet unfolds. Below is a list of the most important shortcuts.

| Snippet | Purpose |
| --- | --- |
| ns_prisma_service | export class PrismaService extends PrismaClient |
| ns_prisma_inject_prisma_service | constructor(private readonly prismaService: PrismaService) {} |
| ns_prisma_export_default_prisma | export default const prisma = new PrismaClient() |
| ns_prisma_id | id Int @id @default(autoincrement()) |
| ns_prisma_updated_at | updatedAt DateTime @updatedAt |
| ns_prisma_default_now | createdAt DateTime @default(now()) |
| ns_prisma_default_dbgenerated | createdAt DateTime @default(dbgenerated()) |
| ns_prisma_default_cuid | id String @id @default(cuid()) |
| ns_prisma_default_uuid | id String @id @default(uuid()) |
| ns_prisma_default_sequential | id Int @id @default(sequential()) |
| ns_prisma_default_random | id Int @id @default(random()) |
| ns_prisma_default_anonymous | id Int @id @default(anonymous()) |
| ns_prisma_relation | @relation(fields: [Id], references: [id]) |
| ns_prisma_unique | @@unique([]) |
| ns_prisma_map | @@map() |
| ns_prisma_schema | @@schema() |
| ns_prisma_create | prismaService.create({ data: { ... } }) |
| ns_prisma_find_many | prismaService.findMany({ ... }) |
| ns_prisma_find_unique | prismaService.findUnique({ ... }) |
| ns_prisma_update | prismaService.update({ ... }) |
| ns_prisma_delete | prismaService.delete({ ... }) |
| ns_prisma_delete_many | prismaService.deleteMany({ ... }) |
| ns_prisma_upsert | prismaService.upsert({ ... }) |
| ns_prisma_aggregate | prismaService.aggregate({ ... }) |
| ns_prisma_count | prismaService.count({ ... }) |
| ns_prisma_group_by | prismaService.groupBy({ ... }) |
| ns_prisma_findFirst | prismaService.findFirst({ ... }) |
| ns_prisma_order_by | orderBy: { } |
| ns_prisma_where | where: { } |
| ns_prisma_skip_take | skip , take |
| ns_prisma_include | include: { } |
| ns_prisma_select | select: { } |
| ns_prisma_transaction | this.prismaService.$transaction([]) |
| ns_prisma_query_raw | this.prismaService.$queryRaw() |
| ns_prisma_execute_raw | this.prismaService.$executeRaw() |
| ns_prisma_use | this.prismaService.$use() |
| ns_prisma_on | this.prismaService.$on() |
| ns_prisma_disconnect | this.prismaService.$disconnect() |
| ns_prisma_connect | this.prismaService.$connect() |
| ns_prisma_query_raw_unsafe | this.prismaService.$queryRawUnsafe() |
| ns_prisma_execute_raw_unsafe | this.prismaService.$executeRawUnsafe() |

## Other Extensions

- [NestJS File Generator for VSCode](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-generator)
- [NestJS Snippets for VSCode Editor](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nestjs-snippets-extension)
- [Angular File Generator for VSCode Editor](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-angular-generator)
- [React / NextJS / T3 Stack File Generator](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nextjs-generator)
- [Nx / Angular / Nest / Next Essential Extension Pack](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-nx-pack)
- [CodeIgniter 4 Snippets for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-codeigniter4-shield-snippets)
- [CodeIgniter 4 Spark for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-codeigniter4-shield-spark)
- [Moodle Pack](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-moodle-snippets)
- [Mustache Template Engine - Snippets & Autocomplete](https://marketplace.visualstudio.com/items?itemName=imgildev.vscode-mustache-snippets)

## Changelog

See [CHANGELOG.md](./CHANGELOG.md)

## Authors

- **Manuel Gil** - _Owner_ - [ManuelGil](https://github.com/ManuelGil)

See also the list of [contributors](https://github.com/ManuelGil/vscode-nestjs-prisma-snippets/contributors) who participated in this project.

## License

NestJS Prisma Snippets for VSCode is licensed under the MIT License - see the [MIT License](https://opensource.org/licenses/MIT) for details.
