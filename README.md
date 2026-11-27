
# final.-









Here are all 7 Python programs extracted from your PDF, ready to copy and paste directly into GitHub or a Gist so you can easily search them later:
Assignment 1: Set Operations using Python
python
# NAME     :
# ROLL NO. :
# Assignment 1 : Set Operations using Python

# Step 2: Read two sets A and B
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

print("Set A:", A)
print("Set B:", B)

# Step 3: Union
union_set = A.union(B)
print("Union (A U B):", union_set)

# Step 4: Intersection
intersection_set = A.intersection(B)
print("Intersection (A n B):", intersection_set)

# Step 5: Difference (A - B)
difference_A_B = A.difference(B)
print("Difference (A - B):", difference_A_B)

# Step 6: Cartesian Product (A x B)
cartesian_product = [(x, y) for x in A for y in B]
print("Cartesian Product (A x B):", cartesian_product)
Use code with caution.
Assignment 2: Checking Relation Properties
python
# NAME     :
# ROLL NO. :
# Assignment 2 : Checking Relation Properties

# Step 2: Elements of set A
A = {1, 2, 3}

# Step 3: Ordered pairs of relation R
R = {(1, 1), (2, 2), (3, 3), (1, 2), (2, 1)}

# Step 4-5: Reflexive -> every (a,a) must be in R
reflexive = True
for a in A:
    if (a, a) not in R:
        reflexive = False

# Step 6-7: Symmetric -> for every (a,b), (b,a) must be in R
symmetric = True
for (a, b) in R:
    if (b, a) not in R:
        symmetric = False

# Step 8-9: Transitive -> (a,b) and (b,c) in R, then (a,c) in R
transitive = True
for (a, b) in R:
    for (c, d) in R:
        if b == c:
            if (a, d) not in R:
                transitive = False

# Step 10: Equivalence Relation -> all three properties are True
# Step 11: Display the results
print("Reflexive:", reflexive)
print("Symmetric:", symmetric)
print("Transitive:", transitive)

if reflexive and symmetric and transitive:
    print("The relation is an Equivalence Relation")
else:
    print("The relation is NOT an Equivalence Relation")
Use code with caution.
Assignment 3: Injective, Surjective and Bijective Functions
python
# NAME     :
# ROLL NO. :
# Assignment 3 : Injective, Surjective and Bijective Functions

# Step 2-4: Domain and Codomain
A = [1, 2, 3]
B = [2, 4, 6]

# Step 5: Image of each domain element
f = {1: 2, 2: 4, 3: 6}
images = list(f.values())

# Step 6: Injective -> all mapped values are distinct
if len(images) == len(set(images)):
    injective = True
else:
    injective = False

# Step 7: Surjective -> every codomain element is an image
surjective = True
for b in B:
    if b not in images:
        surjective = False

# Step 8: Bijective -> both Injective and Surjective
# Step 9: Display the results
print("Injective:", injective)
print("Surjective:", surjective)

if injective and surjective:
    print("The function is BIJECTIVE")
else:
    print("The function is NOT BIJECTIVE")
Use code with caution.
Assignment 4: Mean, Median and Mode
python
# NAME     :
# ROLL NO. :
# Assignment 4 : Mean, Median and Mode

# Step 2-3: Number of observations and data values
data = [10.0, 15.0, 20.0, 20.0, 25.0, 30.0]
n = len(data)

# Step 4: Mean
mean = sum(data) / n

# Step 5: Arrange data in ascending order
sorted_data = sorted(data)

# Step 6: Median
mid = n // 2
if n % 2 != 0:
    median = sorted_data[mid]
else:
    median = (sorted_data[mid - 1] + sorted_data[mid]) / 2

# Step 7: Count the frequency of each value
counts = {}
for item in data:
    counts[item] = counts.get(item, 0) + 1

# Step 8: Determine the Mode
max_freq = max(counts.values())
modes = []
for key in counts:
    if counts[key] == max_freq:
        modes.append(key)

# Step 9: Display Mean, Median and Mode
print("Dataset:", data)
print("Mean:", mean)
print("Median:", median)
if max_freq == 1:
    print("Mode: No mode")
else:
    print("Mode(s):", modes)
Use code with caution.
Assignment 5: Variance and Standard Deviation
python
# NAME     :
# ROLL NO. :
# Assignment 5 : Variance and Standard Deviation
import math

# Step 2-3: Number of observations and data values
data = [10.0, 12.0, 14.0, 16.0, 18.0]
n = len(data)

# Step 4: Mean
mean = sum(data) / n

# Step 5: Squared deviation of each observation from the mean
total = 0
for x in data:
    total = total + (x - mean) ** 2

# Step 6: Variance (population) = sum / N
variance = total / n

# Step 7: Standard Deviation = square root of variance
std_dev = math.sqrt(variance)

# Step 8: Display Mean, Variance and Standard Deviation
print("Dataset:", data)
print(f"Mean: {mean}")
print(f"Variance: {variance:.2f}")
print(f"Standard Deviation: {std_dev:.4f}")
Use code with caution.
Assignment 6: Probability of Events
python
# NAME     :
# ROLL NO. :
# Assignment 6 : Probability of drawing a Face Card

# Step 2: Total possible outcomes
total_cards = 52

# Step 3: Favorable outcomes (Jack, Queen, King in 4 suits)
suits = 4
face_cards_per_suit = 3
total_face_cards = face_cards_per_suit * suits

