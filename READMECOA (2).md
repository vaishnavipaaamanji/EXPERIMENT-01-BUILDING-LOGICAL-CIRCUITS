# EXPERIMENT-01: BUILDING LOGICAL CIRCUITS

## Name : VAISNAVI
## Register Number : RA2511030010325

## 1. Aim

To design, implement, simplify, and verify combinational logic circuits using Boolean algebra and digital logic gates.

## 2. Boolean Notation

Use the following notation throughout this experiment:

| Symbol | Meaning | Example |
|---|---|---|
| `!A` | NOT A | `!A` |
| `A & B` | AND | `A & B` |
| `A \| B` | OR | `A \| B` |
| `A ^ B` | XOR | `A ^ B` |
| `A XNOR B` | XNOR | `A XNOR B` |

**Important:** In these equations, `!` means NOT, `&` means AND, `|` means OR, and `^` means XOR. Parentheses determine the order of operations.

## 3. Advanced Boolean Equations

### Equation 1: Four-Input Sum-of-Products

```text
F1 = (!A & B & C)
   | (A & B & !D)
   | (!B & C & D)
   | (A & !C & D)
```

**Inputs:** A, B, C, D  
**Output:** F1  
**Challenge:** Simplify the expression and compare gate counts.

<img width="1247" height="726" alt="Screenshot 2026-10-27 at 2 08 39 PM" src="https://github.com/user-attachments/assets/9c88aa00-eb84-4c9d-a3b4-1df19f5deb8a" />


### Equation 2: Product-of-Sums Circuit

```text
F2 = (A | !B | C)
   & (!A | B | D)
   & (B | !C | !D)
```

**Inputs:** A, B, C, D  
**Output:** F2  
**Challenge:** Implement the circuit using NAND gates and verify functional equivalence.

<img width="1600" height="881" alt="WhatsApp Image 2026-10-27 at 2 21 46 PM" src="https://github.com/user-attachments/assets/554f99ce-d55f-413f-af32-56938bd142e9" />


### Equation 3: Nested Complement Logic

```text
F3 = !(
       ((! (A | B)) | (C & D))
       &
       (A | (!(B | C)))
     )
```

**Inputs:** A, B, C, D  
**Output:** F3  
**Challenge:** Apply De Morgan's theorems and implement the circuit using NAND and NOR gates.

<img width="1075" height="672" alt="WhatsApp Image 2026-10-27 at 2 28 05 PM" src="https://github.com/user-attachments/assets/84848645-d452-4ee2-b63e-1a7858ecb69b" />


### Equation 4: XOR-XNOR Combinational Circuit

```text
F4 = ((A XOR B) & (C XNOR D))
   | (!A & B & (C XOR D))
```

**Inputs:** A, B, C, D  
**Output:** F4  
**Challenge:** Compare an XOR/XNOR implementation with a basic-gate implementation.

<img width="1073" height="572" alt="WhatsApp Image 2026-10-27 at 2 26 44 PM" src="https://github.com/user-attachments/assets/c21f6ccd-7911-47a9-86dc-6ab5763df564" />



### Equation 5: Five-Input Logic Function

```text
F5 = (A & B & !C)
   | (!A & D & E)
   | (B & C & !E)
   | (!B & C & D)
```

**Inputs:** A, B, C, D, E  
**Output:** F5  
**Challenge:** Generate and verify all 32 input combinations.

### Equation 6: Six-Input Mixed Logic

```text
F6 = ((A | B) & !(C | D))
   | ((C XOR E) & (D | G))
   | (!A & B & E)
```

**Inputs:** A, B, C, D, E, G  
**Output:** F6  
**Challenge:** Calculate gate count and logic depth. Verify all 64 input combinations.

### Equation 7: NAND-NOR Hybrid Logic

```text
F7 = (! (A & B) & !(C | D))
   | (!(A | C) & B & D)
```

**Inputs:** A, B, C, D  
**Output:** F7  
**Challenge:** Implement the function using NAND and NOR gates with any required input inversions.

### Equation 8: Six-Input Advanced Combinational Logic

```text
F8 = ((A XOR B) & (C XNOR D))
   | (!(A | B) & C & E)
   | (A & B & !(D | F))
```

**Inputs:** A, B, C, D, E, F  
**Output:** F8  
**Challenge:** Simplify the expression, design the circuit, and verify all 64 input combinations.

## 4. Experimental Procedure

1. Identify all input variables and the output.
2. Draw the logic circuit for each equation.
3. Implement the circuit in Logisim Evolution, Proteus, or a digital logic trainer kit.
4. Apply all possible input combinations.
5. Record the expected and observed outputs.
6. Simplify the Boolean expression using Boolean algebra.
7. Build the simplified circuit and compare gate counts.
8. Save the circuit diagrams, truth tables, and verification screenshots.

## 5. Truth Table Requirements

| Number of inputs | Required combinations |
|---:|---:|
| 4 | 16 |
| 5 | 32 |
| 6 | 64 |

Use this format to record the results:

| Inputs | Expected output | Observed output | Status |
|---|---|---|---|
| 0000 |  |  |  |
| 0001 |  |  |  |
| 0010 |  |  |  |
| ... |  |  |  |

Extend the table to include every input combination required by each equation.

## 6. Performance Analysis

For each circuit, record:

- Number of AND gates
- Number of OR gates
- Number of NOT gates
- Number of XOR/XNOR gates
- Total gate count
- Logic depth
- Functional equivalence before and after simplification

## 7. Expected Results

The eight Boolean functions should be implemented successfully. Their outputs should match the theoretical truth tables for all input combinations.

## 8. Result

The logic circuits are designed, implemented, and verified using Boolean algebra and digital logic gates. The original and simplified circuits are compared based on gate count and logic depth.

## 9. Repository Structure

```text
EXPERIMENT-01-BUILDING-LOGICAL-CIRCUITS/
├── README.md
├── circuit_diagrams/
├── truth_tables/
├── simulation_files/
└── results/
```

## 10. Viva Questions

1. What are universal logic gates?
   Universal logic gates are gates that can be used to implement any Boolean function.
* NAND gate
* NOR gate
2. State De Morgan's theorems.
  De Morgan’s theorems are:
1. First theorem: (A · B)’ = A’ + B’
2. Second theorem: (A + B)’ = A’ · B’
3. What is the difference between SOP and POS?
     SOP vs POS: SOP means Sum of Products (AND-OR), whereas POS means Product of Sums (OR-AND).
4. How does XOR differ from XNOR?
       XOR vs XNOR: XOR gives output 1 when inputs are different, whereas XNOR gives output 1 when inputs are the same.
5. How can Boolean expressions be simplified?
   Boolean Simplification: Boolean expressions can be simplified using Boolean algebra laws, De Morgan’s theorems and K-maps.
6. How many truth-table rows are required for six inputs?
       Truth Table for Six Inputs: 2⁶ = 64 rows.
9. What is logic depth?
        Logic Depth: Logic depth is the maximum number of logic gate levels between input and output.
11. Why is functional verification necessary?
        Functional Verification: It ensures that the circuit works correctly according to its design specifications and detects errors.
