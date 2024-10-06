<a href="https://github.com/Codehagen/Dingify">
  <!-- <img alt="Dingify" src="public/og.jpg"> -->
  <h1 align="center">Dingify</h1>
</a>

<p align="center">
  Start at full speed with Dingify !
</p>


<p align="center">
  <a href="#introduction"><strong>Introduction</strong></a> ·
  <a href="#installation"><strong>Installation</strong></a> ·
  <a href="#tech-stack--features"><strong>Tech Stack + Features</strong></a> ·
  <a href="#author"><strong>Author</strong></a> ·
  <a href="#credits"><strong>Credits</strong></a>
</p>
<br/>

## Introduction

Welcome to Dingify, where we're we are going to make your alerts easy for you

## Directory Structure

Dingify is a monorepo managed by [Turborepo](https://turbo.build/repo). The monorepo is split between `apps` and `packages` directories.

    .
    ├── apps                         # Its app workspace which contains
    │    ├── www                     # Nextjs app which is deployed in Vercel
    │    ├── api                     # Hono app that is our REST-api for our SDK
    │    └── ...
    ├── packages                     # are the shared packages that are used by the apps 
    │    ├── db                      # Prisma DB connector
    │    └── ui                      # Shared UI components (Shadcn)
    ├── tooling                      # are the shared configuration that are used by the apps and packages
    │    ├── eslint                  # Shared eslint presets
    │    ├── prettier                # Shared prettier configuration
    │    ├── tailwind                # Shared tailwind configuration
    │    └── typescript              # Shared tsconfig you can extend from
    ├── LICENSE
    └── README.md

## Installation

Clone & create this repo locally with the following command:

```bash
git clone https://github.com/Codehagen/Dingify
```

1. Install dependencies using pnpm:

```sh
pnpm install
```

2. Copy `.env.example` to `.env.local` and update the variables.

```sh
cp .env.example .env.local
```

4. Input everything you need for the env.

   1. Create [Neon Database](https://neon.tech/) Account
   2. Create [Stripe](https://stripe.com) Account
   3. Create [Google Console](https://console.cloud.google.com/) Account
   4. Create [Resend](https://resend.com/) Account

5. Start the development server from either yarn or turbo:

```sh
# To start the server
pnpm dev

# To push the DB schema
pnpm --filter=db db:push
```

## REST-API Installation (optinal)

If you want to use the REST-api you need to update the hono under `apps/api`

```bash
[vars]
#MY_VAR = "my-variable"
#DATABASE_URL = "Use same link as your db URL"
```

If you want to deploy it on Cloudflare you need to go run
```bash
pnpm run deploy
```

## Tech Stack + Features

### Frameworks

- [Next.js](https://nextjs.org/) – React framework for building performant apps with the best developer experience
- [Auth.js](https://authjs.dev/) – Handle user authentication with ease with providers like Google, Twitter, GitHub, etc.
- [Prisma](https://www.prisma.io/) – Typescript-first ORM for Node.js
- [React Email](https://react.email/) – Versatile email framework for efficient and flexible email development

### Platforms

- [Vercel](https://vercel.com/) – Easily preview & deploy changes with git
- [PlanetScale](https://planetscale.com/) – A cutting-edge database platform for seamless, scalable data management
- [Resend](https://resend.com/) – A powerful email framework for streamlined email development

## Contributing

We love our contributors! Here's how you can contribute:

- [Open an issue](https://github.com/Codehagen/Dingify/issues) if you believe you've encountered a bug.
- Make a [pull request](https://github.com/Codehagen/Dingify/pull) to add new features/make quality-of-life improvements/fix bugs.

<a href="https://github.com/Codehagen/Dingify/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Codehagen/Dingify" />
</a>

## Repo Activity

![Nextify repo activity – generated by Axiom](https://repobeats.axiom.co/api/embed/ca3e357dc3abec5d0e392ee4d10896f5a8fdecb1.svg "Repobeats analytics image")
