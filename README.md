# Ex.No.6 AI-Assisted Programming and Debugging

### Date: 

### Name: N.bharath

### Register no. 212223230030

---

# AIM

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

---

# AI TOOLS REQUIRED

* ChatGPT
* Google Gemini
* GitHub Copilot

---

# EXPLANATION

Experiment the persona pattern as a programmer for any specific application related to your interesting area. Generate the output using more than one AI tool and, based on the code generation, analyse and discuss the generated code.

Learners generate:

* Python
* C
* Java

using AI.

Then:

* Identify bugs
* Optimise code
* Explain complexity
* Generate unit tests
* Finally compare manual coding versus AI-assisted coding

**Deliverable:** Code quality analysis.

---

# AI-ASSISTED PROGRAMMING AND DEBUGGING

## OBJECTIVE

To use multiple AI tools as programming assistants for generating, analysing, debugging, optimizing and testing code.

The experiment focuses on comparing AI-generated solutions and evaluating their correctness, efficiency, readability and code quality.

---

# TOOLS USED

| Tool           | Purpose                                         |
| -------------- | ----------------------------------------------- |
| ChatGPT        | Code generation, debugging and code explanation |
| Google Gemini  | Alternative code generation and comparison      |
| GitHub Copilot | Code suggestions and optimization               |
| Python         | API interaction and automation                  |
| C              | AI-assisted programming                         |
| Java           | AI-assisted programming                         |

---

# EXERCISE DESCRIPTION

The experiment is carried out using multiple AI tools.

The following activities are performed:

1. Generate Python code using AI.
2. Generate C code using AI.
3. Generate Java code using AI.
4. Compare the generated outputs from different AI tools.
5. Identify bugs in the generated code.
6. Debug and correct the identified errors.
7. Optimize the generated code.
8. Analyse time and space complexity.
9. Generate unit test cases.
10. Compare manual coding with AI-assisted coding.
11. Analyse the overall code quality.

---

# 1. PYTHON PROGRAMMING

## Prompt

> Act as a Python programmer. Generate a simple Python program that interacts with an API, processes the API response and displays useful information. Provide clean and readable code and explain the complexity.

## AI-Generated Code

```python
import requests

url = "https://api.github.com"

response = requests.get(url)

if response.status_code == 200:
    data = response.json()
    print("API Response:")
    print(data)
else:
    print("API request failed")
```

## Output

```text
API Response:
{API response data}
```

## Analysis

The Python program sends a request to an API using the `requests` library and processes the returned response.

The response is checked using the HTTP status code before displaying the data.

## Complexity

* **Time Complexity:** O(n), depending on the size of the API response.
* **Space Complexity:** O(n), because the response data is stored in memory.

---

# 2. C PROGRAMMING

## Prompt

> Act as a C programmer and generate a simple program to demonstrate AI-assisted programming. The program should accept an integer and determine whether it is prime.

## AI-Generated Code

```c
#include <stdio.h>

int main()
{
    int n, i, flag = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n < 2)
        flag = 1;

    for (i = 2; i * i <= n; i++)
    {
        if (n % i == 0)
        {
            flag = 1;
            break;
        }
    }

    if (flag == 0)
        printf("Prime number");
    else
        printf("Not a prime number");

    return 0;
}
```

## Output

```text
Enter a number: 17
Prime number
```

## Analysis

The AI-generated program checks whether the input number is divisible by any number from 2 up to its square root.

## Complexity

* **Time Complexity:** O(√n)
* **Space Complexity:** O(1)

---

# 3. JAVA PROGRAMMING

## Prompt

> Act as a Java programmer and generate a program to compare two outputs and identify whether they are equal.

## AI-Generated Code

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first output: ");
        String output1 = sc.nextLine();

        System.out.print("Enter second output: ");
        String output2 = sc.nextLine();

        if (output1.equals(output2))
            System.out.println("Outputs are equal");
        else
            System.out.println("Outputs are different");

        sc.close();
    }
}
```

## Output

```text
Enter first output: 100
Enter second output: 100
Outputs are equal
```

## Analysis

The program accepts two outputs and compares them using Java's `equals()` method.

This can be used to compare outputs generated by different AI tools.

## Complexity

* **Time Complexity:** O(n), where n is the length of the strings.
* **Space Complexity:** O(n)

---

# 4. BUG IDENTIFICATION AND DEBUGGING

## Prompt

> Identify the bug in the following Python code, explain why the error occurs and provide the corrected version.

## Buggy Code

```python
import requests