# Step 4: Check favorable <= total
if total_face_cards <= total_cards:
    # Step 5: P(E) = Favorable Outcomes / Total Outcomes
    prob_decimal = total_face_cards / total_cards
    prob_percentage = prob_decimal * 100

    print("--- Probability of Drawing a Face Card ---")
    print(f"Total Cards in Deck: {total_cards}")
    print(f"Total Face Cards: {total_face_cards}")
    print(f"Probability (Fraction): {total_face_cards}/{total_cards}")
    print(f"Probability (Decimal): {prob_decimal:.4f}")
    print(f"Probability (Percentage): {prob_percentage:.2f}%")
else:
    print("Invalid: favorable outcomes cannot exceed total outcomes")
Use code with caution.
Assignment 7: Gradient, Divergence and Curl
python
# NAME     :
# ROLL NO. :
# Assignment 7 : Gradient, Divergence and Curl
import sympy as sp

# Step 3: Define the variables
x, y, z = sp.symbols('x y z')

# ---------- 1. Gradient of phi = x^3 + y^3 + z^3 ----------
phi = x**3 + y**3 + z**3
grad_x = sp.diff(phi, x)
grad_y = sp.diff(phi, y)
grad_z = sp.diff(phi, z)
gradient = [grad_x, grad_y, grad_z]

print(f"Scalar function phi = {phi}")
print(f"Gradient of phi = {gradient}")

# ---------- 2. Divergence of F = (x^2, y^2, z^2) ----------
P = x**2
Q = y**2
R = z**2
divergence = sp.diff(P, x) + sp.diff(Q, y) + sp.diff(R, z)

print(f"\nVector field F = ({P}, {Q}, {R})")
print(f"Divergence of F = {divergence}")

# ---------- 3. Curl of F = (-y, x, 0) ----------
P = -y
Q = x
R = 0
curl_x = sp.diff(R, y) - sp.diff(Q, z)
curl_y = sp.diff(P, z) - sp.diff(R, x)
curl_z = sp.diff(Q, x) - sp.diff(P, y)
curl = (curl_x, curl_y, curl_z)

print(f"\nVector field F = ({P}, {Q}, {R})")
print(f"Curl of F = {curl}")
Use code with caution.
(Tip: On your phone, you can paste all 7 of these into a single GitHub Gist by clicking Add file at the bottom of the Gist editor for each assignment, like assignment1.py, assignment2.py, etc. No Desktop mode required!)
Would you like me to:
Combine all 7 into a single downloadable .py or .zip file for easy uploading
Walk you through saving them into a multi-file GitHub Gist on your phone
Let me know what works best!




Here are all 7 dynamic (user-input) Python programs extracted from your PDF, ready to copy and paste:
Assignment 1: Set Operations using Python
python
# NAME     :
# ROLL NO. :
# Assignment 1 : Set Operations using Python

# Step 2: Read two sets A and B from the user
A = set(map(int, input("Enter elements of A: ").split()))
B = set(map(int, input("Enter elements of B: ").split()))

print("\nSet A:", A)
print("Set B:", B)

# Step 3: Union
union_set = A.union(B)
print("Union (A U B):", union_set)

# Step 4: Intersection
intersection_set = A.intersection(B)
print("Intersection (A n B):", intersection_set)

# Step 5: Difference (A - B)
difference_A_B = A.difference(B)
print("Difference (A - B):", difference_A_B)

# Step 6: Cartesian Product (A x B)
cartesian_product = [(x, y) for x in A for y in B]
print("Cartesian Product (A x B):", cartesian_product)
Use code with caution.
Assignment 2: Checking Relation Properties
python
# NAME     :
# ROLL NO. :
# Assignment 2 : Checking Relation Properties

# Step 2: Read the elements of set A
A = set(map(int, input("Enter elements of A: ").split()))

# Step 3: Read the ordered pairs of relation R
R = set()
m = int(input("Enter number of ordered pairs in R: "))
for i in range(m):
    a, b = map(int, input("Enter pair (a b): ").split())
    R.add((a, b))

# Step 4-5: Reflexive -> every (a,a) must be in R
reflexive = True
for a in A:
    if (a, a) not in R:
        reflexive = False

# Step 6-7: Symmetric -> for every (a,b), (b,a) must be in R
symmetric = True
for (a, b) in R:
    if (b, a) not in R:
        symmetric = False

# Step 8-9: Transitive -> (a,b) and (b,c) in R, then (a,c) in R
transitive = True
for (a, b) in R:
    for (c, d) in R:
        if b == c:
            if (a, d) not in R:
                transitive = False

# Step 10-11: Equivalence Relation and display results
print("\nReflexive:", reflexive)
print("Symmetric:", symmetric)
print("Transitive:", transitive)

if reflexive and symmetric and transitive:
    print("The relation is an Equivalence Relation")
else:
    print("The relation is NOT an Equivalence Relation")
Use code with caution.
Assignment 3: Injective, Surjective and Bijective Functions
python
# NAME     :
# ROLL NO. :
# Assignment 3 : Injective, Surjective and Bijective Functions

# Step 2-3: Read the domain
A = list(map(int, input("Enter domain elements: ").split()))

# Step 4: Read the codomain
B = list(map(int, input("Enter codomain elements: ").split()))

# Step 5: Read the image of each domain element
f = {}
for x in A:
    f[x] = int(input(f"Enter image of {x}: "))

images = list(f.values())

# Step 6: Injective -> all mapped values are distinct
if len(images) == len(set(images)):
    injective = True
else:
    injective = False

# Step 7: Surjective -> every