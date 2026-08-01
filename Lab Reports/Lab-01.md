## **Lab 1: Getting Started with Digital Logic**

**Circuit File:** [Lab_1.circ](Lab_1.circ) — This Logisim Evolution project file contains all the circuits designed during this lab session.

## **Software Setup: Acquiring and Installing Logisim Evolution**

**Description:**
To design and test the circuits for this lab, we utilized Logisim Evolution, a free and open-source simulator for digital logic. The first step of the lab involved acquiring and setting up this software environment.

**Procedure:**
1. **Locating the source:**
   - A quick search for "logisim evolution download" directed us to the official Logisim Evolution GitHub repository.

     ![Searching for the Logisim Evolution download page](setup_1_search_download_page.png)

2. **Finding installation details:**
   - Reviewing the repository's README revealed pre-packaged installers for Windows, macOS, and Linux. These packages conveniently include a bundled Java runtime, eliminating the need to install Java separately. There are also instructions for building from source.

     ![Logisim Evolution's README, showing the Download section](setup_2_github_readme_download_section.png)

3. **Selecting the appropriate installer:**
   - Navigating to the GitHub Releases page, we chose the newest available version (4.1.0). For a Windows system with an Intel or AMD processor, the `logisim-evolution-4.1.0-amd64.msi` installer was the correct choice.

     ![Selecting the Windows amd64 .msi installer from the release assets](setup_3_release_assets_page.png)

4. **Downloading the file:**
   - The `.msi` installer was then downloaded to the local computer.

     ![The .msi installer download in progress](setup_4_download_in_progress.png)

5. **Executing the setup:**
   - Opening the downloaded `.msi` file launched the Logisim Evolution Setup Wizard. The on-screen prompts were followed to finalize the installation.

     ![The Logisim Evolution Setup Wizard](setup_5_setup_wizard.png)

**Conclusion:**
With Logisim Evolution successfully installed, the workspace was fully prepared for assembling, wiring, and testing the digital logic circuits explored in the remainder of the lab.


## **Experiment 1: Constructing an OR Gate with NOR Gates**

**Description:**
This experiment demonstrates how to recreate an OR gate using exclusively NOR gates. An OR gate is a fundamental digital logic component that yields a true (1) signal if any of its inputs are true. A NOR gate is a "universal gate," meaning it can be configured to mimic the functionality of any other logic gate, including the OR gate.

**Procedure:**
1. **Understanding the NOR Gate:**
   - A NOR gate operates like an OR gate hooked up to a NOT gate. It produces a true (1) output only when all of its inputs are false (0).
   - The truth table for a 2-input NOR gate is:

   | Input A | Input B | Output (A NOR B) |
   |---------|---------|------------------|
   |    0    |    0    |         1        |
   |    0    |    1    |         0        |
   |    1    |    0    |         0        |
   |    1    |    1    |         0        |

2. **Implementing the OR Gate using NOR Gates:**
   - We rely on the following Boolean identity to build an OR gate from NOR gates:
   - OR(A, B) = NOT(NOR(A, B))
   - To achieve this, the inputs A and B are passed into a primary NOR gate. The output is then fed into a second NOR gate configured as an inverter to reverse the signal.

3. **Circuit Design:**
   - Connect inputs A and B to the first NOR gate.
   - Route the resulting output into both input pins of a second NOR gate, forcing it to act as a NOT gate.

   ![Two-gate NOR circuit implementing OR](circuit_exp1_or_using_nor.png)

4. **Testing the Circuit:**
   - Toggle through all possible binary combinations for A and B to monitor the output.
   - Verify that the resulting outputs mirror a standard OR gate truth table.

**Conclusion:**
This experiment successfully validated that an OR gate can be constructed solely from NOR gates. Showcasing how a NOR gate can be manipulated to perform OR logic emphasizes the flexibility and importance of universal gates in circuit architecture.


## **Experiment 2: Constructing an OR Gate with NAND Gates**

**Description:**
The objective here is to replicate the function of an OR gate using only NAND gates. Similar to the NOR gate, the NAND gate is a universal component capable of assembling any logic operation.

**Procedure:**
1. **Understanding the NAND Gate:**
   - A NAND gate functions identically to an AND gate followed by an inverter. It produces a false (0) output only when every input is true (1).
   - The truth table for a 2-input NAND gate is:

   | Input A | Input B | Output (A NAND B) |
   |---------|---------|-------------------|
   |    0    |    0    |         1         |
   |    0    |    1    |         1         |
   |    1    |    0    |         1         |
   |    1    |    1    |         0         |

2. **Implementing the OR Gate using NAND Gates:**
   - The guiding Boolean logic here is:
   - OR(A, B) = NOT(NAND(NOT(A), NOT(B)))
   - In practice, this requires two NAND gates to individually invert inputs A and B. A third NAND gate then evaluates those inverted signals to generate the final OR output.

3. **Circuit Design:**
   - Pass inputs A and B into separate NAND gates (by tying both input pins of each gate together) to invert their values.
   - Send both of these inverted signals into a third NAND gate.

   ![Three-gate NAND circuit implementing OR](circuit_exp2_or_using_nand.png)

4. **Testing the Circuit:**
   - Test all possible combinations for inputs A and B.
   - Verify that the circuit behaves identically to a dedicated OR gate.

**Conclusion:**
This experiment proved that a working OR gate can be engineered entirely out of NAND gates, providing another clear example of the NAND gate's universal adaptability.


## **Experiment 3: Constructing an AND Gate with NOR Gates**

**Description:**
This task involves building an AND gate purely out of NOR gates. An AND gate outputs true (1) only when all inputs are true. Because NOR is universal, it can easily replicate this strict condition.

**Procedure:**
1. **Understanding the AND Gate:**
   - An AND gate yields a true (1) output solely if both inputs A and B are true (1). Its truth table is:

   | Input A | Input B | Output (A AND B) |
   |---------|---------|------------------|
   |    0    |    0    |         0        |
   |    0    |    1    |         0        |
   |    1    |    0    |         0        |
   |    1    |    1    |         1        |

2. **Implementing the AND Gate using NOR Gates:**
   - The mathematical identity for this conversion is:
   - AND(A, B) = NOT(NOR(NOT(A), NOT(B)))
   - Therefore, you must invert A and invert B using their own NOR gates, and then pass those inverted signals into a third NOR gate to achieve AND functionality.

3. **Circuit Design:**
   - Connect A and B into individual NOR gates (with tied inputs) to act as inverters.
   - Route both of those inverted outputs into a third, combining NOR gate.

   ![Three-gate NOR circuit implementing AND](circuit_exp3_and_using_nor.png)

4. **Testing the Circuit:**
   - Systematically apply all input combinations of A and B.
   - Confirm that the output matches a standard AND gate's truth table.

**Conclusion:**
This setup verified that an AND gate can be built exclusively from NOR gates, reinforcing the NOR gate's status as a foundational building block for any logical structure.


## **Experiment 4: Constructing an AND Gate with NAND Gates**

**Description:**
In this trial, an AND gate is fabricated using only NAND gates. This again relies on the universal nature of the NAND gate to execute any basic logic function.

**Procedure:**
1. **Understanding the AND Gate:**
   - An AND gate registers a true (1) output only when both of its inputs are true (1). Its truth table is:

   | Input A | Input B | Output (A AND B) |
   |---------|---------|------------------|
   |    0    |    0    |         0        |
   |    0    |    1    |         0        |
   |    1    |    0    |         0        |
   |    1    |    1    |         1        |

2. **Implementing the AND Gate using NAND Gates:**
   - The relevant logic identity is highly straightforward:
   - AND(A, B) = NOT(NAND(A, B))
   - A primary NAND gate processes inputs A and B, and a secondary NAND gate—configured as an inverter—flips the result to produce standard AND logic.

3. **Circuit Design:**
   - Send inputs A and B directly into the first NAND gate.
   - Connect that gate's output to both input pins of a second NAND gate to invert the signal.

   ![Two-gate NAND circuit implementing AND](circuit_exp4_and_using_nand.png)

4. **Testing the Circuit:**
   - Run through every logical combination of inputs.
   - Ensure the final output accurately reflects an AND gate's behavior.

**Conclusion:**
This experiment successfully demonstrated that an AND gate can be configured using only NAND gates, illustrating the simplicity and efficiency of universal logic design.


## **Experiment 5: Constructing a NOT Gate with a NOR Gate**

**Description:**
This experiment demonstrates how to craft a NOT gate—a simple inverter that reverses its input—using only a single NOR gate. 

**Procedure:**
1. **Understanding the NOT Gate:**
   - A NOT gate outputs true (1) if its input is false (0), and outputs false (0) if its input is true (1). Its truth table is:

   | Input A | Output (NOT A) |
   |---------|----------------|
   |    0    |        1       |
   |    1    |        0       |

2. **Implementing the NOT Gate using NOR Gates:**
   - The expression used to achieve this is:
   - NOT(A) = NOR(A, A)
   - By feeding the exact same input signal into both pins of a NOR gate, it functions directly as an inverter.

3. **Circuit Design:**
   - Connect input A simultaneously to both input terminals of one NOR gate.

   ![Single NOR gate wired as a NOT gate](circuit_exp5_not_using_nor.png)

4. **Testing the Circuit:**
   - Toggle the single input A and observe the output.
   - Verify that the signal successfully inverts.

**Conclusion:**
This simple experiment proved that duplicating an input across a NOR gate's pins transforms it into a functional NOT gate, once again highlighting the utility of universal gates.


## **Experiment 6: Constructing a NOT Gate with a NAND Gate**

**Description:**
Similar to the previous experiment, this test builds a basic NOT gate (inverter) using a single NAND gate.

**Procedure:**
1. **Understanding the NOT Gate:**
   - A NOT gate reverses its input: a false (0) becomes a true (1), and vice versa. Its truth table is:

   | Input A | Output (NOT A) |
   |---------|----------------|
   |    0    |        1       |
   |    1    |        0       |

2. **Implementing the NOT Gate using NAND Gates:**
   - The controlling identity here is:
   - NOT(A) = NAND(A, A)
   - Tying the same input into both pins of a single NAND gate will immediately invert the signal.

3. **Circuit Design:**
   - Wire input A to both terminals of a single NAND gate.

   ![Single NAND gate wired as a NOT gate](circuit_exp6_not_using_nand.png)

4. **Testing the Circuit:**
   - Switch input A between 0 and 1 and verify the output.
   - Confirm it behaves perfectly as an inverter.

**Conclusion:**
This setup verified that a single NAND gate with tied inputs operates exactly like a standard NOT gate.


## **Experiment 7: Designing and Testing a Full Adder**

**Description:**
This experiment focuses on constructing a Full Adder utilizing standard logic gates. A Full Adder is an essential arithmetic circuit designed to sum three binary bits—two standard bits and a carry-in bit—producing both a sum and a carry-out.

**Procedure:**
1. **Understanding the Full Adder:**
   - A Full Adder processes three inputs (A, B, and Cin) to generate two distinct outputs (Sum and Cout). The truth table is:

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
   - Logically, a Full Adder consists of two Half Adders linked with an OR gate.
   - The first Half Adder sums A and B to create a preliminary sum (S1) and carry (C1).
   - The second Half Adder adds S1 and the incoming Cin to produce the final Sum and a secondary carry (C2).
   - The final carry-out (Cout) is generated by passing C1 and C2 through an OR gate.

3. **Circuit Design:**
   - The underlying circuit uses XOR gates to calculate the sum, while AND and OR gates are routed to handle the carry paths, accurately mirroring the dual Half-Adder architecture.

   ![Full Adder built from XOR, AND, and OR gates](circuit_exp7_full_adder_gates.png)

4. **Testing the Circuit:**
   - Cycle through all eight combinations of A, B, and Cin to observe the Sum and Cout results.
   - Verify these against the standard Full Adder truth table.
   - To ensure broader functionality, the design was also tested within an 8-bit adder setup:

   ![8-bit adder block used to validate the Full Adder logic](circuit_exp7_full_adder_test.png)

   During an 8-bit test, the adder yielded a sum of 10 with a 0 carry-out. Analyzing this at the bit level, this correlates to a sum bit of 0 and a carry-out bit of 1, which aligns with the structural design. Another test showed a sum of 11 with a 0 carry-out, meaning the bit-level sum is 1 and carry-out is 1—again, matching expected behavior.

**Conclusion:**
This practical implementation of a Full Adder using primitive logic gates was a success. Demonstrating how two Half Adders scale up into a Full Adder establishes a firm understanding of binary arithmetic, a foundational concept for how Arithmetic Logic Units (ALUs) process data.


## **Experiment 8: Designing a Binary to BCD Converter**

**Description:**
This final experiment constructs a Binary-to-BCD (Binary-Coded Decimal) converter. This system translates a standard binary sequence into its BCD format, where individual decimal digits are isolated and represented by their own discrete binary codes.

**Procedure:**
1. **Understanding Binary to BCD Conversion:**
   - The converter takes standard binary inputs and outputs the BCD equivalent.
   - For example, the binary sequence 1010 (which is 10 in decimal) transforms into the BCD sequence 0001 0000 (representing a "1" and a "0" digit).
   - The truth table mapping a 4-bit binary input to its BCD output is as follows:

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
   - The logic maps specific binary states to proper BCD states using an array of logic gates.
   - Logic expressions are created for each output bit (D₄, D₃, D₂, D₁). The resulting data is subsequently routed into a BCD-to-seven-segment decoder, enabling the binary inputs (B₃, B₂, B₁, B₀) to drive visual displays.

3. **Circuit Design:**
   - The 4-bit binary input feeds directly into the converter logic. The processed outputs are then connected to three separate seven-segment displays to visually render the decimal equivalent.

   ![Binary-to-BCD converter driving seven-segment displays](circuit_exp8_bcd_converter.png)

4. **Testing the Circuit:**
   - Input various 4-bit binary combinations and observe the corresponding decimal readouts on the seven-segment displays.
   - Verify that all outputs perfectly align with the expected BCD values from the truth table.

**Conclusion:**
This experiment efficiently showcased how to build a Binary-to-BCD converter from basic gates. It provided excellent practical insight into how raw binary data is processed into human-readable decimal formats, a crucial function for digital clocks, calculators, and hardware readouts.

---
<h1 align="center">End of Lab 1 Report</h1>

