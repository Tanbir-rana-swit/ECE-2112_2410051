
## **Lab 1: Introduction to Digital Logic**
## **Experiment 1: Implementation of OR Gate using NOR Gates**

**Description:**\
In this experiment, we will implement an OR gate using only NOR gates. The OR gate is a fundamental digital logic gate that outputs true (1) when at least one of its inputs is true (1). The NOR gate, on the other hand, is a universal gate that can be used to create any other logic gate, including the OR gate.

**Procedure:**
1. **Understanding the NOR Gate:**
   - A NOR gate is a combination of an OR gate followed by a NOT gate. It outputs true (0) only when all its inputs are false (0).
   - The truth table for a 2-input NOR gate is as follows:

   | Input A | Input B | Output (A NOR B) |
   |---------|---------|------------------|
   |    0    |    0    |         1        |
   |    0    |    1    |         0        |
   |    1    |    0    |         0        |
   |    1    |    1    |         0        |

2. **Implementing the OR Gate using NOR Gates:**
   - To implement an OR gate using NOR gates, we can use the following logic:
   - The OR gate can be expressed in terms of NOR gates as follows:
   - OR(A, B) = NOT(NOR(A, B))
   - This means that we can first use a NOR gate to get the output of NOR(A , B), and then use another NOR gate to invert that output.  

3. **Circuit Design:**
   - Connect the inputs A and B to the first NOR gate.
   - <img width="618" height="343" alt="image" src="https://github.com/user-attachments/assets/c45f5e8c-69e3-4d17-a120-63056a1a0e90" />

   - Connect the output of the first NOR gate to both inputs of the second NOR gate to invert the output.
      <img width="993" height="347" alt="image" src="https://github.com/user-attachments/assets/c500e48a-e8ed-452d-94b5-b219184b7a72" />



4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an OR gate.
 <img width="1007" height="400" alt="image" src="https://github.com/user-attachments/assets/b5e4f95a-1cf8-4f3e-bba6-dd6246eb5afe" />
  <img width="1013" height="428" alt="image" src="https://github.com/user-attachments/assets/2a26ae7f-7ae3-4ec6-a0bf-ffa80838d873" />


**Conclusion:**
In this experiment, we successfully implemented an OR gate using only NOR gates. By understanding the properties of NOR gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 2: Implementation of OR Gate using NAND Gates**

**Description:**\
In this experiment, we will implement an OR gate using only NAND gates. The NAND gate is another universal gate that can be used to create any other logic gate, including the OR gate.

**Procedure:**
1. **Understanding the NAND Gate:**
   - A NAND gate is a combination of an AND gate followed by a NOT gate. It outputs false (0) only when all its inputs are true (1).
   - The truth table for a 2-input NAND gate is as follows:
   
   | Input A | Input B | Output (A NAND B) |
   |---------|---------|-------------------|
   |    0    |    0    |        1          |
   |    0    |    1    |        1          |
   |    1    |    0    |        1          |
   |    1    |    1    |        0          |

2. **Implementing the OR Gate using NAND Gates:**
   - To implement an OR gate using NAND gates, we can use the following logic:
   - OR(A, B) = NOT(NAND(NOT(A), NOT(B)))
   - This means that we can first use two NAND gates to invert the inputs A and B, and then use a third NAND gate to combine the inverted inputs.
3. **Circuit Design:**
   - Connect the inputs A and B to the first two NAND gates to invert them.
   <img width="509" height="341" alt="image" src="https://github.com/user-attachments/assets/1c10b7c1-fa0f-4786-be0b-d5ea69a2eea9" />


    - Connect the outputs of the first two NAND gates to the inputs of the third NAND gate to get the final output.
    <img width="877" height="369" alt="image" src="https://github.com/user-attachments/assets/40530aac-616a-4d4c-9e24-011c982ded27" />


4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an OR gate.

   <img width="961" height="376" alt="image" src="https://github.com/user-attachments/assets/87b15653-2a17-4bc4-b851-5976cefcf6ad" />
<img width="910" height="367" alt="image" src="https://github.com/user-attachments/assets/b0f63569-8b78-4cf5-8fd0-47748a93174d" />



**Conclusion:**
   In this experiment, we successfully implemented an OR gate using only NAND gates. By understanding the properties of NAND gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 3: Implementation of AND Gate using NOR Gates**

