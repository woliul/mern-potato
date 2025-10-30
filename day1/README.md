## 📅 Day 1, Hour 1: `var`, `let`, and `const` (The Modern JS Trio)

| Phase | Duration | Focus Area | Goal |
| :--- | :--- | :--- | :--- |
| **Learn** | 20 min | Define: `var`, `let`, `const`, Scoping | Understand the core differences and the **Rule of `const` First**. |
| **Practice** | 20 min | Write Snippets | Demonstrate reassignment, redeclaration, and block scoping. |
| **Test** | 10 min | Scenario Challenge | Apply best practices to choose the correct keyword. |
| **Review** | 10 min | Mentor Feedback & Result | Self-assessment and solidification of the material. |

-----

### 1\. Learn (20 min)

We focus on the two modern keywords, **`let`** and **`const`**, and why we avoid the old **`var`**.

#### **A. `const` (Constant)**

| Aspect | What it is & Example | How to Use | When to Use (Best Practice) |
| :--- | :--- | :--- | :--- |
| **What** | A keyword for declaring a variable whose value **cannot be reassigned**. | `const API_URL = "http://api.local";` | **Always use `const` by default.** This is the professional standard. If you realize later that the value must change, switch it to `let`. |
| **How** | You must assign a value immediately upon declaration. | `const patientId = 5;` | |
| **Why** | It prevents accidental reassignments, making your code safer and easier to debug. | | |
| **Nuance** | For objects and arrays, you can change the **contents**, but not the variable itself.  | `const user = { name: "Potato" };` | |
| | | `user.name = "Spud"; // Allowed` | |
| | | `user = {}; // Error! Not allowed` | |

#### **B. `let` (Mutable Variable)**

| Aspect | What it is & Example | How to Use | When to Use (Best Practice) |
| :--- | :--- | :--- | :--- |
| **What** | A keyword for declaring a variable whose value **can be reassigned**. | `let count = 0;` | Only use `let` when you know the variable's value must change, such as: **counters** in loops, or variables whose values are calculated over time. |
| **How** | Declare it, and then change its value later. | `let status = "pending";` | |
| | | `status = "complete";` | |
| **Why** | It’s the safe, modern replacement for `var` when mutability (changeability) is needed. | | |

#### **C. Scoping (Where the variable exists)**

| Aspect | What it is & Example | How to Use | When to Use (Best Practice) |
| :--- | :--- | :--- | :--- |
| **What** | **Block Scoping** means a variable only exists within the nearest set of curly braces (`{...}`) where it was defined. This applies to **`let`** and **`const`**. | | **Block Scoping** prevents variables from "leaking" out and clashing with variables elsewhere in your program. |
| **How** | Look for the nearest `{}`. | `if (true) { let x = 10; }` | |
| | | `console.log(x); // ERROR: x is not defined outside the block.` | |
| **Avoid** | **`var`** is **Function Scoped**, meaning it can "leak" out of blocks like `if` statements and `for` loops, which causes bugs. **Never use `var` in MERN projects.** | | |

-----

### 2\. Practice (20 min)

**Your Task:** Open your environment and run these snippets. The goal is to see the errors and the expected output firsthand.

#### **Practice 1: Mutability (Reassignment)**

Use your editor/console to run this code and observe the errors.

```javascript
// A. Reassignment Check
const patientName = "Alice";
// patientName = "Bob"; // Uncomment this line. What error do you see?

// B. Mutating Object Content Check
const admission = {
    date: '2025-01-15',
    department: 'ER'
};
admission.department = 'ICU'; // Change the property. Is this allowed?

// C. Mutating the Reference Check
// admission = { date: '2025-01-16', department: 'ICU' }; // Uncomment this line. What error do you see?

console.log('Final Department:', admission.department);
```

#### **Practice 2: Scoping**

Run this to see exactly where the `let` variable stops existing.

```javascript
function checkScopes() {
    let week = 1; // Function-scoped 'let'

    if (week === 1) {
        let dailyTask = "JS Fundamentals"; // Block-scoped 'let'
        console.log(dailyTask); // ✅ Output: JS Fundamentals
    }

    // console.log(dailyTask); // Uncomment this. What error do you see?
}
checkScopes();
```

-----

**Pause here, run the code, and capture the following results:**

1.  What error message did the reassignment in Practice 1A produce?
2.  What was the `Final Department` output in Practice 1B?
3.  What error message did the reassignment in Practice 1C produce?
4.  What error message did the `console.log(dailyTask)` outside the block in Practice 2 produce?

-----

### 3\. Test (10 min)

**Scenario Challenge:**

For a new feature, a colleague suggests using `var` for one of these variables. Based on **best practice**, which keyword (`let` or `const`) is the *most appropriate* to use instead?

| Variable Name | Intended Usage | Recommended Keyword | Reasoning (Why `const` or `let`?) |
| :--- | :--- | :--- | :--- |
| `MAX_PATIENTS` | A hard limit (e.g., 50) that should never change. | | |
| `selectedPatient` | An object pulled from a list. You might add a temporary property to it, like `selectedPatient.isEditing = true;` | | |
| `searchQuery` | A text field value that changes every time the user types a new character. | | |
| `isComplete` | A boolean flag inside a function that starts at `false` and is set to `true` once at the end. | | |

-----

### 4\. Review & Mentor Feedback (10 min)

Please provide your captured results from the **Practice** section and your keyword choices and reasoning from the **Test** section.

I will then provide immediate feedback on your performance, clarify any weak spots (especially the `const` object nuance), and give you the green light to proceed to **Day 1, Hour 2: Arrow Functions**.
