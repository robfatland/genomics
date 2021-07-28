This notebook should open and run in [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/robfatland/genomics/HEAD)



# genomics and bioinformatics


This repository is worked problems from [Rosalind project](http://rosalind.info/about/). Rosalind is a
platform for learning bioinformatics through problem solving. 


I am paying particular attention to the "text book track" problems. These are a connected series of problems
that begin with the introduction of hidden Markov models ("HMM").  



### Notes from correspondence with a student

A good first step for any problem is to run through the list of "what is provided to us" to try and understand what each one means. 
For example for problem BA10B, the *string x* is simple enough: We know what strings are. I do think they should not have labeled it "x" since "x" 
is in the *alphabet*. And the *alphabet* comes next; it is simply the elements we might find in the string. So: x, y and z are what can appear in the string.
The *hidden path* is like a *string*. However in Markov theory it is supposed to be "something we cannot see". So they say it is hidden. But it is going 
to influence what the *string* looks like by means of some probabilities. So the *hidden path* consists of a sequence of *states*. 
The *states* must be either *A* or *B*. If the *state* is *A* then a new letter from the
*alphabet* will be added to the *string* 
according to three probabilities: There is a 0.612 probability that 'x' will be added. 'y' has probability .314 and 'z' has probability .074.
Likewise if the state is *B*.
And so on across the entire hidden path (sequence of *states*). The connecting probabilities are provided in the *Emission Matrix*.


Now that we have had a look at what is provided we can turn to what it is we are supposed to figure out. Ideally we were thorough 
in the first part and the second part is pretty obvious as a result. 


Here, by the way, is the Hidden Markov Model (HMM) idea: There is a sequence we can see (which has three possible values 
at each point in the sequence); 
and there is something we can't see so it is *hidden* (which in this case has two possible state values at each point). And they are
connected by a probabilistic mechanism. What we *can* see is determined by what is *hidden* and we are trying to learn the rules of 
the hidden thing by looking at the thing we can see. 

