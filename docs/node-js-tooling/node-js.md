---
sidebar_position: 2
---

# Node Js

Basically, [Node Js](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs) is javascript runtime that for developers serves the purpose of a local development runner of javascript code. Javascript was designed for the execution in a Browser context. Node Js is used in place of the Browser for local development.

### Toolchain used in my macOS

First, install Node Js from the official site. Installing Node js comes with npm. [npm](https://www.npmjs.com/) is a package manager for javascript packages. A package manager is what is sounds. A command line utility to **manage** packages (dependencies in a project) for development and for production. So that the required information to replicate the project hereafter is easier. Other package managers are [yarn](https://yarnpkg.com/), pnpm, bun. The difference is that they focus on different factors, but basically do the same thing. A common and useful command line utility is the [npx](https://www.npmjs.com/package/npx) package. It is a runner of package binaries that will use locall installed versions or temporally download and then executed the given package binary command.

The real use of npx is usually to scaffold projects using the lastest scaffolding package version by using npx instead of npm or others we assure that the latest version is used when executed in a new directory.

I installed [n](https://www.npmjs.com/package/n) a NodeJS version manager.

