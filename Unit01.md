**Unit 1: Model Theory** <span id="1"></span> 
*Model theory is a generalization of combinatorics and abstract algebra
in which mathematical structures are described by axioms, and their
structure is examined through homomorphisms and definable sets. 
Roughly, we start with some “language,” giving the functions, relations,
and constants that are relevant.  In this language, we can “define”
certain properties, and can also check the truth of statements about
whether these properties are satisfied.  
  
 We will first define the general concepts of “structure” and
“morphism,” which give rise to the language as the list of things that
must be “preserved” by the morphism: in a graph, for instance, a
morphism is a function that preserves adjacency.  The power of this
approach is clarified by three major results: the back-and-forth
technique to construct isomorphisms, the Löwenheim-Skolem Theorem to
construct non-isomorphic structures sharing many properties with an
original, and the Compactness Theorem, which allows us to determine some
“extra” properties preserved by isomorphism but not definable in the
language.  
  
 Central questions to keep in mind throughout this unit:  What
properties can be defined?  What properties cannot?  When is it possible
to specify a particular mathematical object up to isomorphism, and what
does this specification look like?*

**Unit 1 Time Advisory**  
This unit should take approximately 30 hours to complete.  
  
 ☐    Subunit 1.1: 5 hours

  
 ☐    Sub-subunit 1.1.1: 2 hours  
  
 ☐    Sub-subunit 1.1.2: 3 hours

  
 ☐    Subunit 1.2: 8 hours

  
 ☐    Sub-subunit 1.2.1: 2 hours  
  
 ☐    Sub-subunit 1.2.2: 3 hours  
  
 ☐    Sub-subunit 1.2.3: 3 hours

  
 ☐    Subunit 1.3: 9 hours

  
 ☐    Sub-subunit 1.3.1: 3 hours  
  
 ☐    Sub-subunit 1.3.2: 3 hours  
  
 ☐    Sub-subunit 1.3.3: 3 hours

  
 ☐    Subunit 1.4: 8 hours

  
 ☐    Sub-subunit 1.4.1: 2 hours  
  
 ☐    Sub-subunit 1.4.2: 3 hours  
  
 ☐    Sub-subunit 1.4.3: 3 hours

**Unit1 Learning Outcomes**  
Upon successful completion of this unit, the student will be able to:
-   Define the syntax and semantics of first-order logic.
-   Distinguish syntactic and semantic features.
-   Define morphisms in a general context.
-   Define elementarity.
-   Use the back-and-forth method to construct isomorphisms.
-   Use the Löwenheim-Skolem Theorem to establish non-elementarity.
-   Use compactness to establish non-elementarity.

