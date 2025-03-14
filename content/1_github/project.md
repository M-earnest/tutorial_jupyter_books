# Setting Up a Repository on GitHub

In this section, you'll first learn how to start a new project on GitHub, followed by a step-by-step guide on how to use the free course template for your own course. By using our course template instead of starting a completely new project, you can take advantage of the existing structure and only need to customize and add individual pages to fit your content.

## Create a New Repository
Now, let's put that new account to use by creating an online repository — often called a "remote repo"!

1. Open Github in your browser

2. Click on the `+` sign in the top right corner and click "New repository"

3. Fill out the repository details: Give your repository a name, description, and check the box next to "public" to make sure others can find your directory. 

This could look something like this:

<img src="https://diler-digitell.github.io/Jupyter-Book/main/static/new_repo_example.png?raw=true" alt="depicting an example of a new repository" class="bg-primary" width="500px">

4. Check the box "Add a README file", this will initiate your repository with a file that can later be used to display basic information to others viewing your repo.

5. Choose a license! You can start out with "None" as this repo is just for testing, but if you plan to use Github for your projects it's imperative to include one to prevent misuse.

6. Click the "Create repository" button to create your new repository.

7. Now you can add files to your repository by clicking the "Add file" button by either uploading them or creating a new file.

Congratulations! You are now the proud owner of a GitHub repository. 


## Working With the Course Template

To work with our materials, you need to "fork" (i.e., copy) the course template repository to your account:

### 1. Fork the Course Template

Head over to the [course template repo](https://github.com/DiLER-Digitell/Course-template), and on the upper right-hand side, click "fork". 

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/fork_button.png?raw=true" alt="depicting position a look of the fork button on a GitHub repository" class="bg-primary" width="500px">

You'll be asked to create a new fork; simply add a new repository name, provide a short description, or keep the existing one, check the box "Copy the main branch only," and click the "create fork" button.

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/create_fork.png?raw=true" alt=" depicting position a look of the fork button on a GitHub repository" class="bg-primary" width="500px">

Now you created your own course repository!

### 2. Getting Familiar with the Structure and Existing Files

**The course template is structured in the following way**

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/repo.png?raw=true" alt="depicting the contents of the course template repository on GitHub" class="bg-primary" width="500px">


Where:

- **.github/workflows folder**: contains the prewritten scripts to automatically create your website every time new content is pushed online.

- **lecture**: contains all our content files and directories, as well as the "toc.yml" and the "config.yml" files, which define the structure and functionality of the website.

- **README**: a short explanation of your website/course.

- **LICENSE**: self-explanatory, stating who and how people are allowed to use or reproduce the content of this repo.

- **requirements.txt**: contains the necessary requirements for the automatic scripts building the website to run; there is no need to change anything here.

Now, most the things that you'll be adapting are contained in the content folder "lecture", which looks like this.

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/lecture_folder.png?raw=true" alt="depicting the contents of the course template repository on GitHub" class="bg-primary" width="500px">

Where:

- **content**: Contains files making up the main content of a course website.

- **general information**: Contains files providing information, such as the necessary setup, the outline of the course, a code of conduct, etc. The included \"index.md" file will be the landing point of the course website.

- **introduction**: Contains files making up the introductory sessions of a course.

- **static**: Contains all the pictures and graphs contained in a course. It's recommended that should you add new files. e.g., a course logo to this folder.

- **config.yml**: Contains the course title, authors, and copyright notice at the footer of the website, which you should change before hosting your website. Further, it contains the specifics for the technical implementations of a course, e.g., whether Jupyter notebooks should be re-run every time the course website is created  by the GitHub workflow or, e.g., whether a course incorporated interactive elements.

- **toc.yml**: Contains information on the structure of the course website. For an in-depth explanation, jump to the [respective section](https://diler-digitell.github.io/Jupyter-Book/content/setup-files.html).

<br>

### 3. Make Your First Adjustments

To get started, let's take a look into the "index.md" and the "config.yml" file and exchange the information with your course title, author's names and affiliation, and so on.

It is further essential that you adapt the README and LICENSE files to your needs:

#### The README

To actually display the purpose and, e.g., acknowledgments of your course, you'll have to adapt the "README.md" file on your public repo. In the template, this looks like this:

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/readme.png?raw=true" alt=" depicting the README" class="bg-primary" width="500px">

and translates to this view at the bottom of your public remote repo:

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/readme_rendered.png?raw=true" alt=" depicting the rendered README" class="bg-primary" width="500px">

So simply add the name and explanation of your course, your credentials, and, e.g., how others may get in contact with you to the README.md. Please keep the credit included to our original G0RELLA template lectures.

#### The LICENSE

You may further change the contained LICENSE file to your liking as long as you respect the stated stipulations.

<img src="https://github.com/DiLER-Digitell/Jupyter-Book/main/static/license.png?raw=true" alt=" depicting the LICENSE of the course template" class="bg-primary" width="500px">

```
Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of the copyright holder nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.
```


Before going into detail on how to add and modify this template to your needs, you will learn how to host your course website. 

#### Next Chapter:
In the next chapter, you will discover how to publish and maintain your own course website.



Of course, you can start to add markdown files or Jupyter Notebook files in e.g., the introduction or content folder according to your needs or simply adapt the already existing files.

You will learn how to modify this template and add files according to your needs in the chapter on ["Creating Content"](https://diler-digitell.github.io/Jupyter-Book/content/create/intro.html).


Next, you want to add all your new files to your "toc.yml" file, as described here:
* [Structuring content](https://felixkoerber.github.io/jb/tutorialcontent/structure.html)