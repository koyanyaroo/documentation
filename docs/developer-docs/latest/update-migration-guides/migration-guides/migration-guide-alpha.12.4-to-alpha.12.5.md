---
title: Migrate from alpha.12.4 to alpha.12.5 - Strapi Developer Docs
description: Learn how you can migrate your Strapi application from alpha.12.4 to alpha.12.5.
canonicalUrl: https://docs.strapi.io/developer-docs/latest/update-migration-guides/migration-guides/migration-guide-alpha.12.4-to-alpha.12.5.html
---

# Migration guide from alpha.12.4 to alpha.12.5

**Here are the major changes:**

- Email providers Mailgun and Sendgrid
- Add Arabic language

**Useful links:**

- Changelog: [https://github.com/strapi/strapi/releases/tag/v3.0.0-alpha.12.5](https://github.com/strapi/strapi/releases/tag/v3.0.0-alpha.12.5)
- GitHub diff: [https://github.com/strapi/strapi/compare/v3.0.0-alpha.12.4...v3.0.0-alpha.12.5](https://github.com/strapi/strapi/compare/v3.0.0-alpha.12.4...v3.0.0-alpha.12.5)

<br>

::: tip
Feel free to [join us on Slack](http://slack.strapi.io) and ask questions about the migration process.
:::

<br>

## Getting started

Install Strapi `alpha.12.5` globally on your computer. To do so run `npm install strapi@3.0.0-alpha.12.5 -g`.

When it's done, generate a new empty project `strapi new myNewProject` (don't pay attention to the database configuration).

<br>

## Update node modules

Update the Strapi's dependencies version (move Strapi's dependencies to `3.0.0-alpha.12.5` version) of your project.

Run `npm install strapi@3.0.0-alpha.12.5 --save` to update your strapi version and then run the same command for `strapi-mongoose` or `strapi-bookshelf` depending on the module you use in your application.

<br>

## Update the Admin

::: tip
If you performed updates in the Admin, you will have to manually migrate your changes.
:::

Delete your old admin folder and replace it with the new one.

<br>

## Update the Plugins

::: tip
If you did a custom update on one of the plugins, you will have to manually migrate your update.
:::

Copy the fields and relations you had in your `/plugins/users-permissions/models/User.settings.json` and `/plugins/users-permissions/config/jwt.json` file in the new one.

Then, delete your old `plugins` folder and replace it with the new one.

<br>

That's all, you have now upgraded to Strapi `alpha.12.5`.
