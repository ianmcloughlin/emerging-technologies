# Assessment Brief

**Emerging Technologies, Summer 25/26**

This assessment is an opportunity for you to demonstrate achievement of the module learning outcomes.
The primary focus of this assessment is to complete the problems in the [Problems](#problems) section of this document.
Start by making a new GitHub repository solely for this assessment.
Create a new Jupyter notebook named `problems.ipynb` in the root of the repository.
Submit the repository URL using the link below before the given URL submission date.
You should then work consistently on your repository until the final deadline for commits below.
The last commit pushed to GitHub on or before the deadline will be assessed.

> [!IMPORTANT]  
> [Submit Your Repository URL Here by 06 February 2026 (ATU Login required)](https://forms.cloud.microsoft/e/dnB7Dmhgb8)  
>   
> Final Deadline for Commits:  
> <ins>**01 May 2026**</ins>  

Always keep your latest work in GitHub.
If you have problems, especially with git, ask for help well before the deadline.
Do not delete your repository without consulting the lecturer.
Disproportionately large commits, especially late in the semester, will usually not be accepted.
Make sure to consult and adhere to the policies on the student portal, such as those relating to student conduct and plagiarism.

## Target Audience

Complete the assessment with the following target audience in mind: an informed computing professional, such as a prospective employer.
Assume they have a strong background in computing but may not be familiar with the specific language, packages, or tools you use.
They should be able to clone your repository and run any code within it with minimal setup and without any extra help from you.
Include setup instructions in your `README.md`, and keep all necessary data files and images cleanly organized.
If any files are too large to include in your repository, explain this in your `README.md` and, where possible, provide code to automatically download them.

## Organization and Structure

Your submission should be in the `main` branch of your repository.
Include a clear [`README.md`](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes), a suitable [`.gitignore` file](https://www.toptal.com/developers/gitignore), and an [accurate `requirements.txt` file](https://realpython.com/what-is-pip/#using-requirements-files).
Avoid including [unnecessary files or folders](https://realpython.com/python-git-github-intro/#what-not-to-add-to-a-git-repo).
Use lowercase file and folder names, except for the usual files like `README.md`.
Do not use spaces or special characters in filenames.
Underscores, hyphens, and full stops are okay.

Your commit history should show how your work evolved: improvements, refinements, and added clarity.
Keep your notebook [reproducible, clean, and concise.](https://arxiv.org/pdf/2202.07233)
Use a [level 1 heading](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#headings) for the notebook title.
Use [level 2 Markdown headings](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#headings) to clearly identify each problem within the notebook.
Use Markdown cells to give explanations and insights into your code.

Follow Python coding standards and guidelines such as [PEP8](https://peps.python.org/pep-0008/).
Write clean, readable, and efficient code using meaningful variable names and consistent formatting.
Break code into smaller, manageable cells whenever possible.
Each code cell should focus on a single step in your overall solution.
Include [meaningful comments](https://realpython.com/python-comments-guide/) and [docstrings](https://peps.python.org/pep-0008/#documentation-strings) in your code.
You can use [modules in the standard library](https://en.wikipedia.org/wiki/Standard_library) and any of the packages in the [requirements.txt file in this repository](./requirements.txt) and their dependencies.
Ask before using anything else.

## Submission Checklist

- [ ] **Repository Link Submitted:** You have submitted your GitHub repository URL in the format `https://github.com/username/reponame` via the Microsoft Forms link above.

- [ ] **Correct Notebook Name:** Your primary submission file is located in the root of the repository and is named exactly `problems.ipynb` (all lowercase, no spaces).

- [ ] **Essential Files:** Your repository includes a `.gitignore`, a `README.md` with setup instructions, and a `requirements.txt` listing all necessary Python packages (e.g., `numpy`).

- [ ] **Notebook Cell Order:** You have restarted the kernel and run all cells in your notebook to ensure they execute in sequential order (1, 2, 3...) without errors, providing a clean and reproducible output.

- [ ] **Folder Organization:** Any extra files are organized into subfolders; specifically, any datasets are in a `/data` folder and any images, plots, or diagrams are in an `/img` folder.

- [ ] **Repository Tidiness:** You have removed all irrelevant files (e.g., `.DS_Store`, `__pycache__`, local checkpoints, or temporary scratchpads).

- [ ] **Environment Reproducibility:** When someone clones your repo, they will likely use the following workflow. Ensure your `README.md` and `requirements.txt` make this process seamless:

    1. `git clone <repo-url>`
    2. `pip install -r requirements.txt`
    3. `jupyter notebook problems.ipynb`

## Marking Scheme

Your submission will be assessed across the following five equally-weighted categories.
Make sure you provide clear evidence within your repository of the criteria listed.
A good submission will meet most of the criteria in each category.
An excellent submission will demonstrably meet all the criteria.
Note that the overall impression your submission makes may influence marks in each category.

### Presentation

- Your repository should be well-organized, with a clear and logical structure.
- Your `README.md` should clearly explain the purpose of your repository and how to run any code it contains.
- Your notebook should present a clear narrative, making it easy to follow your thought process.
- A knowledgeable expert reviewing your repository should be able to understand its contents without your help.

### Research

- Your submission should demonstrate research on relevant topics, showing an understanding of the material.
- You should build upon existing literature and documentation rather than just presenting basic solutions.
- References and comparisons to similar work should be included.
- References should be put into context - how and why they are relevant to your submission.

### Documentation

- Your repository should contain standard files, such as a `README.md`, to provide context for your work.
- All concepts should be clearly and concisely explained within your notebooks.
- Code should include informative comments that clarify its purpose and functionality.
- Your `README.md` and notebook should have clear headings and provide a clear context as to what is contained within.

### Development

- Your code should be efficient and well-structured, effectively addressing the problem at hand.
- Standard programming structures, algorithms, and testing methods should be applied where appropriate.
- The overall architecture of your code should be clean, demonstrating good coding practices.
- Your code should demonstrate your knowledge of established style conventions and norms.

### Consistency

- Each commit should focus clearly on a single unit of work.
- Your commit history should show consistent activity across the semester, not a burst of late submissions.
- Your repository should demonstrate incremental review and refinement rather than one-off completion.
- Commits should capture improvements to both code quality and explanations over time.

## Problems

Complete all problems below in your `problems.ipynb` notebook.

These problems explore the difference between classical and quantum algorithms.

## Problem 1: Generating Random Boolean Functions

The [Deutsch–Jozsa algorithm](https://quantum.cloud.ibm.com/learning/en/modules/computer-science/deutsch-jozsa) is designed to work with functions that accept a fixed number of [Boolean inputs](https://realpython.com/python-boolean/) and return a single [Boolean output](https://realpython.com/python-boolean/).
Each function is guaranteed to be either constant (always returns `False` or always returns `True`) or balanced (returns `True` for exactly half of the possible input combinations).
Write a Python function `random_constant_balanced` that returns a randomly chosen function from the set of constant or balanced functions taking four Boolean arguments as inputs.

## Problem 2: Classical Testing for Function Type

[Deutsch's algorithm](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/quantum-query-algorithms/deutsch-algorithm) is designed to demonstrate a [potential advantage of quantum computing](https://www.quantamagazine.org/john-preskill-explains-quantum-supremacy-20191002/) over classical computation.
To understand this advantage, we must first understand the classical cost of solving the underlying problem.
Write a Python function `determine_constant_balanced` that takes as input a function `f`, as defined in Problem 1.
The function should analyze `f` and return the string `"constant"` or `"balanced"` depending on whether the function is constant or balanced.
Write a brief note on the efficiency of your solution.
What is the maximum number of times you need to call `f` to be 100% certain whether it is constant or balanced?

## Problem 3: Quantum Oracles

[Deutsch's algorithm](https://quantum.cloud.ibm.com/learning/en/courses/fundamentals-of-quantum-algorithms/quantum-query-algorithms/deutsch-algorithm) is the simplest example of a [quantum algorithm](https://www.ibm.com/quantum/blog/group-theory) using [superposition](https://scienceexchange.caltech.edu/topics/quantum-science-explained/quantum-superposition) to determine a [global property](https://plato.stanford.edu/archives/fall2008/entries/qt-entangle/#5) of a function with a single evaluation.
In the single-input case, there are four possible Boolean functions.
Using Qiskit, create the appropriate [quantum oracles](https://quantumcomputing.stackexchange.com/a/4626) for each of the possible single-Boolean-input functions used in Deutsch's algorithm.
Demonstrate their use and explain how each oracle implements its corresponding function.

## Problem 4: Deutsch's Algorithm with Qiskit

Use [Qiskit](https://www.ibm.com/quantum/qiskit) to design a [quantum circuit](https://quantum.cloud.ibm.com/learning/en/courses/basics-of-quantum-information/quantum-circuits/introduction) that solves Deutsch's problem for a function with a single Boolean input.
Implement the necessary circuit and demonstrate its use with each of the quantum oracles from Problem 3.
Describe how the interference pattern produced by the circuit allows you to determine whether the function is constant or balanced using only one query to the oracle.

## Problem 5: Scaling to the Deutsch–Jozsa Algorithm

The [Deutsch–Jozsa algorithm](https://quantum.cloud.ibm.com/learning/en/modules/computer-science/deutsch-jozsa) generalizes Deutsch's approach to functions with several input bits.
Use [Qiskit](https://www.ibm.com/quantum/qiskit) to create a quantum circuit that can handle the four-bit functions generated in Problem 1.
Explain how the classical function is encoded as a quantum oracle, and demonstrate the use of your circuit on both of the constant functions and any two balanced functions of your choosing.
Show that the circuit correctly identifies the type of each function.

***

**End**