url = "https://api.github.com"

response = requests.get(url)

print(response.json())
```

## AI-Generated Analysis

The program directly converts the response into JSON without checking whether the API request was successful.

If the API request fails or the response does not contain valid JSON data, an error may occur.

## Corrected Code

```python
import requests

url = "https://api.github.com"

response = requests.get(url)

if response.status_code == 200:
    print(response.json())
else:
    print("API request failed")
```

## Output

```text
API response displayed successfully.
```

## Result of Debugging

The error was identified and the program was modified to check the API response before processing the data.

---

# 5. CODE OPTIMIZATION

## Original Code

```python
numbers = [1, 2, 3, 4, 5, 6]

even_numbers = []

for number in numbers:
    if number % 2 == 0:
        even_numbers.append(number)

print(even_numbers)
```

## Prompt

> Optimize the following Python code using a simple and readable approach without changing its output.

## Optimized Code

```python
numbers = [1, 2, 3, 4, 5, 6]

even_numbers = [number for number in numbers if number % 2 == 0]

print(even_numbers)
```

## Output

```text
[2, 4, 6]
```

## Analysis

The optimized version uses list comprehension.

It reduces the number of lines while maintaining the same functionality.

* **Time Complexity:** O(n)
* **Space Complexity:** O(n)

---

# 6. UNIT TEST GENERATION

## Prompt

> Generate unit test cases for a Python program that compares two outputs and returns whether they are equal.

## Function

```python
def compare_outputs(output1, output2):
    return output1 == output2
```

## Unit Tests

```python
def test_equal_outputs():
    assert compare_outputs("100", "100") == True

def test_different_outputs():
    assert compare_outputs("100", "200") == False

def test_empty_outputs():
    assert compare_outputs("", "") == True

def test_case_difference():
    assert compare_outputs("Python", "python") == False
```

## Test Cases

| Test Case         | Input                | Expected Output |
| ----------------- | -------------------- | --------------- |
| Equal outputs     | `"100", "100"`       | `True`          |
| Different outputs | `"100", "200"`       | `False`         |
| Empty outputs     | `"", ""`             | `True`          |
| Case difference   | `"Python", "python"` | `False`         |

## Output

```text
All test cases passed successfully.
```

## Result

Unit tests were successfully generated using AI to verify different possible inputs and outputs.

---

# 7. MANUAL CODING VS AI-ASSISTED CODING

| Criteria            | Manual Coding                        | AI-Assisted Coding                       |
| ------------------- | ------------------------------------ | ---------------------------------------- |
| Code Generation     | Written completely by programmer     | Generated with AI assistance             |
| Development Speed   | Comparatively slower                 | Faster                                   |
| Bug Identification  | Done manually                        | AI can identify common errors            |
| Debugging           | Requires manual analysis             | AI provides possible corrections         |
| Optimization        | Programmer finds improvements        | AI suggests optimized solutions          |
| Complexity Analysis | Calculated manually                  | AI can explain complexity                |
| Unit Testing        | Written manually                     | AI can generate test cases               |
| Code Comparison     | Done manually                        | Multiple AI outputs can be compared      |
| Learning            | Requires independent problem solving | AI provides explanations and suggestions |
| Verification        | Programmer checks all code           | Human verification is still required     |

---

# 8. CODE QUALITY ANALYSIS

The generated programs were analysed based on the following factors:

| Factor           | Analysis                                                 |
| ---------------- | -------------------------------------------------------- |
| Correctness      | AI-generated code generally produced the expected output |
| Readability      | The generated code was simple and understandable         |
| Efficiency       | AI suggested improvements for better efficiency          |
| Debugging        | Common syntax and logical errors were identified         |
| Testing          | Unit test cases were generated automatically             |
| Maintainability  | Structured code was easier to modify                     |
| Development Time | AI-assisted development reduced coding time              |

The outputs generated using different AI tools can be compared based on correctness, readability, efficiency and completeness.

---

# CONCLUSION

The experiment demonstrated the use of multiple AI tools for AI-assisted programming and debugging. Python, C and Java programs were generated using AI, and the generated code was analysed for correctness, complexity and quality.

Bugs were identified and corrected, code was optimized, and unit test cases were generated using AI. The comparison between manual coding and AI-assisted coding showed that AI can reduce development time and provide useful programming assistance.

However, the generated code must be reviewed and verified by the programmer before implementation.

---

# RESULT

The corresponding Prompt is executed successfully.
