# CSC-270: Computational Approaches to the Humanities

This course aims to teach students of the Liberal Arts concepts, methods, and tools sufficient to make them informed and sophisticated collaborators with computer scientists and professional developers, critical consumers of digital data, and independent and fearless users of computational tools. It should serve as a foundation for further work on digital scholarship. 

The specific work of the course described here will be textual. Each student will pursue a specific project in creating a new digital scholarly edition of a text, testing it with programmatic validation and machine-assisted verification, publishing it, performing basic analyses on it, and capturing the results of that *procedural* analysis as *declarative* scholarly object.

The scholarly, *humanist* principles of this class are ancient, and quite clearly explained by Professor Neel Smith, College of the Holy Cross, in [this video](https://youtu.be/yQ3Znh5vk2w).

## General Expectations

Students are expected to come prepared to class. Specifically:
	
- Laptop working and charged.
- Network connection active (and not in remediation)
- When we start workin in a Virtual Machine, that VM booted and logged in before class.

Students are expected to be *resourceful*:

- In case of errors, read the text that may appear on your screen.
- Look for answers and solutions online.
- Try stuff.

Students are expected to be *collegial*:

- Alert, apparently cheerful, and engaged.
- Generous with help, praise, enthusiasm.
- Stingy with blame.

## Specific Assignments

(Newer assignment appear at the top)
- For **Wednesday, January 23**:
	- Read [Word Processors: Stupid and Inefficient](http://ricardo.ecn.wfu.edu/~cottrell/wp.html). Be able to summarize, very briefly, what the author's point is. 
	- Watch [this video](https://www.youtube.com/watch?v=lSfNQIeb0uo&feature=youtu.be) and [this video](https://www.youtube.com/watch?v=oxuRxtrO2Ag&feature=youtu.be).
	- Know the difference between filesystem, GUI, and CLI.
	- Be able, quickly, to navigate to the *root directory*, your *home directory* and your *desktop directory* in the GUI.
	- Be able to create a folder (or "directory") using the GUI
	- Be able to download a plain-text file from the internet, save it to a given directory, find it in the GUI.
		- Practice with [this file](https://raw.githubusercontent.com/Eumaeus/blackwell_spring2019/master/texts/pride_and_prejudice.txt).
	- Be able to open that text file in a GUI application, by opening *Pride and Prejudice* in Atom.
	- In the CLI, be able to navigate to the *root directory* with `cd /`, to your *home directory* with `cd ~`, and your *desktop directory* with `cd ~/Desktop`.
	- In the CLI, be able to see the files in a directory with `ls`.
	- Know what "tab completion" means, in the CLI.
	- Be able to work with a file using CLI applications: Navigate to where *Pride and Prejudice* is saved on your computer using `cd`, look at its contents using `less` (to get out of `less`, type `q`). Count the words in the novel using `wc`.
	- Be able to find help on any of this by typing, *e.g.* "unix wc" into Google.

- For **Wednesday, January 16**: 
	- Be able to take a screenshot of a portion of your screen. Know how to e-mail a screenshot to someone.
		- [Windows](https://www.laptopmag.com/articles/capture-screenshots-windows-10). Read past the first two, down to #3 and #4!
		- [Mac OS](https://support.apple.com/en-us/HT201361).
	- Download and install [the Atom text editor](https://atom.io). When you first run Atom, read what you see and take action to keep the "Welcome" screen from showing up in the future.
	- Read <https://flight-manual.atom.io/getting-started/sections/atom-basics/> as a basic introduction to Atom.
	- Know how to (or figure out how to) change the UI Theme and Syntax Theme in Atom.
	- Download and install the [DejaVu fonts](https://dejavu-fonts.github.io).
	- **Windows Users** Download the [Git for Windows installer](https://gitforwindows.org) and install it, accepting all defaults.
	- **Mac Users** Via the Mac App Store, download and install XCode. 
	- **There will be a quiz on Wednesday**: You will open Atom, change the theme, take a screenshot of your Atom, and email it to me.

## Module: The Vocabulary, Grammar, & Syntax of Computation

### Technical Skills

- GUI File system: Home, Desktop, Documents, System files.
- The Terminal, or "Command Line Interface" ("CLI"): `terminal.app` on MacOX; `GitBASH` on Windows).
- Navigating the POSIX file system on the CLI: `~`, `pwd`, `cd`, `cat`, `less`.
- Unix commands with flags: `man`, `wc`.
- Text Editor.
	- `Atom.io`.
	- `nano`.
- Downloading, moving, opening, saving in the GUI.
- Back and forth from GUI to CLI.

### Concepts

- A file system is a…
	- hierarchy
	- graph
	- tree
- CLI commands: `[subject] verb [object]`
- It is possible to have multiple views of the same data.
- Tokenization (in simple terms: lines, words, characters).
- Sources for humanist data: the good and the ugly.

### Project Work

- Get an electronic text.
- Save it as a text file; know where it went.
- Make copies of it and rename them.
- Report on its contents with `wc`.
	- Using self-help from `man`, format that output in various ways.

## Attendance policy:

A freshman who exceeds 15% of the class meetings or an upperclassman who exceeds 25% for any reason will be in violation of the maximum established by the University (p. 40 of the Furman University Catalog) and will be dropped from the course with a grade of “F.”

## Academic integrity:

Academic Integrity standards are important to our Furman community and will be upheld in this class.  Students should review the Academic Integrity Pledge posted in the classroom and resources available on <www.furman.edu/integrity>.  In this class, the grade penalty for an academic integrity violation is a reduction in grade in proportion to the gravity of the offense.
 
Additional resources in the Center for Academic Success (CAS; LIB 002):
The Writing & Media Lab (WML) is staffed by student Consultants who are trained to help you improve your writing and multimodal communication skills.  The consultation process is non-directive and intended to allow students to maintain ownership of their work.  In addition to helping with the nuts and bolts, WML Consultants also support you in developing your own ideas thoughtfully and critically, whether you’re writing an essay or planning a video or other multimedia project.  You may drop into the WML during its regular hours (LIB 002; 9 AM to 10 PM) or visit the Writing and Media Lab website to make an appointment online.
 
Professional Academic Assistance Staff in CAS can provide students assistance with time management, study skills, and organizational skills.
 
The Writing and ESL Specialist provides professional writing support as well as support for students whose primary language is not English.

## Accommodation Requests:  

The Student Office for Accessibility Resources is committed to helping qualified students with disabilities achieve their academic goals by providing reasonable academic accommodations under appropriate circumstances. If you have a disability and anticipate the need for an accommodation in order to participate in this class, please register with the Student Office for Accessibility Resources. They will assist you in getting the resources you may need to participate fully in this class.  You can contact the SOAR office at 864.294.2320 or at soar@furman.edu. You can find additional information and request academic accommodations at the SOAR webpage.

## Other Resources

- [The Student Office for Accessibility Resources](http://www2.furman.edu/studentlife/accessibility/Pages/default.aspx) exists to help with any questions or problems having to do with disability, accommodation, or access.
- [Academic Affairs](https://www.furman.edu/about-furman/university-leadership/office-of-academic-affairs/) is the place to go for questions, problems, or complaints about courses, exams, attendance, and grading.
- [Academic Assistance](http://www2.furman.edu/academics/center-for-academic-success/academic-assistance/pages/default.aspx) exists to provide help so you can success; they are excellent and dedicated. They are *not* here only for times of trouble; if you are doing well, they can help you do even better.
- [Title IX](http://www2.furman.edu/sites/title-ix/Pages/default.aspx) of the Educational Amendments Act of 1972, which amended the Civil Rights Act of 1964, and provides: "No person in the United States shall, on the basis of sex, be excluded from participation in, be denied the benefits of, or be subjected to discrimination under any education program or activity receiving Federal financial assistance". If you *even suspect* that another person (faculty, student, staff, outsider) is behaving improperly toward you this office is there to hear your concerns and advise you.

## Grading

| Component     | Percentage |
|---------------|-----------:|
| Quizzes       | 20%        |
| Engagement    | 15%        |
| Presentations | 25%        |
| Final Project | 40%        |
| **Total**     | 100%       |