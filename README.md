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

# Steps

## 0. Project Setup

1. in your terminal, run `npx create-next-app@latest` as it says in https://nextjs.org/
2. run `npm run dev`
3. delete `favicon.ico` in the `app` folder
4. clear the styles in `app\globals.css`
5. set the metadata in `app\layout.tsx`
6. in `app\page.tsx`, delete everything with the `return` of this page, and instead set some basic markup & Tailwind CSS classes
7. install `Tailwind CSS IntelliSense` & `ES7+`
8. customize your Tailwing CSS config by reffering your Figma design https://resource.jsmastery.pro/minimal-portfolio
9. in `tailwind.config.ts`, add your first custom color by extending your actual theme
10. go back to `app\page.tsx` & refer to that customized color