**Description:**\
In this experiment, we will implement an AND gate using only NOR gates. The AND gate is a fundamental digital logic gate that outputs true (1) only when both of its inputs are true (1). The NOR gate, being a universal gate, can be used to create an AND gate as well.

**Procedure:**
1. **Understanding the AND Gate:**
   - An AND gate outputs true (1) only when both of its inputs are true (1). The truth table for a 2-input AND gate is as follows:

   | Input A | Input B | Output (A AND B) |
   |---------|---------|-------------------|
   |    0    |    0    |        0          |
   |    0    |    1    |        0          |
   |    1    |    0    |        0          |
   |    1    |    1    |        1          |

2. **Implementing the AND Gate using NOR Gates:**
   - To implement an AND gate using NOR gates, we can use the following logic:
   - AND(A, B) = NOT(NOR(NOT(A), NOT(B)))
   - This means that we can first use two NOR gates to invert the inputs A and B, and then use a third NOR gate to combine the inverted inputs.

3. **Circuit Design:**
   - Connect the inputs A and B to the first two NOR gates to invert them.
   <img width="540" height="370" alt="image" src="https://github.com/user-attachments/assets/a1f025b0-2166-4ed0-9090-d37e4d8781dd" />

    - Connect the outputs of the first two NOR gates to the inputs of the third NOR gate to get the final output.
    <img width="934" height="388" alt="image" src="https://github.com/user-attachments/assets/ecff9d3c-fe85-416a-a8e3-44af13750d63" />


4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an AND gate.
  <img width="928" height="378" alt="image" src="https://github.com/user-attachments/assets/acab20fd-6ed7-4b96-a55f-d733c2d8328b" />
<img width="856" height="372" alt="image" src="https://github.com/user-attachments/assets/0f1d2e22-8a16-4ce4-9543-65014156b3c9" />


**Conclusion:**
In this experiment, we successfully implemented an AND gate using only NOR gates. By understanding the properties of NOR gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.

## **Experiment 4: Implementation of AND Gate using NAND Gates**

**Description:**\
In this experiment, we will implement an AND gate using only NAND gates. The NAND gate is a universal gate that can be used to create any other logic gate, including the AND gate.

**Procedure:**
1. **Understanding the AND Gate:**
   - An AND gate outputs true (1) only when both of its inputs are true (1). The truth table for a 2-input AND gate is as follows:

    | Input A | Input B | Output (A AND B) |
    |---------|---------|-------------------|
    |    0    |    0    |        0          |
    |    0    |    1    |        0          |
    |    1    |    0    |        0          |
    |    1    |    1    |        1          |


2. **Implementing the AND Gate using NAND Gates:**
   - To implement an AND gate using NAND gates, we can use the following logic:
   - AND(A, B) = NOT(NAND(A, B))
   - This means that we can first use a NAND gate to get the output of NAND(A, B), and then use another NAND gate to invert that output.

3. **Circuit Design:**
   - Connect the inputs A and B to the first NAND gate.
   
    - Connect the output of the first NAND gate to both inputs of the second NAND gate to invert the output.
    <img width="700" height="371" alt="image" src="https://github.com/user-attachments/assets/c5cc1977-7c56-47d6-b7bb-b71d1956b84e" />


4. **Testing the Circuit:**
   - Apply different combinations of inputs (A and B) to the circuit and observe the output.
   - Verify that the output matches the expected results of an AND gate.
   <img width="731" height="341" alt="image" src="https://github.com/user-attachments/assets/8fb17cb9-2dda-428a-be68-bcbfc94a04c3" />
   <img width="744" height="389" alt="image" src="https://github.com/user-attachments/assets/de2ce149-13ad-417b-803a-ee5c7b94a572" />


**Conclusion:**
In this experiment, we successfully implemented an AND gate using only NAND gates. By understanding the properties of NAND gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.

## **Experiment 5: Implementation of NOT Gate using NOR Gates**


**Description:**\
In this experiment, we will implement a NOT gate using only NOR gates. The NOT gate is a fundamental digital logic gate that outputs the opposite value of its input. The NOR gate, being a universal gate, can be used to create a NOT gate as well.

**Procedure:**
1. **Understanding the NOT Gate:**
   - A NOT gate outputs true (1) when its input is false (0) and outputs false (0) when its input is true (1). The truth table for a NOT gate is as follows:

   | Input A | Output (NOT A) |
   |---------|----------------|
   |    0    |        1       |
   |    1    |        0       |

