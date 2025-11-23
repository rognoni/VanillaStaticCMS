# Content management system, made in Vanilla <del>PHP</del>

If you want to rebuild the web from the ground up, without dependencies, this is the right project for you:

- inspired by [VanillaCMS](https://github.com/rognoni/vanillacms) (PHP)
- made in [Vanilla JS](http://vanilla-js.com)
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
