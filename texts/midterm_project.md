# Midterm Challenge: NGrams


1. Do a `git pull` on your repo to get the script `playground.sc` that I put in there.

1. See if you can run it from your SBT Console with `:load ../YOUR_REPO/playground.sc`.

1. Create a new file in your repo named `midterm.md`. This is where you will write stuff in English. Do a `git add midterm.md`, `git commit -m "adding midterm file"`, and `git push`.

1. Duplicate your script file into your own repository. Check it into Git and push it to GitHub.

1. Be able to run the script from your `workspace2019/` directory. Start up SBT as always, but use `:load ../YOUR_REPO/yourscript.sc`.

1. Set it up to load your text into a `Vector[String]`, as you have done before.

1. Tokenize your text, stripping punctuation. You want a `Vector[Vector[String]]`.

1. Read [this page](http://daily-scala.blogspot.com/2009/11/iteratorsliding.html) on `.sliding`. **Note** that "iterator" is a super-class that includes `List`, `Vector`, and other ordered collections. 

1. Read [this page on n-grams](https://en.wikipedia.org/wiki/N-gram).

1. Take things from the script `playground.sc`, starting at the top, and import them into your new script file. Run it. Figure out what they do.


## For a Midterm Assessment.

Produce a project write-up, in Markdown, in the file `midterm.md`. Your topic is "N-Grams".

Things you will get points for:

1. A `midterm.md` file, with content in it, pushed into your repo, whence I can pull it.

1. Correct Markdown formatting. There are a billion websites with help on Markdown; find some and use them if you need to. 

1. A paragraph or two on what N-Grams are, and how they are used in various disciplines. Bonus points for giving examples from humanities, sciences, *and* business/industry.

1. Some discussion, in English, of the steps necessary to find N-grams. I think this can be done in 15 words, but you can use more.

1. Some discussion of the *methods* in Scala that might be useful for analyzing a text for n-grams. Examples of "methods" you have used are, *e.g.* `.size`, `.toUpperCase`, `.map`, `.filter`.

1. If you collaborate on this challenge with a classmate, points for naming her or him and giving appropriate credit in your write-up, *e.g.* "My colleague N show me how to…".

1. Extra deluxe bonus points for pushing into your repo a script that I can `git pull` and run to generate n-gram analysis of your text.

1. Correct use of *e.g.* and *i.e*, which do not mean the same thing.

This is intended to be hard. Successfully scripting an n-gram analysis is *not* a prerequisite for passing or getting a good grade. 


