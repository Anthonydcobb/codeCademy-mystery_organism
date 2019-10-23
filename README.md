# codeCademy-mystery_organism
function that creates an organism with random DNA sequence and matching mRNA sequence.

Mysterious Organism
Use your knowledge of objects to create models of deep-sea organisms for scientists to study.

Tasks

Prerequisites
1.
In order to complete this project, you should have completed the first few sections of Introduction to JavaScript (through Learn JavaScript: Objects).

Project Requirements
2.
Look over the starter code. There are two helper functions: returnRandBase() and mockUpStrand().

DNA is comprised of four bases (Adenine, Thymine, Cytosine, and Guanine). When returnRandBase() is called, it will randomly select a base and return the base ('A','T','C', or 'G').

mockUpStrand() is used to generate a single DNA strand that is 15 bases long.

You’ll use these helper functions later to create your objects that represent P. aequor.

3.
Since you need to create multiple objects, create a factory function pAequorFactory() that has two parameters:

The first parameter is number (no two organisms should have the same number)
The second parameter is a 15 base DNA sequence.
pAequorFactor() should return an object that contains the properties specimenNum and dna that correspond to the parameters provided.

You’ll also add more methods to this returned object in the later steps.

4.
Your team wants you to simulate P. aequor‘s high rate of mutation (change in its DNA).

To simulate a mutation, in pAequorFactory()‘s returned object, add the method .mutate().

.mutate() is responsible for randomly selecting a base in the object’s dna property and changing the current base to a different base. Then .mutate() will return the object’s dna.

For example, if the randomly selected base is the 1st base and it is 'A', the base must be changed to 'T', 'C', or 'G'. But it cannot be 'A' again.

5.
Your research team wants to be able to compare the DNA sequences of different P. aequor. You’ll have to add a new method (.compareDNA()) to the returned object of the factory function.

.compareDNA() has one parameter, another pAequor object.

The behavior of .compareDNA() is to compare the current pAequor‘s .dna with the passed in pAequor‘s .dna and compute how many bases are identical and in the same locations. .compareDNA() does not return anything, but prints a message that states the percentage of DNA the two objects have in common.

For example:

ex1 = ['A', 'C', 'T', 'G']
ex2 = ['C', 'A', 'T', 'T']
ex1 and ex2 only have the 3rd element in common ('T') and therefore, only 25% (1/4) of their DNA in common. The resulting message would read something along the lines of: ex1 and ex2 have 25% DNA in common.

6.
P. aequor have a likelier chance of survival if their DNA is made up of at least 60% 'C' or 'G' bases.

In the returned object of pAequorFactory(), add another method .willLikelySurvive().

This method returns true if the object has at least 60% of its .dna be either 'C' or 'G' bases. Otherwise, it returns false.

7.
With the factory function set up, your team requests that you create 30 instances of pAequor that can survive in their natural environment. Store these instances in an array for your team to study later.

Project Extensions & Solution
8.
Great work! If you’d like, you can compare your project to our solution code. Your solution might not look exactly like ours, and that’s okay! The most important thing is to get the correct answers for now.

9.
If you’d like to challenge yourself further, you could consider the following:

Create a .transcribe() method to the factory function’s object that returns the match RNA sequence of the object’s dna.
Use the RNA sequence to see what protein is translated.
Use the .compareDNA() to see if there’s one instance of pAequor that is most related to the other instances of pAequor.