2. **Implementing the NOT Gate using NOR Gates:**
   - To implement a NOT gate using NOR gates, we can use the following logic:
   - NOT(A) = NOR(A, A)
   - This means that we can connect the input A to both inputs of a NOR gate to get the inverted output.

3. **Circuit Design:**
   - Connect the input A to both inputs of the NOR gate.
   <img width="573" height="289" alt="image" src="https://github.com/user-attachments/assets/8761b646-c1a3-4ec2-bea1-e738005fa062" />


4. **Testing the Circuit:**
   - Apply different values of input A to the circuit and observe the output.
   - Verify that the output matches the expected results of a NOT gate.

   <img width="573" height="289" alt="image" src="https://github.com/user-attachments/assets/cc90de90-0d2f-4078-ae89-86439269239e" />
   <img width="546" height="296" alt="image" src="https://github.com/user-attachments/assets/90e7d2f3-12ad-4163-822e-379b0009c03f" />



**Conclusion:**
In this experiment, we successfully implemented a NOT gate using only NOR gates. By understanding the properties of NOR gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 6: Implementation of NOT Gate using NAND Gates**

**Description:**\
In this experiment, we will implement a NOT gate using only NAND gates. The NOT gate is a fundamental digital logic gate that outputs the opposite value of its input. The NAND gate, being a universal gate, can be used to create a NOT gate as well.

**Procedure:**
1. **Understanding the NOT Gate:**
   - A NOT gate outputs true (1) when its input is false (0) and outputs false (0) when its input is true (1). The truth table for a NOT gate is as follows:

   | Input A | Output (NOT A) |
   |---------|----------------|
   |    0    |        1       |
   |    1    |        0       |

2. **Implementing the NOT Gate using NAND Gates:**
   - To implement a NOT gate using NAND gates, we can use the following logic:
   - NOT(A) = NAND(A, A)
   - This means that we can connect the input A to both inputs of a NAND gate to get the inverted output.

3. **Circuit Design:**
   - Connect the input A to both inputs of the NAND gate.

   <img width="566" height="254" alt="image" src="https://github.com/user-attachments/assets/e6647755-6f88-4d8b-8641-0b0f2b65a5fb" />
   


4. **Testing the Circuit:**
   - Apply different values of input A to the circuit and observe the output.
   - Verify that the output matches the expected results of a NOT gate.

  <img width="566" height="254" alt="image" src="https://github.com/user-attachments/assets/5228ad45-af7b-4d3c-8cb3-2a64e786e0c5" />
<img width="557" height="250" alt="image" src="https://github.com/user-attachments/assets/806379c1-652c-4af4-93b0-458c87c88663" />


**Conclusion:**
In this experiment, we successfully implemented a NOT gate using only NAND gates. By understanding the properties of NAND gates and their ability to create other logic gates, we were able to demonstrate the versatility of digital logic design. This exercise reinforces the concept of universal gates and their applications in digital circuits.


## **Experiment 7: Implementation of Full Adder and testing it.**

**Description:**\
In this experiment, we will implement a Full Adder circuit using basic logic gates. A Full Adder is a digital circuit that performs the addition of three binary bits: two significant bits and a carry bit. The Full Adder produces a sum and a carry output.

**Procedure:**
1. **Understanding the Full Adder:**
   - A Full Adder takes three inputs: A, B, and Cin (carry input). It produces two outputs: Sum and Cout (carry output). The truth table for a Full Adder is as follows:

   | Input A | Input B | Cin | Sum | Cout |
   |---------|---------|-----|-----|------|
   |    0    |    0    |  0  |  0  |  0   |
   |    0    |    0    |  1  |  1  |  0   |
   |    0    |    1    |  0  |  1  |  0   |
   |    0    |    1    |  1  |  0  |  1   |
   |    1    |    0    |  0  |  1  |  0   |
   |    1    |    0    |  1  |  0  |  1   |
   |    1    |    1    |  0  |  0  |  1   |
   |    1    |    1    |  1  |  1  |  1   |

2. **Implementing the Full Adder Circuit:**
   - The Full Adder can be implemented using two Half Adders and an OR gate.
   - The first Half Adder takes inputs A and B and produces a sum (S1) and a carry (C1).
   - The second Half Adder takes the sum (S1) from the first Half Adder and the carry input (Cin) to produce the final sum (Sum) and a carry (C2).
   - The final carry output (Cout) is obtained by ORing the two carry outputs (C1 and C2) from the two Half Adders.

