# LeetCode Problem Manager Extension

The **LeetCode Problem Manager** Chrome extension simplifies the workflow of solving LeetCode problems by automating the extraction of test cases and the creation of solution templates. With this extension, you can seamlessly fetch test cases from the problem page and generate solution files in Python (`.py`) or C++ (`.cpp`) with minimal effort. Additionally, the extension provides a robust testing setup using a `test.py` script and preconfigured VS Code tasks.

---

## **Key Features**

- Automatically detects the open LeetCode problem page URL.
- Prompts for the preferred programming language (`cpp` or `py`) and generates a solution file accordingly.
- Extracts test cases and saves them in a structured JSON file (`test_cases_named.json`).
- Creates boilerplate solution files in the selected language.
- Enables easy testing of solutions against extracted test cases using `test.py` and Visual Studio Code tasks.

---

## **Installation**

### **Step 1: Download the Extension**

1. Clone this repository or download the files to your local system.

### **Step 2: Add the Extension to Chrome**

1. Open Chrome and navigate to `chrome://extensions/`.
2. Enable **Developer mode** in the top-right corner.
3. Click **Load unpacked** and select the directory containing the extension files.

### **Step 3: Set Up the Backend Server**

1. Ensure Python is installed on your system.
2. Install the necessary Python packages:
   ```bash
   pip install flask cloudscraper beautifulsoup4
   ```
3. Start the Flask server:
   ```bash
   python app.py
   ```
4. The server will run locally at `http://127.0.0.1:5000`.

---

## **Usage**

### **Running the Extension**

1. Open any LeetCode problem page in Chrome.
2. Click the **LeetCode Problem Manager** icon in the toolbar.
3. Select the desired programming language (`cpp` or `py`) from the prompt.
4. The extracted test cases and solution files will be saved in the default directory.

### **File Organization**

The generated files will follow this folder structure:

```
/leetcode/
  ├── two-sum/
  │   ├── test_cases_named.json
  │   ├── solution.py
  │   ├── solution.cpp
  ├── test.py
  └── .vscode/
      └── tasks.json
```

---

## **Testing Your Solutions**

### **Prerequisites**

1. Place `test.py` (available in this repository) in the `leetcode` folder.
2. Create a `.vscode` folder in the `leetcode` directory and add the provided `tasks.json` file.

### **Steps to Test**

1. Open Visual Studio Code (VS Code).
2. Open the solution file you wish to test (e.g., `solution.py` or `solution.cpp`).
3. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) and choose **Tasks: Run Task**.
4. Select **Test Current Solution** from the task list.
5. View the test results in the VS Code terminal.

---

## **Notes**

- **Custom Folder Paths:** If you rename the `leetcode` folder or change its location, update the path in `fetch.py`.
- **Preconfigured Tasks:** The `tasks.json` file is set up to run the `test.py` script for testing solution files.
- **Language Selection:** Ensure you select the correct language (`cpp` or `py`) when prompted by the extension. This determines the type of solution file generated.

---

Enhance your problem-solving experience with the **LeetCode Problem Manager** and focus on what truly matters—crafting your solutions!
