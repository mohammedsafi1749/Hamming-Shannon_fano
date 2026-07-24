# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
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
![WhatsApp Image 2025-09-01 at 12 33 13_a5dc81da](https://github.com/user-attachments/assets/17ddac48-1f60-4992-b789-681f5465a5a7)
![WhatsApp Image 2025-09-01 at 12 33 11_1388be16](https://github.com/user-attachments/assets/8ee3cd3e-b2a3-4bc3-8cff-d302c090fd6b)




# Output

<img width="1011" height="215" alt="image" src="https://github.com/user-attachments/assets/8dbde500-41ae-4914-a9f4-4848fcde70dc" />

# Results:

The Huffman and Shannon-Fano of the given statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} using python are verified.
