## Build the book's HTML

You can build the HTML for your book by running the following command:

```bash
jupyter-book build observational_astronomy/
```

This will generate a fully-functioning HTML site using a **static site generator**.
The site will be placed in the `_build/html` folder, something like this:

```bash
observational_astronomy
 └──_build
    └── html
       ├── _images
       ├── _static
       ├── index.html
       ├── intro.html
       ...
```

## Publish the book to gh-pages

1. Install `ghp-import`

   ```bash
   conda install -c conda-forge ghp-import
   ```

2. Update the settings for your GitHub pages site:

    a. Use the `gh-pages` branch to host your website.

    b. Choose root directory `/` if you're building the book in it's own repository.
       Choose `/docs` directory if you're building documentation with jupyter-book.

3. From the `main` branch of your book's root directory (which should contain the `_build/html` folder) call `ghp-import` and point it to your HTML files, like so:

   ```bash
   ghp-import -n -p -f _build/html
   ```

Make sure that you included the `-n` - this tells GitHub *not* to build your book with Jekyll. Use `-p` to push the changes and `-f` to force.

## View the Book

https://westminster-astronomical-society.github.io/observational_astronomy/
