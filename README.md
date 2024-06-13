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

## 1. Hero Section

Build a top title, a primary title, a subtitle & the call to action button to show your work

1. in the root of your directory, create a new folder called `components`
2. within this folder, create a new file called `Hero.tsx`
3. in this file, type `rafce` to quickly create a `Home()` component function (feature from `ES7+ React/Redux/React-Native snippets`)
4. in `app\page.tsx`, output the `<Hero />` component imported from `components\Hero.tsx`
5. back to `components\Hero.tsx`, set some classes to the `<div>`
6. inside that `<div>` create another `<div>` acting as a wrapper for your first components coming from Aceternity to add the spotlight effects available in your Figma design in desktop version
7. here are examples on how to use a nice search feature to find exactly what you're looking for quickly:
   1. Aceternity:
   - go to https://ui.aceternity.com/ & press `Ctrl + K` to open up a search no matter where on the page you are
   - search for `spotlight` & press `Enter`
   - you'll get redirected to https://ui.aceternity.com/components/spotlight
   2. NextJS:
   - go to https://nextjs.org/docs & press `Ctlr + K`
   - search for `server actions` & press `Enter`
   - there you are https://nextjs.org/docs/app/building-your-application/data-fetching/server-actions-and-mutations#convention
   - then press `Ctrl + F` & search for `use server`
8. so, back to Aceternity, look for `spotlight` to reach out to https://ui.aceternity.com/components/spotlight
   1. below "Install dependencies", copy `npm i framer-motion clsx tailwind-merge`
   - in your terminal, run `npm i framer-motion clsx tailwind-merge`
   2. below "Add util file", copy the code for `utils/cn.ts`
   - in the root of your project, add a new `utils` folder & add a new `cn.ts` file & in there paste the code you copied before
   3. below "Copy the source code", copy the code for `components/ui/Spotlight.tsx`
   - inside of the `components` folder, create a new `ui` folder, inside of which you create a new file called `Spotlight.tsx` & paste what you just copied
   4. below "Copy the highlighted `spotlight` animation into `tailwind.config.js` file", copy the code
   - in `tailwind.config.js`, paste the code you just copied to override the content
   5. press `Ctrl + K` & search for `Add utilities`, you'll see that you have to add this `flattenColorPalette` in `tailwind.config.js` by overriding the code in your `tailwind.config.js`
9. since you will be continuing overriding some files, use the provided code in the open source GitHub repository
   1. `tailwind.config.ts`
   - go to https://github.com/adrianhajdin/portfolio?tab=readme-ov-file#snippets
   - then copy the code below `tailwind.config.ts`
   - override the content of your `tailwind.config.js` file with the code you just copied
   2. do the same thing for `app\globals.css`
10. install all the dependencies required in the updated `tailwind.config.ts` file, so in your terminal, run:
    - `npm install mini-svg-data-uri`
    - `npm install tailwindcss-animate`
11. use the `<Spotlight />` component within `components\Hero.tsx` inside the previously added `<div>`
12. pass some native Tailwind CSS classes to this `<Spotlight>` component & `fill="white"`
13. duplicate this component 2 more times & change their styles
14. right below the `<div>` that contains this spotlight, create another `<div>` that will act as a UI grid
    - for that, you'll use a component called "Grid and Dot Backgrounds" from https://ui.aceternity.com/components/grid-and-dot-backgrounds
    - click on `Code` to switch over the code & copy the 2 `<div>`s with the `<p>` tag in between & paste it there
    - modify a couple of classes of this code
    - use a theme provider which is a package called `next-themes` available in https://www.npmjs.com/package/next-themes to switch the background to dark
      - in your terminal, run `npm i next-themes`
      - google "next themes" & click on "Next.js - shadcn/ui" to go to https://ui.shadcn.com/docs/dark-mode/next & follow this setup
        1. like we did above, you have to "Install next-themes" by running `npm install next-themes` in your terminal
        2. Create a theme provider
        - copy the provided code
        - go to `app` & create a new file called `provider.tsx`
        - in there, paste the code you just copied
        3. Wrap your root layout
        - copy the `<ThemeProvider>` layout
        - go to `app\layout.tsx` & wrap your `{children}` with it & import `{ ThemeProvider }` from `./provider`
        - set the `defaultTheme` to `"dark"`
15. go back to `components\Hero.tsx`
    - add a new `<div>` that will wrap your heading below the `<div>` containing your grid & give it some CSS classes
    - inside of it, add an inner `<div>` with some CSS classes
    - and in it, render an `<h2>` that would say "Dynamic Web Magic with Next.js"
    - make this `<h2>` text appear over the grid by setting the grid to a position of `absolute` & less noticable by giving a background color of `dark:bg-grid-white/[0.05]`
16. below this `<h2>`, render your primary text & give it its animation
    - go back to Aceternity UI & search for `Text Generate Effect`
    - you will be redirected to https://ui.aceternity.com/components/text-generate-effect
    - Copy the source code for `components/ui/text-generate-effect.tsx`
    - inside `components\ui`, add a new file called `TextGenerateEffect.tsx` & paste in there the code you just copied
    - go back to `components\Hero.tsx` & use this `<TextGenerateEffect />` & pass to it 2 props `className` & `words`
17. below this `<TextGenerateEffect />` output a `<p>` tag to add the subtitle
18. go back to `components\ui\TextGenerateEffect.tsx`, modify some of the content
    - make the `motion.span` CSS class dynamic to turn the "Experiences" word into purple
    - a bit down, replace `mt-4` with `my-4`
    - remove the `text-2xl` CSS class to make the text in the `words` bigger
19. like in the Figma design, implement the "Show my Work" button
    1. go back to Aceternity & finc `Tailwind CSS buttons`
    2. you'll reach https://ui.aceternity.com/components/tailwindcss-buttons
    3. in there, copy the "Border Magic" button
    4. within the `ui` folder, create a new component called `MagicButton.tsx` & create a new React component with help of the `rafce` shortcut
    5. paste the code you just copied in there
    6. go to `components\Hero.tsx` & render the `<MagicButton />` component in there
    7. in `components\ui\MagicButton.tsx`, make the button more dynamic with help of props to render some dynamic content & updated some of the CSS classes
    8. go to `components\Hero.tsx` & render some props to `<MagicButton>`
       1. `title`
       2. `icon`
          - use React Icons https://react-icons.github.io/react-icons/ to render some icons by installing `react-icons` https://www.npmjs.com/package/react-icons by running `npm i react-icons` in your terminal
          - use it by setting some `FaLocationArrow` imported from `react-icons/fa6` to the `icon` prop
       3. `position` set to `right`
20. add the navigation bar
    1. go to Aceternity & find "Floating Navbar"
    2. you'll be redirected to https://ui.aceternity.com/components/floating-navbar
    3. copy the source code for `components/ui/floating-navbar.tsx`
    4. within the `ui` folder, create a new component called `FloatingNav.tsx`
    5. paste in there the code you just copied
    6. go to `app\page.tsx` & output the `<FloatingNav />` component & pass to it the `navItems` prop like it says in the docs under "Props"
