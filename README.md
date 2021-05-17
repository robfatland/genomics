# genomics
Inspired by the Rosalind project. 

Here is a solution to the Textbook track [problem BA10A](http://rosalind.info/problems/ba10a/).

```
# Hidden Markov Model problem
# The probability of the initial 'A' or 'B' is equal, so the lead
# factor is 1/2. Thereafter the probabilities are given by a transition matrix.

# solve for the probability of...
path = 'AABBBAABABAAAABBBBAABBABABBBAABBAAAABABAABBABABBAB'

probability = 0.5

for i in range(0, len(path)-1):
    if path[i] == 'A': probability *= .194 if path[i+1] == 'A' else .806
    else:              probability *= .273 if path[i+1] == 'A' else .727

print(probability)
```
