Including Media

## Images
In Jupyter Books, there few different ways to include images. Here we will highlight the way that is most optimal for hosting the Book with our provided gh-actions script.

The easiest way is to add the images to your projects in the static folder of your project. Once you push/ upload the project to your GitHub you essentially are hosting the images through their services.

To add images in your Jupyter Book, use the following line of Markdown in a markdown cell:

`![alternative_imagetext](https://YOURGITHUBNAME.github.io/PROJECTNAME/_static/FILENAME.png)`

Resulting, for example, in:

![alternative_imagetext](https://felixkoerber.github.io/jb/_static/logo.png)

As you are able to use essentially any imagelink, you can add images that are hosted through other websites, too!


If you want more control about the size, orientation and more, you will have to rely on HTML tags. E.g. the following line of code will present the same image as above only downscaled to a width of 200 pixels.


`<img src="https://felixkoerber.github.io/jb/_static/logo.png" alt="logo" class="bg-primary mb-1" width="200px">
`

which results in:

<img src="https://felixkoerber.github.io/jb/_static/logo.png" alt="logo" class="bg-primary mb-1" width="200px">



</br>
</br>
</br>
</br>

**The code above is made up of multiple html keywords, that each control a separate parameter of the image you want to control:**

`<img>` is an HTML tag used to display an image on a web page.

`src="(https://YOURGITHUBNAME.github.io/PROJECTNAME/_static/FILENAME.png"` is an attribute that specifies the URL or path to the image file you want to display. In this case, it points to an image file on GitHub with a specific URL that you will need to replace with your own GitHub account name, project name, and file name.

`alt="alternative_imagetext"` is an attribute that provides alternative text for the image. This text is used by screen readers for visually impaired users, and it is also displayed when the image cannot be loaded for some reason.

`class="bg-primary mb-1"` is an attribute that defines the CSS class or classes to apply to the image. In this case, the class bg-primary sets the background color of the image to a primary color, and mb-1 adds a margin-bottom of 1 unit to the image.

`width="200px"` is an attribute that sets the width of the image to 200 pixels. This can be adjusted to suit your needs.

Simply copy-paste the above line of code and adjust it to your need as necessary to emebdd every kind of image into your notebooks.

**For a more in-depth exploration of the `img` tag checkout the [w3schools html tutorial](https://www.w3schools.com/html/html_images.asp)**


## Videos, Presentations, GIFs, and more: iframes

Jupyter Book enables you to implement `html` into your books, which allows for the integration of almost every type of media, including - but not limited to - `Videos, Presentations, GIFs, Maps` and `Images` via `iframes`.

```{note}
`iframes` or *inlineframes* are HTML-elements, that can be used to embed content from different websites.
```

Inlineframes are structured and implemented like this:

`<iframe src="http://www.example.com/" height="100" width="200" name="iframename">Alternative title</iframe>`

Thus, they essentially follow the same structure as the HTML-image integration.

To quickly generate this code for the media of your choice, you can use a tool like the [iframe-generator](https://www.iframe-generator.com/), where you add the media URL, can change various settings and can then generate the iframe code.

Let us go over different types of media embeddings:

___


## Google Slides

To embed Google Slides in Jupyter Book, you can use an HTML iframe. Here's how:

* Go to your Google Slides presentation and click on the "File" button in the top-left corner of the screen.

* Click on "share" and select "Publish to the web"

* Select "Embed" and click "Publish"

* Open your Jupyter Book and create a new Markdown cell where you want to embed the Google Slides presentation.

* In the Markdown cell, copy the HTML-code, which could result in something like this:

```
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTJvUAN-dg7r7Dbj-KpxcNO6ssd7akDQjBbHzhTTBBU7zSBZ4sTfjYPtHZL6V7GmM0VQvo6Aviu5oSG/embed?start=false&loop=false&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
```

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTJvUAN-dg7r7Dbj-KpxcNO6ssd7akDQjBbHzhTTBBU7zSBZ4sTfjYPtHZL6V7GmM0VQvo6Aviu5oSG/embed?start=false&loop=false&delayms=10000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

Note that the width and height of the iframe can be adjusted to fit your specific use case. You may also want to adjust the styling of the iframe to match your Jupyter Book's visual design better.

### Videos

To add videos, you need to add the "embed"-URL of the video. 
This URL is formatted like this:
`http://www.youtube.com/embed/VIDEO_ID`

Thus, `https://www.youtube.com/watch?v=c-bemNZ-IqA` would become `https://www.youtube.com/embed/c-bemNZ-IqA`.

Added in iframes, it looks like this:

```<iframe src="https://www.youtube.com/embed/c-bemNZ-IqA" style="border:0px #ffffff none;" name="Open Science Video" scrolling="no" frameborder="1" marginheight="0px" marginwidth="0px" height="400px" width="600px" allowfullscreen></iframe>```

Turning into:
<iframe src="https://www.youtube.com/embed/c-bemNZ-IqA" style="border:0px #ffffff none;" name="Open Science Video" scrolling="no" frameborder="1" marginheight="0px" marginwidth="0px" height="400px" width="600px" allowfullscreen></iframe>



### GIFs

To implement GIFs in Jupyter Books, you can also use HTML to embed a GIF in Jupyter Books. Here's an example:

`<iframe src="link/to/your/gif/file.gif" width="240" height="200" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>'`

Again, replace "link/to/your/gif/file.gif" with the URL or file path to your GIF.

This could result in:

<iframe src="https://giphy.com/embed/l5s71uAp3CzKwxwkoZ" width="240" height="200" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

```{note}
Note that if you're using a local file path, the path should be relative to the location of the notebook or Markdown file that you're embedding the GIF in. If you're using a URL, it should be a direct link to the GIF file.
```

___

There are plenty of other datatypes you can add! This section is only a short introduction to the embedding of media.

## Next section:

[Structuring content](./tutorialcontent/structure)

How do we structure our course website?
