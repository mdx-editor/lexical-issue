This is a [Next.js](https://nextjs.org/) template to use when reporting a [bug in the Next.js repository](https://github.com/vercel/next.js/issues) with the `app/` directory.

# What's the problem?

**Only in dev mode** Lexical `registerUpdateListener` with Next.js 14.2.0 works differently than with Next.js 14.1.1. 

In production mode, both versions work as expected.

To reproduce, run the project and open the console. You will see:

```
binding counter 0
binding counter 1
Update listener from instance 0
```
Typing in the editor triggers updates from instance 0.

If you run 

```
npm i next@14.1.1
```

And run the project again, you will see:

```
binding counter 0
binding counter 1
Update listener from instance 1
```
Typing in the editor triggers updates from instance 1.