3. **Circuit Design:**
   
   <img width="653" height="354" alt="image" src="https://github.com/user-attachments/assets/281950a5-c659-47b5-9460-7bc4b90f7fc6" />


5. **Testing the Circuit:**
   - Apply different combinations of inputs (A, B, and Cin) to the circuit and observe the outputs (Sum and Cout).
   - Verify that the outputs match the expected results of a Full Adder.
   <img width="725" height="379" alt="image" src="https://github.com/user-attachments/assets/0df7e7c9-c53c-40a9-887c-71e574792b74" />
   <img width="663" height="340" alt="image" src="https://github.com/user-attachments/assets/51035cf7-5b41-4dfe-ad1d-ee55288da36b" />
   <img width="662" height="376" alt="image" src="https://github.com/user-attachments/assets/458067a7-2939-4ed9-ada2-debd7d25b23a" />
<img width="692" height="366" alt="image" src="https://github.com/user-attachments/assets/0bf3c86e-d798-4035-ac1a-13dc5387101b" />

**Conclusion:**
In this experiment, we successfully implemented a Full Adder circuit using basic logic gates. By understanding the properties of Half Adders and their combination to form a Full Adder, we were able to demonstrate the addition of binary numbers. This exercise reinforces the concept of digital arithmetic and its applications in digital circuits. The Full Adder is a crucial component in the design of arithmetic logic units (ALUs) and other digital systems that require binary addition.


## **Experiment 8: Implementation of Binary to BCD Converter**

**Description:**\
In this experiment, we will implement a Binary to BCD (Binary-Coded Decimal) converter using basic logic gates. A Binary to BCD converter is a digital circuit that converts a binary number into its equivalent BCD representation. BCD is a form of decimal representation where each digit of a decimal number is represented by its binary equivalent.

**Procedure:**
1. **Understanding Binary to BCD Conversion:**
   - A Binary to BCD converter takes a binary input and produces a BCD output.
   - For example, the binary number 1010 (which is 10 in decimal) can be represented in BCD as 0001 0000 (1 and 0 in BCD).
   - The truth table for a 4-bit binary input and its corresponding BCD output is as follows:

| Binary Code |   |   |   | BCD Code |   |   |   |
|:-----------:|:-:|:-:|:-:|:--------:|:-:|:-:|:-:|
| B₃ | B₂ | B₁ | B₀ | D₄ | D₃ | D₂ | D₁ |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 1 | 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 0 | 0 | 0 | 1 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 1 | 1 | 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 0 | 1 | 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 | 1 | 1 | 1 | 0 |
| 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |

2. **Implementing the Binary to BCD Converter Circuit:**
   - The Binary to BCD converter can be implemented using a combination of logic gates to map the binary inputs to their corresponding BCD outputs.
   - The circuit design will involve creating logic expressions for each BCD output bit (D₄, D₃, D₂, D₁) which will be displayed on the BCD to seven-segment display based on the binary input bits (B₃, B₂, B₁, B₀).

3. **Circuit Design:**
  <img width="582" height="254" alt="image" src="https://github.com/user-attachments/assets/46fa12a2-6da9-480b-8c32-7e7fa371499d" />

4. **Testing the Circuit:**
   - Apply different combinations of binary inputs (B₃, B₂, B₁, B₀) to the circuit and observe the BCD outputs (D₄, D₃, D₂, D₁).
   - Verify that the outputs match the expected results of the Binary to BCD conversion.
   !<img width="582" height="254" alt="image" src="https://github.com/user-attachments/assets/c11082e5-e660-41f3-b28f-73bc619f6573" />
<img width="656" height="302" alt="image" src="https://github.com/user-attachments/assets/3a845e05-463a-40a0-a522-4d0bb1d8d237" />
<img width="655" height="275" alt="image" src="https://github.com/user-attachments/assets/d7aea595-b42d-430b-8314-22d92d1f60a3" />


**Conclusion:**
In this experiment, we successfully implemented a Binary to BCD converter using basic logic gates. By understanding the properties of binary numbers and their corresponding BCD representations, we were able to demonstrate the conversion process. This exercise reinforces the concept of digital number systems and their applications in digital circuits, particularly in systems that require decimal representation of binary numbers, such as digital displays and calculators.

