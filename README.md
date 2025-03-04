# Parachuting Into a New Codebase

As developers, we will frequently find ourselves working with codebases we didn't create. At first glance, these systems may have complex file organizations, convoluted function interactions, foreign code structures, and mysterious symbols. Building the skill of understanding code and systems that you did not write or design is crucial and time-saving. This guide offers practical strategies to help you efficiently navigate and comprehend unfamiliar code.

## Why Improve your ability to navigate unfamiliar code bases?
- Understanding system architecture and file organization is essential but time-intensive.
- Finding the right files to modify can be frustrating and experimental.
- Effective navigation techniques can dramatically reduce onboarding and development time.


## Steps to Find your Bearings
<details>
<summary> <h3> Step 1: Initial Reconnaissance </h3></summary>

#### 1. Get oriented with the file organization
Look over the files and folders just to figure out **what’s there and what’s where**. Check if there’s frontend code, backend code, or both. How are screens and pages organized? Are images kept in a separate folder? Where are the CSS files? Are helper functions abstracted out? Identify what languages are used and what they do—this is important so you know how to print. This helps you build intuition about where different parts of the project are located and where you might find what you're looking for.

#### 2. Figure out how to run the project 

* **Check the `README.md` file for run instructions.** This file would usually contain detailed instructions on how to set up and run a project, including information like required dependencies, installation steps, commands to execute the project, and any specific environment configurations needed to run the code properly, etc.  
![Image](https://github.com/user-attachments/assets/a3cc089c-33e5-4816-b984-c599fc23a1bd)


* If the run instructions are not in the `README` file, **look into configuration files (e.g., `package.json`, `docker-compose.yml`) for clues.**  These files specify **dependencies, scripts, services, and environment configurations needed to set up and run the project** and have a section that outlines how to run the project locally.  
#### For example:
| In `package.json`, check the run instructions. Under the `script` section,  you will find a list of terminal commands that may run, build, deploy and etc. your project. |Identify which package manager the project uses. The most common are npm (`package-lock.json` file exists) and yarn (`yarn.lock` file exists). Then use the correct packet manager command to execute the command.  eg. To start a project, use either `yarn start` or `npm start`, depending on the package manager used.| Check the console for errors. These usually contain further clues or corrections that help you correct run the project|
|-----------------|----------------|----------------|
|  ![Image](https://github.com/user-attachments/assets/fba1cf77-0aa6-43ad-8324-28807d157826) | ![Image](https://github.com/user-attachments/assets/a65f3371-62f0-492b-a15a-e584c79a2c9b)|![Image](https://github.com/user-attachments/assets/7d743a91-73a4-4692-b9ff-ac3bcc062bea) |

<img width="901" alt="Image" src="https://github.com/user-attachments/assets/a58236bd-4c7a-4fbc-81c2-dd41a231c157" />

</details>
<details>
<summary> <h3> Step 2: Poke and Observe </h3></summary>
At this point, you likely have a task or goal in mind—whether fixing a bug or adding a new feature—and need to find the relevant files to edit. Now that you're familiar with the file organization and have managed to run the code, we’ll take a Dr. House approach to locating the correct files and functions: change something and see what happens.

#### Navigation Tools:

- **Browser Inspection:**
For web development, most browsers come with built-in inspectors that allow you to view the HTML governing the page content. This is useful for examining HTML elements, their hierarchy, their classes, and other debugging and tracing tools.

| Inspect Element  | Evaluate HTML |
|---------------|---------------|
|<img width="542" alt="Image" src="https://github.com/user-attachments/assets/0aafedbb-6206-4f86-ac0f-e67b016a715a" />|<img width="1487" alt="Image" src="https://github.com/user-attachments/assets/fd0a0893-b8b5-454b-95b1-30b54190ec08" />|
| **Chrome:** Right-click > Inspect <br/> **Safari:** Right-click > Inspect Element    | You can identify what each HTML tag is responsible for rendering, helping you locate the section you need.| 


- **Print as you go:**
  [start with 
  plonk a print staetment wherever]

  Print statements help wuth:
  - Check if a function is running
  - check control flow
  - ives you an x-ray into variables and parameters, can print whole file strutures and almost any data type with 

  <br/> When printing there are three main places your output might appear:

| Terminal Console | Browser Console    | Log File|
|---------------|---------------|---------------|
| <img width="513" alt="Image" src="https://github.com/user-attachments/assets/2e89c844-901c-4d03-add7-9c8a00667a34" /> | <img width="513" alt="Image" src="https://github.com/user-attachments/assets/cc992840-3574-404f-847f-c7a3513c72c7" /> |![Image](https://github.com/user-attachments/assets/2489393d-c9b3-44ce-97c8-9dc3c3bf3f28) ![Image](https://github.com/user-attachments/assets/1323eccc-5c24-4401-b1f9-e64996144444)|
| This is usually the terminal that you used to original run your project | **Chrome:** Right-click > Inspect > select the Console tab <br/> **Safari:** Right-click > Inspect Element  > select the Console tab  |the `log` file is a computer generate file that logs user actions, error messages and print statements (depending on the project settings) |



- **Use IDE code navigation features:**
   Visual Studio has a host of ["Go To" features](https://learn.microsoft.com/en-us/visualstudio/ide/navigating-code?view=vs-2022&viewFallbackFrom=vs-2025) that allow you to quickly locate definitions, references, and implementations. Simply, right click on any function, variable, element, object etc.
![Image](https://github.com/user-attachments/assets/1bd8f992-ee33-4d78-8912-d20f94f1fc32)

- **Guess the file, function, and variable names using common words and syntaxes:** 
  It's good practice to give variables, functions, files, and other structures intuitive names that follow standard conventions. The benefit of this is guessability—if you’re struggling to find something, you can often predict its name. This makes searching easier using the `search (Shift + Cmd + F)` feature to search the entire project or `find Cmd + F` feature to search within the current file. <br/>
  Eg. if you're looking for a function that formats dates, you might try searching for keywords like "formatDate" or "parseDate" to quickly locate it.
</details>

## Summary
Quickly understanding a new codebase is essential. This guide covers key strategies like file navigation, browser inspection, print debugging, and IDE search tools to help you locate and modify code efficiently.
