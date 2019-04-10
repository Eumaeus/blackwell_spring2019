
# Read: Readability Formulas

Read about "readability formulas here: [Readability Formulas](https://en.wikipedia.org/wiki/Readability#Popular_readability_formulas).

Come to class ready to say 

- which of these you think would be easiest to implement, and why;
- which of these would be *best* for certain applications;
- what might be the benefit of doing Readability Analysis on *specific passages* of your text?



## Describe: Understanding Working with a Corpus

Having checked out [my demo repo](https://github.com/Eumaeus/csc270_demo_project), and having done an `sbt console`, be able to describe in plain English what each of the following commands does. **There will be a written assignment similar to this on the final exam.** 

Type the commands in the SBT Console (Do not type the `scala>` part.) Remember that you have a `showMe()` method that can provide a comprehensive view of any value.

Remember, too, that Pope's *Iliad* is cited by: Book / Stanza / Line.

~~~
scala> :load scripts/sentence_work.sc
~~~

In the above, what does `:load` mean?

~~~
scala> popeCorpus
~~~

In the above, what is this value identifying? 

~~~
scala> popeCorpus.nodes
~~~

In the above, what kind of data-structure is identified?

~~~
scala> val resX = popeCorpus.urns.map(_.collapsePassageBy(1))
~~~

What does the above command do? An explanation may take a few sentences.

~~~
scala> val resY = resX.distinct
~~~

What does the above do?

~~~
popeCorpus ~~ resY(0)
popeCorpus ~~ resY(1)
~~~

What am I doing to `popeCorpus` with these `~~` methods? What is the result of each of these commands?

~~~
scala> val resZ = (popeCorpus ~~ resY(0)).nodes
~~~

The above is a slight addition to the previous step. What happens here?

~~~
scala> val resA = resZ.map(_.text)
~~~

And what did the above do?

~~~
scala> val stanzaProse = resA.mkString(" ")

What does `.mkString()` do to a Collection? You may need to look this up.
