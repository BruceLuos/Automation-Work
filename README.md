This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## Setup
```
bunx --bun create-next-app@latest . --typescript --tailwind --eslint

npx shadcn-ui@latest init

## for acternity-ui https://ui.aceternity.com/components

bun add framer-motion clsx tawilwind-merge 

bun add next-themes

```

## Next.js New Feature
```
"dev": "next dev --experimental-https",
```
it can allow your local dev has a https certificates

## Prisma
```
bun i -D prisma

bunx prisma init
```
Next steps:
1. Set the DATABASE_URL in the .env file to point to your existing database. If your database has no tables yet, read https://pris.ly/d/getting-started
2. Set the provider of the datasource block in schema.prisma to match your database: postgresql, mysql, sqlite, sqlserver, mongodb or cockroachdb.
3. Run prisma db pull to turn your database schema into a Prisma schema.
4. Run prisma generate to generate the Prisma Client. You can then start querying your database.

更新线上数据库
```
bunx prisma db push
```

本地查看prsima 连接的数据库
```
bunx prisma studio
```
## Uploadcare to handle image upload
```
bun add @uploadcare/blocks --save-exact
```

## Clerk.js authentication
```
bun add @clerk/nextjs

```
copy env
https://dashboard.clerk.com/apps/app_2f5FDj2YzpVvYSPBkMMiBonqS8P/instances/ins_2f5FDjAGFjsoCPuHIDfmxNYuUqm

 clerk google scopes settings
 set google drive access

https://www.googleapis.com/auth/userinfo.email
https://www.googleapis.com/auth/userinfo.profile
https://www.googleapis.com/auth/drive.activity.readonly
https://www.googleapis.com/auth/drive.metadata
https://www.googleapis.com/auth/drive.readonly

## Google developer console
get google app clientId and secret key and copy to clerk google auth setting
set auth redirect link 
set test user account
https://console.cloud.google.com/apis/credentials/consent?project=auto-work-420308


## use ngrok for clerk webhooks
get the link from ngrok and copy to the clerk webhooks endpoint
https://dashboard.clerk.com/apps/app_2f5FDj2YzpVvYSPBkMMiBonqS8P/instances/ins_2f5FDjAGFjsoCPuHIDfmxNYuUqm/webhooks

if ngrok link change webhook endpoint need to change too
```
ngrok http https://localhost:3000
```
## Code security 代码中提交了机密内容
[解决方法](https://docs.github.com/zh/enterprise-server@3.11/code-security/secret-scanning/pushing-a-branch-blocked-by-push-protection)