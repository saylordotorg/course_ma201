---
layout: default
title: "MA201: Mathematical Logic and Theory of Computation"
course_description: "An examination of the use of mathematical logic and computation for solving some of the world's fundamental problems."
next: ../Unit03
previous: ../Unit01
---
**Unit 2: Modeling Computation** <span id="2"></span> 
*The advance of first-order logic as a way to formalize mathematical
truth inspired several efforts in the 1930s to give a technical
definition for what an effective process – an algorithm, or a method for
computing – ought to look like.  Several of these definitions turned out
to be equivalent.  In the next two decades, these definitions became the
dominant mathematical model and the dominant metaphor behind the
invention of the digital computer.  
    
 Our first attempt to model computation uses a somewhat weaker
definition, one that takes seriously the limitations on memory and
storage space that a computer has, and that lends itself to making
comprehensive pictures of the model.  This model of computation is
called the* finite-state automaton*, which proves to be very useful but
very restrictive.  
    
 We then move on to the equivalent definitions given by several people
in the 1930s, which abstract the time and memory restrictions in real
computers – and give the most convincing negative results.  After all,
if you couldn’t solve the problem even with unbounded time and memory,
you couldn’t solve it in a more realistic model, either.  We will
explore in some detail how to encode these computations as natural
numbers, and how to use these encodings to prove impossibility results,
including Gödel Incompleteness (the theorem that a certain kind of
first-order structure cannot be described by a computable set of
first-order axioms), and to construct examples of counterintuitive
behavior in computation.  
    
 Central questions to keep in mind throughout this unit:  What is a
computer?  What features are included or abstracted in each model?  Is
there a psychological or philosophical difference between the
mathematically equivalent models?  What is the importance of the
counterexamples (e.g., the Gödel sentence and the incomplete set)?*

**Unit 2 Time Advisory**  
This unit should take approximately 55 hours to complete.  
  
 ☐    Subunit 2.1: 15 hours

  
 ☐    Sub-subunit 2.1.1: 2 hours  
  
 ☐    Sub-subunit 2.1.2: 2 hours  
  
 ☐    Sub-subunit 2.1.3: 2 hours  
  
 ☐    Sub-subunit 2.1.4: 2 hours  
  
 ☐    Sub-subunit 2.1.5: 2 hours  
  
 ☐    Sub-subunit 2.1.6: 3 hours  
  
 ☐    Sub-subunit 2.1.7: 2 hours

  
 ☐    Subunit 2.2: 16 hours

  
 ☐    Sub-subunit 2.2.1: 3 hours  
  
 ☐    Sub-subunit 2.2.2: 2 hours  
  
 ☐    Sub-subunit 2.2.3: 2 hours  
  
 ☐    Sub-subunit 2.2.4: 3 hours  
  
 ☐    Sub-subunit 2.2.5: 1 hour  
  
 ☐    Sub-subunit 2.2.6: 3 hours  
  
 ☐    Sub-subunit 2.2.7: 2 hours

  
 ☐    Subunit 2.3: 7 hours

  
 ☐    Sub-subunit 2.3.1: 2 hours  
  
 ☐    Sub-subunit 2.3.2: 2 hours  
  
 ☐    Sub-subunit 2.3.3: 3 hours

  
 ☐    Subunit 2.4: 11 hours

  
 ☐    Sub-subunit 2.4.1: 1 hour  
  
 ☐    Sub-subunit 2.4.2: 2 hours  
  
 ☐    Sub-subunit 2.4.3: 3 hours  
  
 ☐    Sub-subunit 2.4.4: 3 hours  
  
 ☐    Sub-subunit 2.4.5: 2 hours

  
 ☐    Subunit 2.5: 6 hours

  
 ☐    Sub-subunit 2.5.1: 2 hours  
  
 ☐    Sub-subunit 2.5.2: 4 hours

**Unit2 Learning Outcomes**  
Upon successful completion of this unit, the student will be able to:
-   Give examples of languages recognized by finite-state automata.
-   Prove the equivalence of deterministic and non-deterministic finite
    automata.
-   Apply the pumping lemma to show that some computations are
    impossible for finite automata.
-   Construct a Turing machine to compute a function.
-   Use Church’s Thesis to argue that a function is computable.
-   Distinguish primitive recursive functions from recursive functions.
-   Define functions in the lambda calculus.
-   Give an example of a computably enumerable set that is not
    computable.
