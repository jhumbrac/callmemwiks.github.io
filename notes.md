## Oh hayy

Okay so I don't know what your teacher is talmbout. Your code isn't _terrible_, it's pretty solid, just a few things to note:

### DOM life

Every html file has the following structure, also called the DOM (Document Object Model):


    ```<!DOCTYPE html>
    <html>
    <head>
    <!-- All the meta data -->
      <title></title>
    <!-- Path to the CSS  -->
      <link rel="stylesheet" type="text/css" href="">
    </head>
    <body>
    <!-- All the site's visible content -->
    </body>
    </html>
    ```

I noticed some divs in the `<head>`, and these which won't be shown / will mess up the structure of the DOM.

Also for easier editing and spotting of errors, just be aware of indentation. It'll keep the code clean, and organized, and it won't be as annoying to check for tags that weren't closed, and so on.


### CSS

- Some divs weren't given any [specifity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity), which would make it easier to style the document. For instance instead of `<h3 class="about"></h3>` you could do `<div class="about"> <h3></h3> </div>`.
Same for classes and IDs (I left a real long comment in the CSS), but giving IDs instead of classes is usually frowned upon because they make styling real difficult. A style on an ID will overpower the style on a class, so that could break shit and be annoying to fix if you have a _super_ long stylesheet.

- Beware of repeating the styles, or adding the same style with different values twice (more notes in the CSS) but Cascading Style Sheets are read top to bottom, and will only use the latest style. So if you style something up top a certain way, but then restyle it by accident below, it will disregard the first element and take the last.

- Try to group similarly looking things as best as you can. You could do that by giving the same class to the elements, or you could use [semantic tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) and bypass giving classes altogether.
On the same note, if you style a parent element like `body`, `html`, `div`, etc... these styles will be applied to all the children elements within them. So in one of the css file, there was a `color` set on the `body` element, that was repeated throughout the file. No need for the repeating, setting it on the `body` is all that was needed, and is real clever!

- For background images, always find the path to the image from the stylesheet.

- Hexcodes instead of color names


I think that's all? But overall good job!! :rainbow: