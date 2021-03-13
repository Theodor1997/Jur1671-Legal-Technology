Legal app Article 6 of the GDPR aimed at data controllers and/or processers. 

Non-expert algorithm, this is a student project.

  In making the algorithm I have tried to do as little interpretation as possible,
so as to avoid misinterpreting the rules laid down in the article.
Therfore the questions are often only slighly different than the actual legal text,
usually only different in the placent of the "is".
  This is a result of not being supposed to take into account other legal texts than 
Article 6. The structure of the decision tree is based on some interpretation, but
this is with a basis in the internal refrencing of the text and use of logical 
quantifiers ("and", "or", "If", "not"). 
  I have also taken into account that some questions should come earlier in the tree 
so as to give the user an answer as quickly as possible. Especially questions that 
do not have followup questions(branches), have been put higher up in the decision 
tree.


  The decision tree/model looks like this : 

						a
					      /   \
					     d <-4- a'
					   /  \	     \
				     b v b'    P       P
					/   \
				     1.2     P
				     / \   
				   f    (if "yes", goes to 'c v e')
				 /   \
			    c v e <-- f'
			     /   \     /
			   -P     Q   P

	a,a',d,b,b',1.2,...= questions 
	P = Legal					/ = if no/false		
	- = not						\ = if yes/true
	Q = undecided					v = or
	<-4- = if no/false arrow, with 'advice'
	<-- = if yes/true arrow


  On the analysis of the legal text

  I started out with copying and pasting the legal text into a MicrosoftOffice 
Notebook-page, and then i split it into smaller pieces. Article 6 1) has a number of
points from a-f and I split these up and lined them up horizontally. The remaininder 
of art.6 sets up conditions for these points, some lead out of the article such as 
2) and 3), and to tackle this there is an "undecided"(Q) outcome. 
  I drew arrows from the these horizontally lined points to the other parts of the 
article that they related to and from this initial mapping i tried to approximate the 
logical structure. I used first order logic/truth functional logic(TF) to do this, 
which is the simplest form of logic. Allthough I did consider deontic modal logic,
which is highly relevant to the legal field, but it would have been too complex for
me as I dont yet have a firm grasp on this type of logic. 
  There are 6 outcomes in this model, four Ps(legal), one Q(undecided) and one 
-P(not legal),these are implied by a some premises, the sum of which makes up the 
logical structure of the model.

  As you may see in the model above there are some "branches" which means that 
followup questions are required in order to decide whether the law applies or not.
To code these branches I have made separate functions that gives a boolean value
(True/False) as output. This output from the "branch"-functions are then used to 
decide wether the main function/ the stem of the tree, which is a while-loop, should break 
or not. ¨




