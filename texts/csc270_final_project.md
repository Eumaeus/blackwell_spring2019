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
    ├── htmlWriter.sc
    └── [README_analysis.sc]

~~~

## Final Deliverables

**Due Tuesday, May 7.** I will do a `git pull` on each of your repos at 5:00 on Tuesday, and evaluate whatever I see there. The essay part of the exam you can email me as a Markdown, MS Word, Pages, or PDF file; get that to me by 5:00 on Tuesday, May 7.

### Mandatory Pieces

- A README.md file, in good Markdown, that explains the contents of this repository and how to use those contents. Remember that *the whole world and everyone in it* can see this. Describe your repository as clearly and comprehensively as possible. You can assume a the your readers know how to use Git and GitHub.
- An HTML version of your text with CSS that goes with it.
- A CEX version of your text.
- **A Reflective Essay**: 500–1000 words. You are writing to someone you have not met. 
	- Describe briefly your academic major and why you chose that (2-3 sentences max).
	- Ennumerate the skills, tools, and concepts your learned this semester. Don't under-sell yourself (but don't lie wildly either). Be as specific and accurate as you can. It can be effective to toss in links when you mention specific tools, like [Scala](https://www.scala-lang.org).
	- After the specific enumeration, devote a couple of sentences to higher-level thinking and abstraction. Computer stuff is complicated, in its details, but if you can boild things down, you will seem like you know what you are talking about. Hints: 
		- Note that whatever we did, we always started with a Collection (Vector in our case).
		- Remember the two things you can do to a Collection of data-objects.
		- Remember the one and only thing a computer can do. Remember that humans are not good at this thing. 
		- You can use the technical term "closure" to describe the `.map` and `.filter` methods you've written.
	- The best essay will then explain how these skills and techniques will make you *better* at what you want to do.
	- It is perfectly okay to focus on Computer OS level stuff, if that is where you can make the best argument; or the design work you did in CSS, or whatever. This  is *practice* for how you will be successful at selling yourself and this little part of your experience.

### Optional Pieces that can Count

The Mandatory Pieces will earn a passing grade of some sort. For more than a minimally passing grade, include one or more of the following (their presence *and* quality will count, of course):

- `analysis.sc` A script that reads your CEX into a CITE Library with a TextRepository ( = Catalog + Corpus ), and performs some kind of analysis or visualization, reporting the results. A very good version of this script will:
	- Have desciptive comments in the code
	- Be described in your (optional) README_analysis.md file (see above), perhaps with links to sources (reading scores, or whatever)
- Discussion of *why* your analysis might be interesting, and *what its limitations are*. 
- Discussion of *how you can have confidence in the results of your analysis*.
- An `md` directory containing Markdown files for your text. And/or a `docx` directory containing `.docx` versions of your texts. You can use [pandoc](https://pandoc.org) for this. (Sample code is in the demo-repository.)

### Overall Assessment

I will grade these with an open mind. Your interpretive essay will *go a long way* toward shaping the criteria I apply to the rest of your work. If you are clear and persuasive in that essay, and whatever else you have done serves to illustrate that, you will earn the hightest grade. I will pay attention to the *professionalism* of your repo. Clean it up. Make the README.md files look good. Remove extra stuff (I can help with that if you need help… deleting stuff from Git can be tricky).

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

- Have a `htmlWriter.sc` script that uses the CiteLibrary API to generate a series of HTML pages for your text; these need to go in `html`. You can use `workspace2019/cite.sc` as the basis for this script. You can also look at the files in [my demo project](https://github.com/Eumaeus/csc270_demo_project).

For **Friday, April 3**:

- Be ready to show off your project's progress.

Later:

- Write a script (`scripts/htmlWriter.sc`), that uses the CiteLibrary API to generate a series of HTML pages for your text; these need to go in `html`. You can use `workspace2019/cite.sc` as the basis for this script.
- In the same script, or in a second one, write methods that generate a Markdown version of your text. This is easier; it can produce a single file.
- Include `html/my.css` to make your HTML pages look pretty.
- Make another script (`scripts/analysis.sc`) that loads your text into a library, and includes some commands for interacting with your text as a Corpus. Ideally:
	- A string search.
	- A token search.
	- An example of an N-Gram analysis.
	- A visualization of where characters appear.

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

