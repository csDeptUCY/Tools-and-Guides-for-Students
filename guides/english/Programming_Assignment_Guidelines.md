# General Guidelines and Assessment Parameters for Programming Assignments

These guidelines apply to all programming assignments. Each assignment is graded on a scale of **0–100**, unless otherwise specified in the assignment description.

Each student must study the assignment description carefully and implement a solution that fully satisfies all its requirements. The solution must be the student's own work and must follow the material taught in the lectures and laboratory sessions (see Section 3).

> **Individual responsibility:** Each student is individually responsible for fully understanding, and being able to explain without the aid of notes or external tools, every part of the code submitted under their name—even in a group assignment. This understanding is assessed through a mandatory oral/practical examination (see Section 6), which may reduce the assignment grade, potentially to zero.

---

## 1. Code Comments and Program Structure

The code must be properly organized, with a clear design, logical decomposition into classes or files and methods/functions, consistent indentation, comprehensible naming, and meaningful comments. Comments should explain the **role** of each class, file, or method/function; they should not merely restate the code in natural language.

A **top-down** design approach is recommended: first the overall design and interfaces, then the data structures and methods/functions, and finally the implementation details.

---

## 2. Functional Correctness

The code must fully satisfy the specifications in the assignment brief and produce the correct answer for every required task. A program that does not run, does not terminate, terminates with an error, or does not produce the required output cannot receive a high grade, irrespective of the intention behind it or any partial implementation effort.

**If the program produces no output or encounters errors during execution, the assignment grade will not exceed 20 points (out of 100). This cap applies to the initial grade, before it is adjusted through the examination described in Section 6.**

---

## 3. Permitted Data Structures and Techniques

The data structures and techniques used must be consistent with those taught and required in the lectures and laboratory sessions. The brief for each assignment explicitly specifies which techniques, methods, or libraries are permitted or prohibited; in case of doubt, the matter must be clarified with the instructor **before** submission.

**The implementation must use the data structures, techniques, methods, and libraries specified in the assignment brief and taught or explicitly required in the course. The use of prohibited or unauthorized techniques, as well as failure to implement required data structures, limits the maximum assignment grade to 20 points (out of 100), regardless of the correctness of the result and before the application of Section 6.**

---

## 4. Use of GitHub and Classroom 50, Submission, and Deadline

The assignment must be completed and submitted exclusively through the GitHub repository assigned via Classroom 50. Submission by any other means (e.g., email) will not be accepted.

- Each student must use only their **personal** GitHub account so that individual contributions can be attributed correctly.
- Commits must be made regularly, correspond to meaningful and logically distinct stages of development, and have descriptive messages. The repository history must document the gradual development of the assignment. Submitting most or all of the project through only a few commits, at any point in time, and especially shortly before the deadline, will adversely affect the assessment of GitHub use (see Section 5).
- In group assignments, when explicitly required in the assignment brief, each member must work on their own branch, and integration must be carried out through pull requests with code review, as described in the **Guide to Good Practices for Using GitHub**.
- For every assignment, the repository must include **README.md** and **.gitignore**; group assignments must additionally include **changelog.md** (describing each member's contribution). The brief for each assignment specifies the other mandatory submission files (e.g., source code, report).
- For guidance on writing `.md` files, see the [Markdown Guide](https://www.markdownguide.org/).

**Deadline:** All files required for submission must be present on the **main branch** before the deadline; the time of the last relevant commit to the main branch is considered the submission time. No changes to the repository are permitted after the deadline.

- Late submission results in a grade of **zero**.
- If any file designated as mandatory in the assignment brief or in this section is absent from the main branch, the maximum assignment grade is limited to **50 points (out of 100)**. This cap applies to the initial grade, before it is adjusted through the examination described in Section 6.
- Each student bears sole responsibility for verifying, before the deadline, that the main branch contains the correct and final files and that those files open and run without error.

---

## 5. Assessment Criteria and Weightings

The assignment grade is initially calculated using the criteria in Section 5 and is subject to the grade caps set out in Sections 2, 3, and 4. It is derived from the combination of the following criteria, with **indicative weightings** (the exact weighting for each assignment is specified in its brief):

| Criterion | Weighting | Reference |
|---|---|---|
| Design quality, functional correctness, and completeness | 85% | Sections 1 and 2 |
| Compliance with permitted techniques/data structures | limiting criterion | Section 3 |
| Use of GitHub (commits, branches, files, individual contribution) | 15% | Section 4 |

The grade resulting from the table above (the **initial grade**) is subject to the mandatory procedure in Section 6, which may reduce it, potentially to zero, regardless of how high it is. The oral examination **does not add a separate percentage of its own** to the grade; it functions solely as a factor for confirming or reducing the initial grade.

In specialized cases, the criteria in the table may be explicitly supplemented in the assignment brief by the following: appropriate selection of algorithms/data structures for the specific assignment, quality of experiments and discussion of results, and ability to adapt the solution to changes in requirements during the examination described in Section 6.

---

## 6. Oral/Practical Examination

The assessment of understanding is **mandatory for all programming assignments**, unless explicitly stated otherwise in the assignment brief. For each assignment, the instructor determines and announces whether the examination will be oral, practical and conducted on a computer, or a combination of both, as well as its date, time, duration, location, and permitted aids. For group assignments, the examination may begin with a joint group discussion. The instructor may then ask individual questions or assign individual practical modifications to each member in order to assess their individual understanding and contribution.

During the examination, each student may be asked to:

- Explain the overall architecture of the solution.
- Justify the choice of data structures and algorithms.
- Identify and correct errors in real time.
- Adapt the code to new requirements provided during the examination.
- Describe the sources and tools used (see Section 7) and how they were used.

**Effect on the grade:** The initial grade from Section 5 is adjusted on the basis of performance in the examination, as follows:

- A complete and independent explanation of all requested points: the initial grade **remains unchanged**.
- A partial or incomplete explanation: the initial grade is **reduced proportionally**, according to the extent to which the student is unable to substantiate their work.
- Inability to explain fundamental aspects of the solution, or absence from the examination without a documented reason: the assignment grade is **reduced to zero**, regardless of the initial grade from Section 5.
- Violations of Section 7 are addressed in accordance with the consequences specified in that section.

---

## 7. Use of Sources and Artificial Intelligence

Each assignment must include a section in README.md entitled "Sources and Use of AI Tools," in which the external sources and tools that directly influenced the design, implementation, or documentation of that specific assignment are explicitly disclosed. This includes books, websites, notes, code repositories, examples, forum discussions, and all AI tools. For each source, the following must be stated: which source was used, where in the assignment it was used, and how it contributed (to understanding, design, or implementation).

**Permitted**: use of sources/AI tools to understand concepts or techniques, with substantial independent engagement and explicit disclosure, provided that such use is consistent with the restrictions in Section 3. For example, an AI tool may be used to explain a concept or an error message.

**Not permitted**: verbatim copying of code or text from AI tools or other sources without disclosure; concealing the use of AI or presenting another person's work as one's own. Submitting code that was generated, transformed, or substantially corrected by an AI tool is not permitted, even if the student has studied it or can explain it.

Disclosure of use does not, in itself, make that use legitimate: the use must be permitted, limited, and consistent with the learning objectives of the assignment. Each student must also comply with the [University of Cyprus Artificial Intelligence Guidelines](https://www.ucy.ac.cy/ai/ucy-guidelines/). Unauthorized use of sources or AI tools may result in a grade of zero and disciplinary sanctions.