**1.1 Structures and Morphisms** <span id="1.1"></span> 
**1.1.1 Structures and Isomorphism** <span id="1.1.1"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 1.1”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    1.1”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read section 1.1 in its entirety.  As you
    read, remember the key rule to reading mathematical definitions:
    make up examples as you go.  Can you make up first-order structures
    in different languages?  With the same domain?  With the same
    language but important differences?  Use these to build examples of
    the later definitions.  Also, try to build “near-miss” non-examples:
    things that satisfy all but one part of a definition, or that
    otherwise nearly satisfy the definition, but not quite.  Once you
    have done this, solve Exercise 1.1.14.  When you are finished, you
    can check your answers against the Saylor Foundation’s [“Solutions
    for Exercises in Unit 1 – Exercise
    1.1.14”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.1.1.pdf)
    (PDF).  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.1.2 Examples** <span id="1.1.2"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 1.2”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    1.2”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read section 1.2 in its entirety.  If you are
    not familiar with fields and groups, you have two options at this
    point: First, you can ignore the terms, and think of a *field* as
    being like the rational numbers with addition and multiplication,
    and of a *group* as being like the integers under addition or the
    invertible 2x2 matrices under matrix multiplication (the latter is
    the better example, if you know it).  The second option is to look
    in, briefly, on [MA231: Abstract Algebra
    I](http://www.saylor.org/courses/ma231/), where you can find
    definitions.  (These are not critical to this course but may make
    you feel a bit more comfortable.)  In any case, think on these
    questions: What are the important properties of each kind of
    structure that we might want to be able to express or to require a
    homomorphism to preserve?  Make a list of important properties for
    each kind of structure, and keep the list for the next subunit.  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.2 First-Order Formulas** <span id="1.2"></span> 
**1.2.1 The Syntax** <span id="1.2.1"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Chapter 2 Introduction and Section 2.1”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Chapter 2 Introduction and Section
    2.1”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read from the beginning of Chapter 2 through
    the end of section 2.1.  Be careful in reading proofs.  Even with a
    proof that we know is correct, the right way to read a proof is by
    believing, for as long as possible, that it is wrong.  Much of this
    section is the near-obvious bookkeeping system; that is, the
    clerical methods by which we can keep track of necessary details.
     Very little will be surprising.  However, a careful – even
    skeptical – reading of the proofs gives a good idea of the level of
    formal detail that is often necessary in logic, even if it is
    unnecessary in algebra or analysis.  After you have read the
    formula, prove the statement given as Exercise 2.1.10.  When you are
    finished, you can check your answers against the Saylor Foundation’s
    [“Solutions for Exercises in Unit 1 – Exercise
    2.1.10”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.2.1.pdf)
    (PDF).  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.2.2 The Semantics** <span id="1.2.2"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 2.2”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    2.2”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read section 2.2 in its entirety, solving
    Exercise 2.2.4 when you come to it.  Then go back to the list of
    properties you made in subunit 1.1.2.  Write a formula, where
    possible, to express each of these properties.  Remember, in doing
    so, to use the definitions *strictly*: the variables may range only
    over elements of the domain (and not, for instance, over other
    formulas); only finitely many applications of the rules in the
    inductive definition can be made (so that, for instance, one can
    have only a finite conjunction).  In some cases, it will be
    impossible.  Two very important points arise here, which will form a
    good part of the rest of Unit 1: (a) Many important properties can
    be expressed by formulas in the natural signature, and (b) Some
    important properties cannot.  When you are finished, you can check
    your answers against the Saylor Foundation’s [“Solutions for
    Exercises in Unit 1 – Exercise
    2.2.4”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.2.2.pdf)
    (PDF).  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.2.3 Definable Sets** <span id="1.2.3"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 2.3”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    2.3”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read section 2.3 in its entirety, and solve
    Exercise 2.3.6.  When you are finished, you can check your answers
    against the Saylor Foundation’s [“Solutions for Exercises in Unit 1
    – Exercise
    2.3.6”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.2.3.pdf)
    (PDF).  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.3 Elementarity** <span id="1.3"></span> 
**1.3.1 Theories and Elementarity** <span id="1.3.1"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Chapter 3 Introduction and Section 3.1”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Chapter 3 Introduction and Section
    3.1”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read from the beginning of Chapter 3 through
    the end of section 3.1, solving the two in-text exercises as you
    come to them.  Continue to read the proofs carefully (i.e.,
    skeptically).  The proof in section 3.1.11 is worthy of special
    mention: it is the classic example of the so-called “back-and-forth”
    argument, which is ubiquitous in model theory.  Why is it called
    “back-and-forth”?  Can you say what the general method is?  When you
    are finished, you can check your answers against the Saylor
    Foundation’s [“Solutions for Exercises in Unit 1 – Exercise 3.1.2
    and
    3.1.4”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.3.1.pdf)
    (PDF).  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.3.2 Elementary Maps and Partial Isomorphisms** <span
id="1.3.2"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 3.2”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    3.2”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read section 3.2 in its entirety, solving the
    in-text exercises as you come to them.  The importance of this
    section is hard to overstate; almost everything else in model theory
    depends on elementary maps, and on the ability to match parts of
    structures.  Notice that, in general, an elementary bijection need
    not be an isomorphism.  Under what conditions must it be?  When you
    are finished, you can check your answers against the Saylor
    Foundation’s [“Solutions for Exercises in Unit 1 – Exercise 3.2.1,
    3.2.3, 3.2.4, and
    3.2.5”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.3.2-1.pdf)
    (PDF).  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

-   **Assignment: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Exercise 1”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Exercise
    1”](http://staff.science.uva.nl/~domenico/model.html) (PDF)  
      
     Instructions: Click on the link to “Exercise 1” and solve the
    problem.  When you are finished, you can check your answers against
    the Saylor Foundation’s [“Solutions for Exercises in Unit 1 –
    Exercise
    1”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.3.2-2.pdf)
    (PDF).  
      
     This assignment should take approximately 1 hour.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.3.3 The Downward Löwenheim-Skolem Theorem** <span
id="1.3.3"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 3.3”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    3.3”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read section 3.3 in its entirety, solving the
    in-text exercise as you come to it.  Notice how counterintuitive the
    Löwenheim-Skolem Theorem is: All properties of the real numbers that
    can be expressed with first-order formulas can simultaneously be
    satisfied in a countable structure.  In algebra, this is not so
    surprising, but this is extremely restrictive for expressing
    analysis.  Any talk of limits is, in particular, problematic.  Many
    interesting parts of calculus can be reconstructed on algebraic
    grounds, but the usual approach to calculus and analysis is
    completely missed by the first-order theory.  When you are finished,
    you can check your answers against the Saylor
    Foundation’s [“Solutions for Exercises in Unit 1 – Exercise
    3.3.4”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.3.3.pdf) (PDF).  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.4 Compactness** <span id="1.4"></span> 
**1.4.1 Consistency** <span id="1.4.1"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Chapter 4 Introduction and Section 4.1”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Chapter 4 Introduction and Section
    4.1”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read from the beginning of Chapter 4 through
    the end of section 4.1.  Don’t be put off by the “How not to read
    this chapter” paragraph.  Zambella’s advice on skipping the Henkin
    proof is reasonable enough for the pure model theorist, but for the
    present course, where we intend eventually to understand
    computation, this proof is important: it is a proof by induction,
    but one in which we must order the stages carefully in order to
    finish in a finite time.  Such constructions are at the heart of
    computability.  As usual, try to think of examples and near-misses
    for the definitions.  
      
     This reading should take approximately 2 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.4.2 Compactness** <span id="1.4.2"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 4.2”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    4.2”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read all of section 4.2, solving the in-text
    exercises as you come to them.  Compactness is, in an important
    sense, the combinatorial heart of model theory, and the interaction
    between partial isomorphisms and compactness accounts for much of
    the discipline.  If you have heard mention of compactness in
    mathematics before, perhaps in analysis or topology, the notion is
    exactly the same (and, in fact, the Compactness Theorem in model
    theory can be taken as the statement that a certain topological
    space is compact).  The proofs are technical but important.  When
    you are finished, you can check your answers against the Saylor
    Foundation’s [“Solutions for Exercises in Unit 1 – Exercise 4.2.8
    and
    4.2.9”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.4.2.pdf)
    (PDF).  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.

**1.4.3 Monster Models** <span id="1.4.3"></span> 
-   **Reading: Università di Torino: Domenico Zambella’s A Crèchet
    Course in Model Theory: “Section 4.3”**
    Link: Università di Torino: Domenico Zambella’s *A Crèchet Course in
    Model Theory*: [“Section
    4.3”](http://www.dm.unito.it/personalpages/zambella/papers/creche/) (PDF
    or PS)  
      
     Instructions: Click on the link to the PDF or PS version of any
    version of the text.  Read all of section 4.3, solving the in-text
    exercise as you come to it.  You could think of the complex numbers
    as being the example that motivates monster models.  In the complex
    numbers, we have solutions to every polynomial equation we could
    ever think of, and so algebra can be done comfortably there – even
    if it is a bit bigger than the world we find “natural.”  A *monster
    model* is exactly that: an awkwardly big world in which we can
    comfortably find solutions to formulas.  When you are finished, you
    can check your answers against the Saylor Foundation’s [“Solutions
    for Exercises in Unit 1 – Exercise
    4.3.10”](https://resources.saylor.org/archived/wp-content/uploads/2012/10/MA201-Solutions-1.4.3.pdf)
    (PDF).  
      
     This reading should take approximately 3 hours.  
      
     Terms of Use: Please respect the copyright and terms of use
    displayed on the webpage above.


