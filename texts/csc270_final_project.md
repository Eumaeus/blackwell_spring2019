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


By **Friday, March 29**: 

- Have a valid, working CEX file of your text. If you aren't there, make an appointment with me to get there. Clean up your repo and get it ready for the final project. 
- Organize your Repo if you haven't done so by the end of class on Wednesday.
- Push your CEX file into your repository.
- You will have a copy of `cite.html` pushed into your repo. Edit it so it loads your text by default. This is the "analysis tool" version of your text.

By **Monday, April 1**:

- Be able to do the following:
	- Load a CiteLibrary from your CEX file in SBT Console. You have the `loadLibrary` function in `cite.sc`.
	- Access its `.corpus` with `_.textRepository.get.corpus` 
	- Be able to select a single passage or range of passages using your Corpus, `~~`, and a CtsUrn.
	- Select a part

By **Wednesday, April 3**:

- Have a `htmlWriter.sc` script that uses the CiteLibrary API to generate a series of HTML pages for your text; these need to go in `html`. You can use `workspace2019/cite.sc` as the basis for this script.

Later:

- Write a script (`scripts/htmlWriter.sc`), that uses the CiteLibrary API to generate a series of HTML pages for your text; these need to go in `html`. You can use `workspace2019/cite.sc` as the basis for this script.
- In the same script, or in a second one, write methods that generate a Markdown version of your text. This is easier; it can produce a single file.
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

## Notes & Logic

There is a demo project online [here](https://github.com/Eumaeus/csc270_demo_project).

I stick useful little code snippets in [my GitHub Gists](https://gist.github.com/Eumaeus). You are free to use those. Ask for help if you need it.

Use the [API for CTS URNs](http://folio2.furman.edu/xciteAPI/edu/holycross/shot/cite/CtsUrn.html) and the [API for the OHCO2 Library](http://folio2.furman.edu/ohco2Api/edu/holycross/shot/ohco2/index.html).

Remember a `CitableNode` object consists of a `urn` and `text`; a `Corpus` object is made from a `Vector[CitableNode]`.

- To write your HTML text, you will need to "chunk" your longer text, producing from your big Corpus a `Vector[Corpus]`, the collection of chunks.
- Once you have, *e.g.* `val vc:Vector[Corpus] = …`, you can use a `for` expression to do the work:

~~~ scala
for (corp <- vc ){
	val myHtml:String = … // results of some Map of corp.nodes
	pageIndex:Int =  vc.indexOf(corp)
	val htmlFileName:String = "file" + s"${pageIndex}" + ".html"
	saveFile(myHtml, fileName = htmlFileName)
}
~~~

- The challenge and fun will be in mapping the `corp.nodes` to HTML strings.
- For chunking, you have two choices:
	- Chunk by number of passages, using `corp.nodes.sliding(N, N)`
	- Chunk by citation-scheme. This might be best for Biblical texts.
	- This would involve combining:
		- Getting a list of the URNs in your corpus
		- Dropping the right-hand element of each to turn verse-URNs into chapter-URNs
		- using `.distinct` to get rid of duplicates
		- using a `.map` to do something to each chapter-Urn
		- using `~~` to get all passages for a chapter-Urn
		- turning those passages into an HTML page

