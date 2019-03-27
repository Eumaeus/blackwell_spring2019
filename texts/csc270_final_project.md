# Organizing for the Final Project

## Repo Organization

- Create a directory in your directory called `attic` with `mkdir attic`.
- Put all your old working files in there to get them out of the way.
- If you do not already have a `README.md` file in your repo, make one. This is where you will describe what you are publishing.
- The final organization of your github repo should look like this:
~~~
my_repo/
├── MY_Text.cex
├── README.md
├── attic
├── build.sbt
├── cite.html
├── html
│   ├── file_2.html
│   ├── file_3.html
│   ├── index.html
│   └── my.css
└── scripts
    ├── analysis.sc
    └── htmlWriter.sc
~~~

## What You Are Assigned to Do

- By **Friday, March 29**: Have a valid, working CEX file of your text. If you aren't there, make an appointment with me to get there. Clean up your repo and get it ready for the final project. 
- Push your CEX file into your repository.
- Edit the copy of `cite.html` that I will give you, so it loads your text by default. This is the "analysis tool" version of your text.
- Write a script (`scripts/htmlWriter.sc`), that uses the CiteLibrary API to generate a series of HTML pages for your text; these need to go in `html`. You can use `workspace2019/cite.sc` as the basis for this script.
- Include `html/my.css` to make your HTML pages look pretty.
- Make another script (`scripts/analysis.sc`) that loads your text into a library, and includes some commands for interacting with your text as a Corpus. Ideally:
	- A string search.
	- A token search.
	- An example of an N-Gram analysis.
- Document your work in `README.md`:
	- Your text and its source.
	- Why someone might care about your text.
	- The URNs for it.
	- Some discussion of how folks might use `analysis.sc` and `cite.html` to work with your text.
	- Some discussion of your aesthetic decisions in making your HTML page.

