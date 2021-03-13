No requirements

Non-expert algorithm, this is a student project.

The decision tree looks like this :
a,a'1,d,b,b'1,1.2,...= questions
P = Legal				/ = if no/false		
- = not					\ = if yes/true
Q = undecided				v = or
<-4- = if no/false arrow, with 'advice'
<-- = if yes/true arrow
 

						a
					      /   \
					     d <-4- a'1
					   /  \	     \
				    b v b'1    P       P
					/   \
				     1.2     P
				     / \   
				   f    (if 'yes' goes to 'c v e')
				 /   \
			    c v e <-- f'1
			     /   \     /
			   -P     Q   P

