# Content management system, made in Vanilla <del>PHP</del>

Introducing **Vanilla(static)CMS** a lightweight and minimalistic Content Management System built with Vanilla JavaScript and Markdown. Designed for simplicity and ease of use, this CMS empowers users to manage content effortlessly, focusing on a clean and streamlined user experience:

- inspired by [VanillaCMS](https://github.com/rognoni/vanillacms) (PHP)
- built with [Vanilla JS](http://vanilla-js.com) and [Markdown](https://en.wikipedia.org/wiki/Markdown)
- front-end with [Pico CSS](https://picocss.com), [Marked](https://marked.js.org)

This is the core idea:

```
window.addEventListener("load", async (event) => {
    const params = new URLSearchParams(document.location.search)
    const filepath = params.get("c") ?? "index.md"
    const filefetch = await fetch(filepath, {method: "GET", cache: "no-store"})
    const markdown = await filefetch.text()
    document.getElementById("content").innerHTML = marked.parse(markdown)
})
```
