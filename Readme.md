> # NEXT-JS
![NextJS](./nextjs.jpg)

### 📚 Recommended Resources

* 🔗 [Next.js Official Docs](https://nextjs.org/docs)
* 🔗 [Learn Next.js by Vercel](https://nextjs.org/learn)
* 📹 [Next.js Full Course (freeCodeCamp)](https://www.youtube.com/watch?v=1WmNXEVia8I)


## ✅ Why **Next.js** is a Powerful Extension of **React**

Think of **React** as the engine that powers your car (it helps you build UI components).
But **Next.js** is the **fully assembled car** — ready to drive, complete with a body, seats, wheels, navigation system, and much more.

Next.js **extends** React by solving the **real-world problems** developers face when building production-grade web apps with React alone.

---

### 🔍 React Alone: What’s Missing?

React is powerful, but it only helps with:

* Component-based UI building (JSX)
* Declarative state and props handling
* Client-side rendering (CSR)

But when you're making a **full-fledged application**, you face questions like:

| Problem                | React Alone                                  |
| ---------------------- | -------------------------------------------- |
| Routing                | You need `react-router-dom` manually         |
| SEO                    | Poor (CSR only; no meta tags in HTML source) |
| Performance            | Slow initial load for large apps             |
| Code Splitting         | Needs manual configuration                   |
| Server-side rendering  | Not built-in                                 |
| File structure/routing | You must design from scratch                 |
| Image optimization     | You manage yourself                          |
| API building           | You need to set up Express or something else |

---

### 🚀 What Next.js Adds to React (Why It's Powerful)

| Feature                                   | Benefit                                                                     |
| ----------------------------------------- | --------------------------------------------------------------------------- |
| **File-based routing**                    | No need for `react-router-dom`. Just add files to `/pages` or `/app` folder |
| **Server-side rendering (SSR)**           | Renders pages on the server for better performance and SEO                  |
| **Static Site Generation (SSG)**          | Pre-build pages for ultra-fast performance (great for blogs/docs)           |
| **Incremental Static Regeneration (ISR)** | Rebuild static pages in the background without full redeploy                |
| **API routes**                            | Backend and frontend in one codebase — define APIs inside the app           |
| **Image optimization**                    | Built-in with `next/image` for lazy loading, resizing, etc.                 |
| **Metadata and SEO**                      | Set `<head>` tags easily for better search engine optimization              |
| **Built-in CSS support**                  | Includes CSS Modules and support for Sass, Tailwind, etc.                   |
| **Fast Refresh & Auto Code Splitting**    | Improves developer experience                                               |
| **App Router**                            | A new layout and routing system introduced in Next.js 13+                   |
| **Ready for deployment**                  | Deploy easily on platforms like Vercel with built-in optimizations          |

---

### 💡 In Simple Terms:

> **React** is great for building UIs.
> **Next.js** is great for building **entire applications** using those UIs.

With Next.js, you can:

* Build frontend AND backend in the same project
* Serve SEO-optimized pages
* Control when and how pages are rendered (static/SSR)
* Enjoy performance boosts and developer tools out of the box

---

### 📘 Real-World Example

Let’s say you're building an **e-commerce site**:

| Feature                        | Without Next.js              | With Next.js               |
| ------------------------------ | ---------------------------- | -------------------------- |
| Homepage loads after JS bundle | ✅ CSR only                   | ✅ Can do SSG/SSR           |
| Product detail pages           | Needs router setup           | File = route               |
| SEO & social sharing           | Poor without SSR             | Meta tags pre-rendered     |
| Admin dashboard API            | Needs Express setup          | Built-in with `pages/api`  |
| Image optimization             | Manual (e.g., Cloudinary)    | Built-in with `next/image` |
| Deployment                     | Manual config (e.g., Docker) | Vercel-ready               |

---

### 📌 Summary: Why Next.js is Powerful

✅ Extends React with built-in solutions
✅ Makes SEO, performance, and routing simple
✅ Unifies frontend + backend
✅ Perfect for static sites, dynamic apps, and everything in between

---

# Next.js Overview and Prerequisites

**Next.js** is a React-based framework for building full-stack web apps.  It adds powerful features (file-based routing, hybrid rendering, optimized bundling) on top of React so you can focus on building your app.  Under the hood it configures tools for you (webpack, Babel, etc.) so you spend less time on setup.  By using Next.js, your React app can pre-render pages on the server or at build time, which makes it faster and SEO-friendly.

* **Key features:** File-system routing (each file in `pages/` is a route); built-in data fetching methods; hybrid rendering (Static Generation and Server-Side Rendering); optimized code-splitting, images and font handling; and easy deployment. Next.js even handles things like development/production differences and supports hot-reloading (Fast Refresh) out of the box.
* **Why use Next.js?** It lets you choose per-page whether to pre-render content at build time (Static Generation) or on each request (SSR). Static Generation (pre-render at build time) makes pages load very fast and can be served from a CDN. SSR (Server-Side Rendering) regenerates a page on every request, which is useful for dynamic or user-specific content. You can even mix these strategies in one app. In short, Next.js gives you the power and flexibility of React plus production-ready features like routing and server-side logic.

**Prerequisites:** You should already know basic HTML, CSS and React (components, JSX).  Knowledge of JavaScript (ES6+) and the Node.js/npm ecosystem is important since Next.js runs on Node.  (If you need a React refresher, see the official [React tutorial](https://react.dev/learn/).)  With those in hand, you can follow the steps below to start a Next.js project.

Absolutely! Below is a **detailed and well-structured note** on **Project Setup and Configuration in Next.js**, suitable for your Next.js Unit-1 or Day 1 class lecture. It includes key concepts, clear explanations, and real-world context — ideal for your notes or to deliver to students.

---

# 📘 Unit 1: Project Setup and Configuration in Next.js

---

## 🔹 1. Creating a New Next.js App

To get started with Next.js, you use the **official scaffolding tool**: `create-next-app`. This command creates a new Next.js project with all configurations pre-built for you.

### ✅ A. Prerequisites

Make sure you have:

* Node.js **v18 or higher**
* npm or yarn installed
  Check versions:

```bash
node -v
npm -v
```

---

### ✅ B. Creating the App

```bash
npx create-next-app@latest my-next-app
```

> Replace `my-next-app` with your project name.

You’ll be asked a few prompts:

* Would you like to use TypeScript? → **No** (for now)
* Would you like to use ESLint? → Yes (recommended)
* Would you like to use Tailwind CSS? → Optional (can be skipped or added later)
* Would you like to use `src/` directory? → Optional
* Would you like to use App Router? → Yes ✅ (since App Router is now the default in Next.js 14)

Once complete, it creates the project folder and installs all dependencies.

---

### ✅ C. Running the App

```bash
cd my-next-app
npm run dev
```

The development server will start at:
👉 `http://localhost:3000`

You now have a fully functional Next.js development environment. 🎉

---

## 🔹 2. Project Structure Overview

Here’s what you’ll see inside the created project:

```
my-next-app/
├── app/                  # App Router directory (used instead of 'pages/')
│   ├── layout.js         # Root layout (applied globally)
│   └── page.js           # Home page route
├── public/               # Static files (images, icons, etc.)
├── styles/               # Global styles (CSS/SCSS)
├── .env.local            # Environment variables
├── .gitignore            # Ignored files/folders for Git
├── jsconfig.json         # JS path aliases and IntelliSense
├── next.config.js        # Next.js config options
├── package.json          # Dependencies and scripts
└── README.md
```

Let’s go through some of the key folders and files.

---

### ✅ A. `app/` Directory (New App Router)

This replaces the older `pages/` directory (from Next.js 13+). It follows **file-based routing** with a component tree approach.

**Important Files**:

* `layout.js` → Global wrapper for all pages (can include headers, footers, etc.)
* `page.js` → This is the route for `/`

You can create nested folders to define routes and layouts.

Example:

```
app/
├── about/
│   ├── page.js     # /about
│   └── layout.js   # Layout for only /about route
```

---

### ✅ B. `public/` Folder

* Use this to store static files like:

  * `favicon.ico`
  * Images (e.g., `/logo.png`)
  * Robots.txt

Files in `public/` can be accessed directly:
👉 `http://localhost:3000/logo.png`

---

### ✅ C. `styles/` Folder

Contains global CSS files (e.g., `globals.css`) and can include modular styles or Sass files.

* If using Tailwind, styles are configured here.
* You can import global styles in `app/layout.js`.

```js
import '../styles/globals.css';
```

---

## 🔹 3. Config Files in Next.js

Next.js provides several config files for environment variables, settings, and path aliases.

---

### ✅ A. `next.config.js`

This is the **main configuration file** for customizing your Next.js app.

```js
/** @type {import('next').NextConfig} */
const nextConfig = {
  reactStrictMode: true,
  images: {
    domains: ['images.unsplash.com'], // allow external images
  },
  redirects: async () => [
    {
      source: '/old-blog',
      destination: '/blog',
      permanent: true,
    },
  ],
};

module.exports = nextConfig;
```

**Common use cases**:

* Enabling image domains
* Custom headers and redirects
* Enabling experimental features
* Configuring base paths for deployments

📘 [Official Docs on `next.config.js`](https://nextjs.org/docs/app/building-your-application/configuring/next-config-js)

---

### ✅ B. `.env.local`

Used to store **environment variables**, like API keys, database credentials, etc.

Create this file in the root of your project:

```
.env.local
```

Add your variables:

```
NEXT_PUBLIC_API_URL=https://api.example.com
PRIVATE_DB_PASSWORD=12345
```

* Prefix `NEXT_PUBLIC_` for client-accessible variables.
* Keep sensitive values (like DB credentials) without the prefix (used only on server).

Access variables in your code:

```js
const apiUrl = process.env.NEXT_PUBLIC_API_URL;
```

✅ `.env.local` is ignored by Git by default.

---

### ✅ C. `jsconfig.json`

Used for **path aliases** and **intelligent autocompletion** in JavaScript projects.

Default content:

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./app"]
    }
  }
}
```

With this, instead of:

```js
import Header from '../../components/Header';
```

You can do:

```js
import Header from '@/components/Header';
```

Helps reduce messy relative paths and improves DX (Developer Experience).

📘 [Docs on Path Aliases](https://nextjs.org/docs/advanced-features/module-path-aliases)

---

## 🧠 Recap & Best Practices

| Task                        | File/Folder      |
| --------------------------- | ---------------- |
| Configure routing & layouts | `app/`           |
| Serve static files          | `public/`        |
| Define global styles        | `styles/`        |
| Add environment variables   | `.env.local`     |
| Configure Next.js behavior  | `next.config.js` |
| Use clean import paths      | `jsconfig.json`  |

---

## Setting Up Your First Next.js App

1. **Install Node.js (v18+).** Next.js requires Node.js version 18 or higher.  If you don’t have it, download it from [nodejs.org](https://nodejs.org/).
2. **Create a Next.js project.** In your terminal, navigate to the folder where you want the project and run:

   ```bash
   npx create-next-app@latest my-next-app
   ```

   This `create-next-app` command bootstraps a new Next.js app (using the latest Next.js version).  You can give your project any name (`my-next-app` above).  It will ask a few questions (e.g. if you want TypeScript; since we’re focusing on JavaScript, you can skip that).  The tool sets up a folder (`my-next-app`) with the default template.
3. **Run the development server.** After creation, change into the project directory and start the dev server:

   ```bash
   cd my-next-app
   npm run dev
   ```

   This launches the Next.js development server on `http://localhost:3000`.  Open that URL in your browser: you should see the default Next.js welcome page. You now have a working Next.js environment.

**Project structure:** By default, Next.js creates a few folders/files:

* `pages/`: This is where you put React components for each page/route of your site. For example, `pages/index.js` will be the homepage (`/`), and `pages/about.js` would serve `/about`.
* `public/`: Static assets (images, etc.) live here.
* `styles/`: CSS or module files for styling (though you can use any CSS-in-JS or framework you like).
* `package.json`, `next.config.js` etc.: Standard Node project files.

You can open the project in your editor and explore. In `pages/index.js` you’ll see a default page component. You can edit it and see changes live.




---
## 🔹 1. Fundamentals of Web Rendering

Before diving into Next.js, we need to understand the different ways a web page can be **rendered** and delivered to a user.

---

### ✅ A. **CSR (Client-Side Rendering)**

**Definition**:
In **Client-Side Rendering**, the server sends a **basic HTML file** with a JavaScript bundle. The actual rendering of content happens **in the browser**, after downloading and executing JavaScript.

**How it works**:

* Browser requests page → server sends `index.html` + JavaScript
* JS downloads → React (or other library) renders the UI in the browser
* Until JS loads, user may see a blank screen

**Example**:
Traditional React apps created with **CRA (Create React App)** use CSR.

**Pros**:

* Fast client-side navigation (once loaded)
* Great for building single-page apps (SPAs)

**Cons**:

* Poor SEO (no content in HTML)
* Slow initial load (especially on low-end devices)
* Heavily reliant on JavaScript

---

### ✅ B. **SSR (Server-Side Rendering)**

**Definition**:
In **Server-Side Rendering**, the server renders the HTML **for every request** and sends the fully-formed HTML to the client.

**How it works**:

* Browser sends a request → server fetches data → renders HTML → sends it
* Browser displays content immediately
* JS hydrates the page (makes it interactive)

**Example**:
Next.js uses `getServerSideProps()` for SSR.

**Pros**:

* Great SEO (HTML is ready)
* Faster First Contentful Paint (FCP)
* Useful for dynamic, user-specific content

**Cons**:

* Slower on high-traffic pages (server renders each request)
* Increased server load
* Not suitable for content that rarely changes

---

### ✅ C. **SSG (Static Site Generation)**

**Definition**:
In **Static Site Generation**, the HTML is generated **at build time** and served as a static file for all users.

**How it works**:

* During deployment, the app is built
* HTML is pre-generated and stored on CDN
* Served instantly on request

**Example**:
Next.js uses `getStaticProps()` for SSG.

**Pros**:

* Blazing fast performance
* Scalable (no server computation per request)
* Great SEO (HTML is ready)

**Cons**:

* Content can become outdated unless rebuilt
* Not ideal for user-specific or frequently changing data

---

### ✅ D. **ISR (Incremental Static Regeneration)**

**Definition**:
ISR allows pages to be **updated after deployment** — you get the performance of SSG with the flexibility of SSR.

**How it works**:

* HTML is built at runtime **after** a certain interval (`revalidate` time)
* Old page serves until the new one is ready

**Example**:

```js
export async function getStaticProps() {
  return {
    props: { ... },
    revalidate: 10, // seconds
  };
}
```

**Pros**:

* Fast like SSG
* Pages update automatically in background
* No full rebuild needed

**Cons**:

* Slightly more complex to understand
* First user after expiration may trigger delay

---

### 🔍 Comparison Table

| Feature           | CSR  | SSR  | SSG  | ISR         |
| ----------------- | ---- | ---- | ---- | ----------- |
| SEO-Friendly      | ❌    | ✅    | ✅    | ✅           |
| Fast Initial Load | ❌    | ✅    | ✅    | ✅           |
| Dynamic Data      | ✅    | ✅    | ❌    | ✅ (limited) |
| Server Load       | ❌    | High | Low  | Low         |
| Build Time        | Fast | None | High | Medium      |

---

## 🔹 2. Benefits of SSR / SSG Over CRA

| Feature            | CRA                       | SSR / SSG (Next.js) |
| ------------------ | ------------------------- | ------------------- |
| SEO                | ❌ Poor                    | ✅ Excellent         |
| Load Performance   | ❌ Slower                  | ✅ Faster            |
| Pre-rendering      | ❌ No                      | ✅ Yes               |
| Image Optimization | ❌ Manual                  | ✅ Built-in          |
| Routing            | ❌ Manual                  | ✅ File-based        |
| Server Rendering   | ❌ Not possible            | ✅ Built-in          |
| API Routes         | ❌ External backend needed | ✅ Built-in API      |

SSR/SSG lets your app be **discoverable by search engines**, load **faster**, and offer a **smoother UX**, especially for users on slower devices or poor networks.

---

## 🔹 3. SEO, Performance, and UX Considerations

### ✅ A. **SEO (Search Engine Optimization)**

* In CSR (CRA), search engines see a **blank HTML**
* In SSR/SSG (Next.js), search engines see **pre-rendered content**
* Next.js lets you control meta tags (`<title>`, `<meta>`) per page using `head` or `metadata`

### ✅ B. **Performance**

* SSG is the **fastest** (pre-built, cached pages)
* SSR is fast but can be slower on repeated server hits
* ISR is a smart middle ground: **dynamic + cached**

### ✅ C. **UX (User Experience)**

* Faster load = better UX
* Pre-rendered content reduces “white screen” issues
* Seamless navigation with `<Link>` in Next.js gives SPA-like experience

---

## 🔹 4. When to Choose Next.js for a Project

### ✅ Use Next.js when:

* You need **SEO optimization** (e.g., blogs, portfolios, marketing)
* You want **faster performance** (pre-rendered pages)
* You're building a **multi-page application**
* You want to **avoid boilerplate setup**
* You need both frontend + backend in one project
* You plan to deploy to **Vercel** or any serverless platform

### ❌ Avoid Next.js when:

* You're building a **simple SPA** with no need for SSR/SSG
* You want **maximum control** over your bundler and tooling
* Your app is **purely backend** (Next is frontend-first)

---


## Pages and File-based Routing

Next.js uses **file-based routing**. Each file you put under the `pages/` directory becomes a route in your app:

* `pages/index.js` → route `/` (the homepage).
* `pages/about.js` → route `/about`.
* `pages/blog/hello.js` → route `/blog/hello`.
* **Index routes:** Any `index.js` in a folder maps to the folder’s root. E.g. `pages/blog/index.js` maps to `/blog`.
* **Dynamic routes:** You can create dynamic URL parameters by bracket syntax. For example, a file named `pages/posts/[id].js` will match `/posts/1`, `/posts/hello-world`, etc. (You use `getStaticPaths` with this for static generation; we’ll cover dynamic routing later.).

**Example:** Suppose we create `pages/about.js`:

```js
// pages/about.js
export default function About() {
  return <h1>About Us</h1>;
}
```

When running the app, navigating to `http://localhost:3000/about` shows “About Us”.  The name of the file (without extension) defines the route path.

**Layouts:** If you have a common layout (header/footer) across pages, you can create a custom `<App>` in `pages/_app.js` that wraps every page. For instance:

```js
// pages/_app.js
import Layout from '../components/Layout';
export default function MyApp({ Component, pageProps }) {
  return (
    <Layout>
      <Component {...pageProps} />
    </Layout>
  );
}
```

This wraps every page with `<Layout>`. We won’t dive into layouts deeply right now, but know that `_app.js` is where app-wide wrappers belong. (For now, focus on individual pages and routing.)

## Client-Side Navigation with Link

Next.js provides a built-in `<Link>` component for navigation. Unlike a normal `<a>` tag, `<Link>` performs **client-side transitions** between pages (no full page reload). This makes navigation fast and feels like a single-page app.

&#x20;*Figure: Example of navigating between pages with `<Link>` (the **Link** component lets you click through pages without a full reload).*

To use `<Link>`, import it from `next/link` and set its `href` to the path you want:

```js
import Link from 'next/link';

export default function HomePage() {
  return (
    <div>
      <h1>Welcome!</h1>
      <Link href="/about">Go to About page</Link>
    </div>
  );
}
```

Here, clicking “Go to About page” will take you to `/about`. Under the hood, Next.js preloads linked pages for an ultra-fast transition. You can nest any elements inside `<Link>`; e.g. `<Link href="/posts/first-post">First Post</Link>`. (In Next.js 12.2 and later, you no longer need to put an `<a>` tag inside `<Link>` – you can have it wrap text or elements directly.)

Example from the docs:

```js
// pages/posts/first-post.js
import Link from 'next/link';

export default function FirstPost() {
  return (
    <>
      <h1>First Post</h1>
      <p>This is my first post.</p>
      <Link href="/">← Back to home</Link>
    </>
  );
}
```

In this code, the `<Link href="/">` navigates back to the home page. When building your app, add such links between pages to allow easy navigation. The Next.js Link component ensures pages load without a full refresh.

## Data Fetching: Static Generation vs Server-Side Rendering

A core feature of Next.js is **pre-rendering** pages to HTML before serving them, which improves performance and SEO. You can choose between:

* **Static Generation (SSG):** The page HTML is generated *at build time*. Next.js runs your code once when you build, fetches any data, and produces a static HTML file. That file is reused for every request. This is extremely fast (served by CDN). It’s ideal for content that doesn’t change on every request (e.g. blog posts, marketing pages). If the page needs data, you use `getStaticProps()` in your page component.
* **Server-Side Rendering (SSR):** The page HTML is generated *on each request*. Next.js runs your code on the server every time someone hits that URL. This ensures data is always fresh (great for user-specific or frequently updated data). The trade-off is each request takes longer (slightly slower TTFB) since the page is rendered on the fly. For SSR, you export `getServerSideProps()` from your page.

> **“Next.js has two forms of pre-rendering: Static Generation and Server-side Rendering. The difference is in when it generates the HTML.”**. Static Generation creates the HTML at **build time**, while SSR does it **on each request**. Next.js lets you choose per-page which method to use (you can even mix them in one app).

**Static Generation example:** In a page file (e.g. `pages/index.js`), you can export an async function `getStaticProps`. This function runs at *build time* and returns data as props to your page component. For example:

```js
export default function HomePage({ posts }) {
  return (
    <ul>
      {posts.map(post => (
        <li key={post.id}>{post.title}</li>
      ))}
    </ul>
  );
}

export async function getStaticProps() {
  // This code runs at build time on the server
  const posts = [
    { id: 'post1', title: 'My First Post' },
    { id: 'post2', title: 'Another Post' },
  ];
  return { props: { posts } };
}
```

When you build the app, Next.js calls `getStaticProps`, gets the `posts` data, and generates the HTML for `HomePage`. At runtime, it serves that pre-built HTML to every visitor. The `posts` prop is passed into the component (as indicated by `return { props: { posts } }`), and you can use it just like any React prop. The docs note: **“getStaticProps will pre-render a page at build time using the props returned from the function”**. In our example, the static HTML will list the two posts.

You can also fetch from an API or database inside `getStaticProps`, and Next.js will include that data. *Importantly*, code in `getStaticProps` runs only on the server (build server), so you can safely use Node APIs or secret keys there. (Any modules you import at top-level of the file won’t be sent to the browser.)

Next.js supports **Incremental Static Regeneration (ISR)**: you can tell Next.js to re-generate a static page periodically (with the `revalidate` option) so your static content stays updated without a full rebuild. See [Next.js ISR docs](https://nextjs.org/docs/basic-features/data-fetching/incremental-static-regeneration) for details.

**Server-Side Rendering example:** If your page needs up-to-the-minute data (for example, user-specific content or live data), use `getServerSideProps`. For example:

```js
export default function Dashboard({ stats }) {
  return <div>Current users: {stats.users}</div>;
}

export async function getServerSideProps() {
  // Runs on every request
  const res = await fetch('https://api.example.com/stats');
  const stats = await res.json();
  return { props: { stats } };
}
```

Here, each time someone visits `/dashboard`, Next.js runs `getServerSideProps` to fetch new data and then renders the page. The data (`stats`) is passed as props to the component. The docs explain: **“getServerSideProps is a Next.js function that can be used to fetch data and render the contents of a page at request time.”**. In SSR, there is no build-time HTML – the HTML is generated on demand.

**When to use which:** Use **Static Generation** whenever possible for performance (ideal for public pages, blogs, docs). Use **Server-side Rendering** for data that changes per request or requires secrecy (like auth tokens). The Vercel blog notes: *“Static Generation is more performant… but data could become stale. You can work around this with ISR or client-side fetching”*.

## React Props and State in Next.js Components

Since Next.js pages are just React components, all the usual React principles apply. You can use **props** to pass data into components, and **state** (via `useState`) for dynamic interactivity.

* **Props:** Data returned from `getStaticProps` or `getServerSideProps` is passed into your page component as props. But even without data fetching, you can create child components and pass props down. *Props* are simply how React components receive input. As React docs say: *“React components use props to communicate with each other. Every parent component can pass some information to its child components by giving them props.”*. Think of props like function arguments. For example:

  ```js
  function Avatar({ person, size }) { … } 
  function Profile() {
    const user = { name: 'Alice', img: '...' };
    return <Avatar person={user} size={100} />;
  }
  ```

  Here `Profile` passes a `person` object and `size` number as props to `Avatar`.

* **State:** When a component needs to remember information and react to user input, you use React state. Next.js pages can use state just like any React component. The simplest way is the `useState` hook. The React docs explain: *“Components often need to change what’s on the screen as a result of an interaction… this kind of component-specific memory is called state.”*. For example, you might do:

  ```js
  import { useState } from 'react';

  export default function Counter() {
    const [count, setCount] = useState(0);
    return (
      <>
        <p>Count: {count}</p>
        <button onClick={() => setCount(count + 1)}>Increment</button>
      </>
    );
  }
  ```

  Here `count` is a state variable initialized to `0`, and `setCount` is the function that updates it. When `setCount` is called, React re-renders the component with the new count. In short, **state lets a component “remember” data between renders and update the UI when it changes**.

In a Next.js page, you can freely mix props from data fetching with local state. For example:

```js
export default function Greeting({ initialName }) {
  const [name, setName] = useState(initialName || 'Guest');
  return (
    <>
      <p>Hello, {name}!</p>
      <button onClick={() => setName('Alice')}>Set Name to Alice</button>
    </>
  );
}

// getStaticProps could provide initialName from some API:
export async function getStaticProps() {
  return { props: { initialName: 'Bob' } };
}
```

The `name` state starts as `'Bob'` (from props), and clicking the button changes it to `'Alice'`.

**Summary:** Next.js pages are normal React components, so you use props and state exactly as you would in React. Props (from parent components or from data fetching) are read-only inputs, and state (`useState`, etc.) is for interactive, changeable data inside the component.

## Building a Simple Example

To tie these concepts together, let’s sketch a simple example. Imagine a page that lists blog posts (using static generation) and links to a detail page:

1. **Create some data or markdown:** For simplicity, we’ll hardcode an array in `getStaticProps`.

2. **Index page (`pages/index.js`):** This page will list posts.

   ```js
   // pages/index.js
   import Link from 'next/link';

   export default function Home({ posts }) {
     return (
       <div>
         <h1>Blog Posts</h1>
         <ul>
           {posts.map(post => (
             <li key={post.id}>
               <Link href={`/posts/${post.id}`}>{post.title}</Link>
             </li>
           ))}
         </ul>
       </div>
     );
   }

   export async function getStaticProps() {
     // Simulate fetching or reading posts
     const posts = [
       { id: 'hello-world', title: 'Hello World' },
       { id: 'nextjs-guide', title: 'Learning Next.js' },
     ];
     return { props: { posts } };
   }
   ```

   This uses `getStaticProps` to supply a `posts` array. The component maps over `posts` and renders links to `/posts/hello-world` and `/posts/nextjs-guide`. Because of static generation, this HTML is generated at build time.

3. **Post detail page (`pages/posts/[id].js`):** A dynamic route file. You’d use `getStaticPaths` + `getStaticProps` here (beyond our Unit1 scope), but as a placeholder:

   ```js
   // pages/posts/[id].js
   import { useRouter } from 'next/router';

   export default function PostPage() {
     const router = useRouter();
     const { id } = router.query;  // e.g. 'hello-world'
     return <h1>Post: {id}</h1>;
   }
   ```

   In a full example, you’d fetch or read the post content based on `id`. For now, we demonstrate routing: clicking a link on the home page will bring you here, and `id` comes from the URL.

4. **Running it:** Start the dev server (`npm run dev`) and go to `http://localhost:3000`. You should see the list of posts with links. Clicking a link navigates to, e.g., `/posts/hello-world` (client-side via `<Link>`) and shows “Post: hello-world”.

Through this mini-app, we used **file-based routing** (`pages/index.js` and `pages/posts/[id].js`), **Link** for client navigation, **getStaticProps** for static data, and React **props** to pass data into the component. This covers the Unit1 concepts of routing, props, and basic data fetching.

## Summary of Unit1 Topics

* **Next.js 15 (Latest)** is a React framework for building performant web apps.
* **Prerequisites:** HTML, CSS, React, Node/npm.
* **Creating an App:** Use `npx create-next-app@latest` to scaffold; start with `npm run dev`.
* **Pages/Routes:** Any JS file in `pages/` is a route (file-system routing). Dynamic routes use `[param].js`.
* **Navigation:** Use `<Link href="/path">` from `next/link` for fast client-side navigation.
* **Data Fetching:** Two main modes – **Static Generation** with `getStaticProps` (build-time), and **Server-Side Rendering** with `getServerSideProps` (run on each request). Static is faster (HTML cached/CDN) but data may be stale; SSR is always fresh but slower per request.
* **Props and State:** Next pages are React components, so use props to pass data (e.g. from `getStaticProps`), and use `useState` to manage local state for interactive behavior.

**Next Steps:** In the next lectures, you’ll dive deeper into topics like dynamic routes with `getStaticPaths`, API routes, advanced data fetching (ISR, on-demand revalidation), and the newer App Router. But with this foundation you can already build basic multi-page Next.js apps that use static generation and client-side navigation.

**Resources:** See the official Next.js docs for more detail, especially **“Getting Started”** and **“Basic Features”** sections. The Learn Next.js tutorial (from Vercel) is also helpful for step-by-step chapters. The above citations are from the official docs and related guides to ensure accuracy.


1	Introduction to Modern Development Environment	8	20
	Evolution of software development tools, Overview of modern development stacks, Introduction to Operating Systems (Linux, macOS, Windows) for development, File system navigation, command line basics (CLI, terminal), Introduction to open-source development, Practical: CLI commands, directory structure, text file manipulation

2	Source Code Editors and IDEs	10	20
	Introduction to IDEs and text editors: VS Code, IntelliJ, Sublime, etc., Extensions, themes, and plugin usage, Writing, saving, running basic code snippets (Python, C, JavaScript), Code navigation, auto-complete, code formatting, Using terminal within editors, Practical: Install and configure VS Code, write and run sample scripts

3	Version Control Systems (Git & GitHub)	12	20

	Version control concepts: local vs. remote repositories, Git basics: init, clone, add, commit, push, pull, branch, merge, GitHub workflows: repositories, forks, pull requests, issues, actions, Collaboration through GitHub (teams, permissions, readme files), Resolving conflicts, .gitignore, README.md, Practical: Set up Git, GitHub account, perform end-to-end Git workflow

4	Debugging, Code Quality & Automation Tools	10	20
	Importance of debugging and error handling, Debugging tools in VS Code and browser dev tools, Introduction to linters (ESLint, Pylint), formatters (Prettier, Black), Basic task runners: npm scripts, Python virtual environments, Shell scripting introduction (bash scripts for automation), Practical: Debug code using breakpoints, configure ESLint and Prettier
5	CI/CD and DevOps Essentials (Beginner Level)	15	20
	Overview of CI/CD pipelines, Basics of GitHub Actions and Jenkins, Writing basic `.yaml` workflows for CI, Introduction to Docker and container concepts, Deployment concepts (staging, production), intro to Netlify/Vercel, Practical: Implement a GitHub Action to auto-check and deploy a small project