-   Give an example of a non-computable set.
-   Explain the meaning of the Gödel Incompleteness Theorems.
-   Construct a solution to Post’s Problem.

**2.1 Finite Automata and Regular Languages** <span id="2.1"></span> 
**2.1.1 Deterministic Finite Automata** <span id="2.1.1"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Chapter 2, Sections 2.1
    and 2.2”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Chapter 2, Sections
    2.1 and
    2.2”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf)
    (PDF)  
      
     Instructions: Read from the beginning of Chapter 2 to the end of
    section 2.2.  Observe the usual issues about definitions.  Make more
    examples, and some near-misses.  Verify that each example satisfies
    the definition.  Remember that it was said (by no less an authority
    than statistician George Box), “Essentially, all models are wrong,
    but some are useful.”  What aspects of a computer does the
    definition of a finite automaton capture well?  What aspects does it
    capture poorly?  
      
     This reading should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Assignment: Carleton University: Anil Maheshwari and Michiel
    Smid’s *Introduction to the Theory of Computation*: “Exercise 2.1”**
    Link: Carleton University: Anil Maheshwari and Michiel
    Smid’s *Introduction to the Theory of Computation*: [“Exercise
    2.1”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf)* *(PDF)  
      
     Instructions: Go to the Exercises starting on page 78 and solve any
    three items from Exercise 2.1.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.2 Regular Operations** <span id="2.1.2"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Section 2.3”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Section
    2.3”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Read all of section 2.3.  You could think of the
    relationship between regular operations and finite automata as an
    image of the relationship between syntax and semantics in model
    theory.  The hope, in the end, is that the two will coincide – that
    is, that the set of regular languages (those accepted by finite
    automata) will be generated somehow by regular operations.  This
    works out, in the end, but it takes some time to get to this proof.
     Again, make sure you’re reading actively through all these
    definitions and bookkeeping proofs.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.3 Non-Deterministic Finite Automata** <span id="2.1.3"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Section 2.4”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Section
    2.4”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Read all of section 2.4.  Non-deterministic automata
    may – even should – feel a little contrived.  They originated as a
    guess about what kind of “magic” we could add to an automaton in
    order to allow it to do more.  The “magic” involved here is that
    there are two (or more) possibilities for the “right” next step, and
    the automaton is given the ability to “magically” know which one is
    right.  In the end, it doesn’t matter for automata, but with other
    models of computation, this turns out to be a big issue – perhaps
    the biggest open problem in theoretical computing today.  
      
     This reading should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Assignment: Carleton University: Anil Maheshwari and Michiel
    Smid’s *Introduction to the Theory of Computation*: “Exercise 2.2”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Exercise
    2.2”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Go to page 79 and solve Exercise 2.2.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.4 Equivalence of DFAs and NFAs** <span id="2.1.4"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Section 2.5”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Section
    2.5”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Read all of section 2.5.  If you have properly
    understood the definitions of NFAs and DFAs, you should intuitively
    believe that the main theorem of this section is impossible.  The
    result should be surprising.  Suppose you had a magical ability to
    always guess right.  It should help you, shouldn’t it?  And yet this
    result says that (at least in this context) it really doesn’t.  You
    should perhaps read the proof of equivalence with a specific NFA in
    mind, perhaps one that you think would be hard for a DFA to emulate.
     In any case, read skeptically.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.5 Closure Under the Regular Operations** <span id="2.1.5"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Section 2.6”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Section
    2.6”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Read section 2.6.  The goal here is to develop an
    “algebra” to represent what automata are doing.  The roots of this
    sort of analysis go back to Noam Chomsky’s attempt to explain how
    such a complex thing as language could be biologically hard-wired,
    and could be independent of the many wildly different natural
    languages in use.  Try, in each proof, to draw the state diagram of
    the “proof” (i.e., the DFA witnessing closure under that operation)
    before either looking at the figure or reading the proof.  Then look
    at the figure provided, if there is one, and then read the proof.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.6 Regular Expressions and Regular Languages** <span
