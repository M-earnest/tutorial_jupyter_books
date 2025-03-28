# Adding Citations and Bibliographies

If you want to include citations in your course website, you first need to create a BibTeX file to store the citation information. Then, you must edit the `_config.yml` file to ensure that the citations are displayed according to your preferences. 

## Create a Bibliography

Create a new file in your repository and save it with the `.bib` extension to create a BibTeX file. 

![Image of how to name the bibtex file](../../static/bib-file-name.jpg)

Then, add your references to the file and click on "commit changes".

![Image of the newly created bibtex file with one example reference.](../../static/bib-file.png)


## Edit the Config File
There are several inline style options available for your citations (see [here](https://sphinxcontrib-bibtex.readthedocs.io/en/latest/usage.html#referencing-style) for more details). We recommend adjusting the reference style in your `_config.yml` file by adding "bibtex_reference_style: author_year" right under "sphinx: config:". Please ensure the correct indentation.

![Image of the config.yml file, in which the reference style is included as described.](../../static/config_bibtex.png)

This will ensure that author and year are displayed correctly.

## Add a Citation
Now, you can include your citations into your text. Here is an example:

```
{cite}`munafo2017manifesto`
```

Result:
{cite}`munafo2017manifesto`

## Add a Bibliography 


----
**References**

```{bibliography}
:filter: docname in docnames
```

