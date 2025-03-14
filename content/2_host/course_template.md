# The Course Template

This tutorial is further paired with a template course, that you can freely [download here](https://github.com/M-earnest/course_template_diler/archive/refs/heads/master.zip). To see a rendered version of the website this template course produces follow this [link](https://m-earnest.github.io/course_template_diler/general_information/index.html). This course will in essence teach you how to adapt this template to host your own online courses. An explanation of the template can be found below.


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
