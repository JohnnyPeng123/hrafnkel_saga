# hrafnkel_saga
View this visualization from the link below:
https://htmlpreview.github.io/?https://github.com/JohnnyPeng123/hrafnkel_saga/main/index.html

Data Source:

http://mozart.diei.unipg.it/gdcontest/contest2020/topics.html

![alt text](https://github.com/JohnnyPeng123/hrafnkel_saga/blob/main/screen-shot.PNG?raw=true)

The implementation of the individual arc diagram in the graph was based on the codes from the link below:
https://observablehq.com/@d3/arc-diagram#chart

In addition, in order to create the visualization shown in the previous page, additional modifications including data preprocessing, createssmall multiples, varying the position of the arcs were done. 

The Hrafnkel Saga is one of the Icelanders’ sagas. The arc diagram from the previous page shows the interactions between
the characters in each chapter. There are 16 arc diagrams in this visualization, which are corresponding to the 16 chapters
of the saga.

There are seven main marks/elements in this visualization:
1. Black Bold Text under each arc diagram – This indicates the chapter the arc diagram above were based on.

2. Dots – The dots represent the characters that appeared in the indicated chapter.

3. Colour of the dots/texts – This indicates the gender of the character. colour indicates the character is a
male, colour means the character is a female, and colour indicates the character is non-human.

4. Text next to the dots – These are the names of the characters represented by the dots.

5. Arcs – This represents the directed relationship or actions happened between two characters.

6. Colour of the Arc – This represents the nature of the action. colour indicates the action or relationship is
Hostile. indicates the action or relationship is Friendly, and colour indicates the action or relationship
is Neutral. Note that, the original dataset come with 28 unique edge labels. I have manually grouped them into
hostile/friendly/neutral, the detail mapping table for each group can be found from the appendix.

7. Position of the Arc – This represent the direction of the arc. For arcs that is located on the left-hand side of the
dots, their source node is located above the target node, indicating a direction that goes from top to the bottom.
On the other hand, for arcs that is located on the right-hand side of the dots, their source node is located below
the target node, indicating a direction that goes from bottom to the top.
For example, the arcs in chapter 5 that goes from Hrafnkel to Einar indicates a hostile action done by Hrafnkel against
Einar. In chapter 5 of the original story, Hrafnkel truly killed Einar for riding his horse Feryfax. We can confirm this as Einar
did not appeared again in the later chapters. Note that, this arc diagram also indicates Hrafnkel is the most important
character in this chapter as the dots/nodes are sorted by degree.

# Self-evaluation

• (Strength) This visualization clearly shows most of the information given by the dataset at a very granular level,
and all chapters were shown in once, so it is able to answers the following important questions very well:

o Which characters were mentioned in chapter X? What is their gender? Which one of them is the most
important character in this chapter? How is their relationship in this chapter (hostile/friendly/neutral)?
What is the total number of chapters in this Saga?

• (Weakness) Not all the given information was presented in this visualization, and this visualization cannot answer
or directly answer some of the aggregation question. For Example:

o How many times has character X has been mentioned in this book? Who is the most important character
in this book? What is the exact action done by each character? At which chapter/page the character X
was first mentioned?

• (Weakness) When multiple actions were conducted by one character against another character in the same
chapter, multiple arcs will overlay on top of each other. This could lead to underestimate of the interaction
between two characters. In addition, this causes the multiple arc colour being mixed together, which creates
additional confusion for the reader.

• (Weakness) The nodes are simply sorted by degree, there is no aesthetic criteria like minimize edge crossing. Thus,
this visualization might not be optimal in terms of aesthetic.
