# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.45,0.35,0.2} for its output. 
Apply the Huffman and Shannon-Fano to this source. Show that draw the tree diagram, the average code word length, Entropy, Variance, Redundancy, Efficiency.
# Tools Required:
Python IDE with Numpy and Scipy.

# Program:
```
import math
# Probabilities given
p = [0.45,0.35,0.2]
# Corresponding Huffman/Shannon-Fano code lengths
lk = [1,2,2]
n = len(p)
# Average Codeword Length
L = sum(p[k] * lk[k]
for k in range(n))
# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2)
 for k in range(n))
hs = round(hs, 3)
# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)
# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2
for k in range(n))
var = round(var, 3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
# Calculation:

<img width="729" height="1280" alt="image" src="https://github.com/user-attachments/assets/b347aaf8-bbec-4664-bb64-471605704f91" />

<img width="834" height="1280" alt="image" src="https://github.com/user-attachments/assets/8c806288-beca-489c-ae60-f959517fa969" />

# Output

<img width="1011" height="215" alt="image" src="https://github.com/user-attachments/assets/8dbde500-41ae-4914-a9f4-4848fcde70dc" />

# Results:

The Huffman and Shannon-Fano of the given statistics {0.45,0.35,0.2} using python are verified.
