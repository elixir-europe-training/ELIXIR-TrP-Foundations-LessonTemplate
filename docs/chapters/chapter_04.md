## HTML tips and tricks related to the Lesson template

Let's explore the provided files and annotate them step by step. Open the index.html with Edit mode on Github. It has a quite simple structure: 

```
<!DOCTYPE html>
<html>
  <head>
      <script type="application/ld+json">
         insert Bioschemas annotation about course here
      </script>
  </head>
  <body>
     <h2 id="lesson-overview">Lesson overview</h2>
     ...
  </body>
</html>
```

All HTML documents must start with a <!DOCTYPE> declaration. The declaration is not an HTML tag. It is an "information" to the browser about what document type to expect.

This is an example of an HTML file with three HTML elements - `<html>`, `<head>`, and `<body>`. An HTML element is defined by a start tag, some content, and an end tag. For the outer `html` element (`html` is the tagname), the start tag is `<html>` and the end tag is `</html>`. The `/` in front of the tagname indicates an end tag. 

The `<html>` element is the root element of an HTML page. The `<head>` element contains meta information about the HTML page and the `<body>` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

### Images

  If you want to add an image, the best way would be to use html, e.g:

    ```html
    <figure>
    <img src="https://elixir-europe.org/sites/default/files/ebif_news_release_image_news_landingpageimage_.png" width="600" alt="Image on elixir landing page"/>
    <figcaption> Elixir image </figcaption>
    </figure>
    ```
    
Which would result in:

<figure>
    <img src="https://elixir-europe.org/sites/default/files/ebif_news_release_image_news_landingpageimage_.png" width="600" alt="Image on elixir landing page"/>
    <figcaption> Elixir image </figcaption>
    </figure>

 If you want to use local images, add them to `docs/assets/images` and refer to them in the html as a relative path, e.g.:

    ```html
    <figure>
    <img src="../../assets/images/elixir_image.png" width="600" alt="Image on elixir landing page"/>
    <figcaption> Elixir image </figcaption>
    </figure>
    ```

Resulting in: 

<figure>
  <img src="../../assets/images/elixir_image.png" width="600" alt="Image on elixir landing page"/>
    <figcaption> Elixir image </figcaption>
    </figure>