id="2.1.6"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Sections 2.7 and 2.8”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Sections 2.7 and
    2.8”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Read sections 2.7 and 2.8.  This is a continuation of
    the work in the previous reading to develop an algebra to describe
    what automata do.  The regular expressions are quintessential forms
    of “grammatically correct sentences” in the language.  In English,
    for instance, we have a common form SVO, where S is a subject, V is
    a transitive verb, and O is an object.  Whether you would want to
    say it or not, any such construction (with a few extra details) is a
    legitimate English sentence.  Of course, the “languages” we care
    about in computation are a bit more abstract, but it’s helpful to
    think of them as languages anyway.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Assignment: Carleton University: Anil Maheshwari and Michiel
    Smid’s *Introduction to the Theory of Computation*: “Exercise 2.8”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Exercise
    2.8”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Go to page 81 and solve Exercise 2.8.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.1.7 The Pumping Lemma and Non-Regular Languages** <span
id="2.1.7"></span> 
-   **Reading: Carleton University: Anil Maheshwari and Michiel Smid’s
    Introduction to the Theory of Computation: “Section 2.9”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Section
    2.9”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Read all of section 2.9.  While the pumping lemma is
    a theorem usually stated in the form, “For all regular languages A,”
    the real importance is in the contrapositive: “If A does not have a
    certain property, then A is not regular.”  It’s really a way of
    proving that DFAs cannot do certain things; it’s a result about the
    limits of computers, insofar as finite automata are good models for
    them.  
      
     This reading should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Assignment: Carleton University: Anil Maheshwari and Michiel
    Smid’s *Introduction to the Theory of Computation*: “Exercise
    2.22”**
    Link: Carleton University: Anil Maheshwari and Michiel Smid’s
    *Introduction to the Theory of Computation*: [“Exercise
    2.22”](http://www.saylor.org/site/wp-content/uploads/2013/10/MA201-Maheshwari-Smid-TheoryOfComputation.pdf) (PDF)  
      
     Instructions: Go to page 84 and solve Exercise 2.22.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2 Turing Machines and Related Models** <span id="2.2"></span> 
**2.2.1 Turing Machines** <span id="2.2.1"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Chapter 2 Introduction and Sections 2.1 and
    2.2”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Chapter 2 Introduction and Sections 2.1 and
    2.2”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read from the beginning of Chapter 2 through the
    end of section 2.2.  This is a much stronger model than finite
    automata (i.e., one of these can do things that a DFA can’t).
     Again, think of the big modeling questions: Where does the Turing
    machine definition go right as a model of computation (e.g., where
    is it better than a DFA)?  Where does it go wrong?  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  

-   **Assignment: University of Manchester: Andrea Schalk’s Turing
    Machines: “Section 3”**
    Link: University of Manchester: Andrea Schalk’s *Turing Machines*:
    [“Section 3”](http://www.cs.man.ac.uk/~schalk/2121/) (PDF or PS)  
      
     Instructions: In the “Course notes” section, click on the link for
    the format you want of “Section 3: Turing machines.”  Go to page 54
    and solve both parts of Exercise 23.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  

**2.2.2 Primitive Recursion** <span id="2.2.2"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Sections 2.3 and 2.4”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Sections 2.3 and
    2.4”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read sections 2.3 and 2.4.  The great miracle of
    the general-purpose computer in the 1930s was the diversity of
    approaches that produced the same thing.  Primitive recursion was
    the approach of Gödel, whose motivation was more philosophical than
    technical.  As usual, make up examples as you read.  Check the
    examples given.  Make near-miss non-examples.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2.3 Recursive Functions** <span id="2.2.3"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 2.5”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    2.5”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 2.5.  While the definitions are of
    great importance and should be given the usual treatment, the proof
    that begins the section will become the real star of the show.  It
    is known as a “diagonal argument” (can you see why?) and is the
    central technique in all computability theory, although it appears
    in many guises.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2.4 Recursive is Equivalent to Turing Computable** <span
id="2.2.4"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 2.6”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    2.6”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 2.6.  Read the proof critically.  It
    is important that, in the long run, you believe that partial
    recursive functions and partial Turing computable functions are the
    same.  Pick some examples where the theorem seems hard to believe.
     Follow through the proof with these examples, to see how it catches
    them.  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2.5 Church’s Thesis** <span id="2.2.5"></span> 
-   **Reading: Stanford Encyclopedia of Philosophy: B. Jack Copeland’s
    “The Church-Turing Thesis”**
    Link: Stanford Encyclopedia of Philosophy: B. Jack Copeland’s [“The
    Church-Turing
    Thesis”](http://plato.stanford.edu/entries/church-turing/) (HTML)  
      
     Instructions: Read the article.  The real importance for your
    learning of the proof in the previous section is that it helps you
    believe the extremely important Church-Turing Thesis (sometimes
    called Church’s Thesis).  The point here is that if we believe the
    Church-Turing Thesis, then we believe that the concept of
    “computation” is mathematically well-defined – and that, for
    instance, we can prove impossibility results for computation without
    fear that some new idea of what computation means will come and
    supersede our result.  
      
     People often attempt things that are known to be impossible,
    thinking that there is an analogy of mathematical impossibilities
    (things nobody will ever be able to do) with technical
    impossibilities (things we can’t imagine how anybody would ever do).
     People who try to trisect angles, for instance, might say that
    “people used to think airplanes were impossible, too.”  The
    Church-Turing Thesis shows that any impossibility results that we
    prove about computation are like the impossibility of angle
    trisection (a genuine proof of permanent impossibility), not like
    the “impossibility” of flight (a matter of technological
    distance).  
      
     This reading should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  

**2.2.6 Theorems on Computability** <span id="2.2.6"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 2.7”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    2.7”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 2.7.  These theorems all have
    important uses, but the real importance at the moment is that you
    get used to the kinds of things you can do with a formally defined
    model of computation.  Work through each proof.  See if you can
    anticipate the next step in each proof.  Then reflect on the
    importance of Kleene’s Normal Form Theorem: What does it mean for
    computer hardware?  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.2.7 The Lambda Calculus** <span id="2.2.7"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 2.8”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    2.8”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 2.8.  This added model of
    computability (equivalent to Turing computability and partial
    recursion) is of particular importance for computing: it points the
    way (in Unit 3 of this course) to a link between formal proofs and
    computation.  If you want to be impressed by Unit 3 – or even to
    understand its importance – you would do well to make sure you’re
    convinced of the proofs in this section.  Also, lambda calculus is
    the model of computation that has been turned most explicitly into a
    programming language.  Most of the so-called “functional” languages
    (e.g., FORTRAN) are derived from lambda calculus.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.3 Computability Theory** <span id="2.3"></span> 
**2.3.1 Computably Enumerable Sets** <span id="2.3.1"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Chapter 3 Introduction and Sections 3.1 and
    3.2”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Chapter 3 Introduction and Sections 3.1 and
    3.2”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read from the beginning of Chapter 3 through the
    end of section 3.2.  The non-computability of K<sub>0</sub> is our
    second big encounter with the diagonal argument.  It is the
    archetypal proof of which all other non-computability proofs are
    either imitations or applications.  It also, in itself, places a
    kind of limit on automated software verification: If you can’t check
    whether a program halts, then you can’t check much.  
      
     This reading should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Assignment: University of Ottawa: Pieter Hofstra’s Recursion
    Theory: “Exercise 3.23”**
    Link: University of Ottawa: Pieter Hofstra’s *Recursion Theory*:
    [“Exercise
    3.23”](http://mysite.science.uottawa.ca/phofstra/preprints.html) (PS)  
      
     Instructions: Under the heading of “Lecture Notes,” click on the
    link to download the file.  Solve Exercise 3.23 on page 77.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.3.2 Reducibility and Rice’s Theorem** <span id="2.3.2"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 3.3”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    3.3”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 3.3.  This is the way one applies the
    non-computability of K<sub>0</sub> to prove non-computability of
    other things.  The results of this section justify the definition of
    reducibility.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.3.3 The Fixed-Point Theorem** <span id="2.3.3"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Sections 3.4 and 3.5”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Sections 3.4 and
    3.5”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read sections 3.4 and 3.5.  To a mathematician, a
    fixed-point theorem is a very natural thing – if you’re dealing with
    continuous functions in some sort of geometric context.  Here, the
    point is very technical – and it would not be worth studying if it
    were not useful for so many other results, some of which we’ll see
    in later sections.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  

-   **Assignment: University of Ottawa: Pieter Hofstra’s Recursion
    Theory: “Exercise 3.11”**
    Link: University of Ottawa: Pieter Hofstra’s *Recursion Theory*:
    [“Exercise
    3.11”](http://mysite.science.uottawa.ca/phofstra/preprints.html) (PS)  
      
     Instructions: Under the heading of “Lecture Notes,” click on the
    link to download the file.  Solve Exercise 3.11 on page 76.  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.4 Incompleteness** <span id="2.4"></span> 
**2.4.1 Historical Background** <span id="2.4.1"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 4.1”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    4.1”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 4.1.  Many people consider the
    Incompleteness Theorems to be the beginning of modern logic, and
    certainly the beginning of its involvement with computation.  The
    formulation of the theorems, though, is more than a little recondite
    outside its historical context.  If we aren’t careful, the
    Incompleteness Theorems can sound like either shallow philosophy or
    uninteresting technical details in a part of math that not many
    people care about any more.  It is neither, and the point of this
    section is to help you navigate this.  
      
     This reading should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.4.2 Background in Logic** <span id="2.4.2"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 4.2”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    4.2”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 4.2.  Many points will be familiar
    from our study of model theory, but it is good to read them to fill
    in details to which we didn’t attend then.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.4.3 Representability in Q** <span id="2.4.3"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 4.3”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    4.3”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 4.3.  The point here is to make a
    model-theoretic definition of computability, equivalent to the
    others we have just seen.  The ultimate goal is to use this as a way
    to carry out a diagonal argument.  Many of the points here are
    technical and difficult, but they are fundamental for understanding
    the theorems, which are, collectively, one of the great intellectual
    accomplishments of human history.  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  

**2.4.4 The First Incompleteness Theorem** <span id="2.4.4"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 4.4”**
    Link: Carnegie Mellon University: Jeremy Avigad’s *Computability and
    Incompleteness*: [“Section
    4.4”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 4.4.  Much has been made of this
    theorem in the popular literature.  What do you make of it?  What is
    its practical meaning?  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.  

**2.4.5 The Second Incompleteness Theorem** <span id="2.4.5"></span> 
-   **Reading: Carnegie Mellon University: Jeremy Avigad’s Computability
    and Incompleteness: “Section 4.7”**
    Link: Carnegie Mellon University: Jeremy Avigad’s Computability and
    Incompleteness: [“Section
    4.7”](http://www.andrew.cmu.edu/user/avigad/teaching.html) (PDF)  
      
     Instructions: Near the bottom of the page, find the bullet point,
    “Computability and Incompleteness,” and click on the PDF link for
    “Lecture notes.”  Read section 4.7.  What does the Second
    Incompleteness Theorem say that we already knew from the First?
     What does it tell us that is new?  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.5 Turing Reduction and Post’s Problem** <span id="2.5"></span> 
**2.5.1 Post’s Problem and Reducibilities** <span id="2.5.1"></span> 
-   **Reading: National University of Singapore: Frank Stephan’s
    Recursion Theory: “Chapter 4”**
    Link: National University of Singapore: Frank Stephan’s *Recursion
    Theory*: [“Chapter
    4”](http://www.comp.nus.edu.sg/~fstephan/recursiontheory.html) (PDF
    or PS).  
      
     Instructions: In the section labeled “Lecture Notes,” click on the
    link to the file format of your choice.  Read Chapter 4, and solve
    Exercises 4.4, 4.7, and 4.13.  One can still start a very
    interesting (and sometimes heated) conversation among experts by
    asking for a “natural” solution to Post’s problem.  Many people
    believe that the constructions of solutions that we will see (and
    many others more recent) have an *ad hoc* feel to them – as if Post
    might say (though he didn’t), “Yes, but that’s not really what I was
    looking for.”  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**2.5.2 A Solution to Post’s Problem for Enumerable Sets** <span
id="2.5.2"></span> 
-   **Reading: National University of Singapore: Frank Stephan’s
    Recursion Theory: “Chapter 7”**
    Link: National University of Singapore: Frank Stephan’s *Recursion
    Theory*: [“Chapter
    7”](http://www.comp.nus.edu.sg/~fstephan/recursiontheory.html) (PDF
    or PS)  
      
     Instructions: In the section labeled “Lecture Notes,” click on the
    link to the file format of your choice.  Read Chapter 7, and solve
    Exercises 7.2, 7.3, and 7.5.  Think on the issue of naturality, too.
     Does the set constructed in this section seem intuitively
    reasonable to you?  Or is it one of those theorems that you know
    must be true because you’ve seen the proof, but that in your heart
    you still don’t feel quite right about?  There are experts – experts
    at the highest level – on either side of the question.  
      
     This reading should take approximately 4 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.


