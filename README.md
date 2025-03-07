# COMP-2600-A2

## Getting Started

This README outlines the instructions on how this resume is formatted and hosted on this website usign Etter's principles. The resume is written in Markdown and hosted by using Python-based Pelican.

## Prerequisites

Users must have the followings to perform the operations:

- A working personal computer or laptop.

- The Internet connection is also required.

- The operating system must be updated to the latest version.

## Instructions

### *Create and run a website using static site generator:*

- The choice of static site generator may be varied for lots of people, such as Ruby-based Jekyll, Go-based Hugo or Python-based Pelican. In this tutorial we will be using Pelican for simplicity.

#### Installing Python:

- Python can be installed on Microsoft Store or directly from the [website.](https://www.python.org/downloads/). If you already have Python installed and set up in your variable, you can skip these instructions.

#### Installing Pelican and setting up environment variables:

- Once Python is installed, create an empty folder on your computer and access there.

- Right-click in the folder and select the option to open the terminal.

- Type this instruction to the terminal: *python -m pip install "pelican[markdown]"*.

- Go to the search box on your computer and search for "Edit the system environment variables."

- In the System Properties window, click on the "Environment Variables" button. 

- In the Environment Variables windows, locate the "Path" variable and click "Edit". 

- Click on "New" then add the path to the Python Scripts folder (this is the same as what the warnings generated after installing Pelican). 

- Click "Okay" on all windows to confirm these changes.

#### Generating a website:

- In your terminal, type this command: *pelican-quickstart*

- You will then see a prompt that the script will generate the website based on your answers on the given set of questions as below:

```
Welcome to pelican-quickstart v4.11.0.

This script will help you create a new Pelican-based website.
Please answer the following questions so this script can generate the files needed by Pelican.

> Where do you want to create your new web site? [.]
> What will be the title of this web site? //type your website title here
> Who will be the author of this web site? //type your name here
> What will be the default language of this web site? [en]
> Do you want to specify a URL prefix? e.g., https://example.com (Y/n) n
> Do you want to enable article pagination? (Y/n)
> How many articles per page do you want? [10]
> What is your time zone? [America/Winnipeg]
> Do you want to generate a tasks.py/Makefile to automate generation and publishing? (Y/n)
> Do you want to upload your website using FTP? (y/N)
> Do you want to upload your website using SSH? (y/N)
> Do you want to upload your website using Dropbox? (y/N)
> Do you want to upload your website using S3? (y/N)
> Do you want to upload your website using Rackspace Cloud Files? (y/N)
> Do you want to upload your website using GitHub Pages? (y/N)
Done. Your new project is available at [your directory]
```

- Here, we set our answers, except our URL prefix, which in this examples answer 'No', to default by pressing Enter without answering. Any answers in this example that start with "//" in this instruction require your input.

- Once the website contents have been created, type "ls" into the terminal to check for the folder's content.

#### Running the website:

- Type *pelican content # or: make html* to generate the website's content.

- Type *pelican --listen # or: make serve* to run the website on the temporary server.

- Click on the provided Internet protocol (IP address) to visit your website.

- Once you are done, return to the terminal then press Control and C key to terminate the session.

### *Adding your contents to the website:* 

- Go to the content folder then create your markdown files there.

- Optionally, you can add your resume here.

### *Host your website using forges:*

- The choice of forge may be varied for lots of people, such as Github, Gitlab, Savannah, Phorge, etc. In this tutorial we will be using Github for simplicity.

#### Installing Git 

- On the terminal, install ghp-import by typing this instruction: *python -m pip install ghp-import*

- Install git directly [here](https://git-scm.com/).

#### Using GitHub to clone repository:

- Sign in or create an account on [GitHub](https://github.com/).

- In your GitHub main page, click on the "New" button to create a new repository. You can give any name to this repository.

- Open Git bash. Then in this window, type *git remote add origin* for first time creating directory or *git clone* if the directory already exists. Do not press Enter yet until the next instruction.

- Attach the link to your repository to clone it onto your machine. The link to this directory is provided after this command executes.

- Copy the link to created from the prompt, then type *cd [your directory link]* to travel to your directory.

#### Commit website to GitHub using Git:

- Refer to the "Generate a website" instruction to create a website here. The only difference is that our URL prefix will be your website on GitHub, i.e., *[your_user_name].github.io*.

- Open Git bash and set to your directory (see *Using GitHub to clone repository* for details on how to set to current directory).

- Type the following commands to push your contents onto GitHub:

    - *pelican content -s publishconf.py*: When you are ready to publish your website.
 
    - *ghp-import output -b gh-pages*: Create a branch called gh-pages to store your website.

    - *git push origin gh-pages*: Push your changes onto the current repostory on GitHub.

- Your changes can be viewed at the domain you have already set up. You are good to go!

## Resources

- Markdown guide for beginners: https://www.markdownguide.org/

- Pelican documentation: https://docs.getpelican.com/en/latest/

- GitHub's User Guide: https://docs.github.com/en

- Git's documentation: https://git-scm.com/docs/git

## FAQs

- __*Why is Markdown better than writing raw HTML?*__

- *Answer:* Markdown's syntax is simple and easy to learn compared to HTML. HTML may have more freedom in designing choice, however it has a higher learning curve compared to Markdown and may require more complex operations.

- __*I have created the website using Pelican, but I cannot access the address. How to fix this issue?*__

- *Answer:* Try to terminate the current session, then type the command to generate the website again. Once you got the website running, try to validate if the URL you entered during the quickstart is correct or not. It can be viewed in the publishconf.py file in your directory.

## Credits

- Duc Cam Thai - editor

- Saman HM - peer reviewer

- Mehidi - peer reviewer

- Pelican static site theme: 