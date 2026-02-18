#  Multi-Set Intersection Engine

## Overview
This project provides an interactive interface for performing set intersection operations across multiple datasets. It was engineered to solve the common problem of visualizing shared elements in complex discrete math problems without manual calculation. 

The application serves as a bridge between formal set theory and modern web interactivity, allowing users to observe mathematical truths in real-time.



[Image of Venn diagram showing the intersection of three sets A, B, and C]


---

## Functional Highlights

* **Automatic Set Logic**: Implements an $O(n \times m)$ intersection algorithm that evaluates commonality across an array of sets.
* **Reactive User Interface**: The UI is designed to be "invisible"—calculating results instantly as the user inputs data, significantly reducing cognitive load.
* **Set Theory Compliance**: The engine strictly follows formal set properties, automatically removing duplicate entries within a single set and sorting the resulting intersection for professional presentation.
* **Edge Case Handling**: Includes specialized logic to handle empty inputs, non-numeric values, and the mathematical null set ($\emptyset$).

---

## Technical Logic Flow

The intersection is determined by reducing the collection of sets using a filtering predicate. This ensures that an element is only included in the final output if and only if it satisfies the condition:

$$x \in A \cap B \cap C \iff (x \in A \land x \in B \land x \in C)$$



### Algorithm Implementation
1. **Sanitization**: Raw string inputs are parsed, whitespace is trimmed, and strings are cast to numeric types.
2. **De-duplication**: Each individual input is converted to a unique set to respect the fundamental definition of a mathematical set.
3. **Reduction**: A recursive filtering process compares the first two sets, then compares that result to the third, and so on, until the global commonality is found.
4. **Final Rendering**: The result is sorted and displayed using the formal $\emptyset$ symbol if the intersection set is empty.

---

## How to Use
1. Select the **Number of Sets** you wish to compare.
2. Enter your elements separated by commas (e.g., `1, 2, 3`).
3. View the live result in the **Intersection Output** section.
