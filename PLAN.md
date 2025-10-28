# 4-Week MERN Stack MVP Plan

This plan is optimized for local-only development over four weeks, focusing on mastering the MERN stack architecture and delivering a secure, functional CRUD MVP with the foundation for User Authentication.

| Week | Focus Area | Key Goal | Total Hours (L/D) |
| :--- | :--- | :--- | :--- |
| **Week 1** | **JS & React Native Core** | Master fundamentals; build the basic app screens/shell. | 34 hrs (17L / 17D) |
| **Week 2** | **Express API & Data Fetch** | Build the Node/Express API; connect to local MySQL; achieve secure **Read** access on mobile. | 35 hrs (11L / 24D) |
| **Week 3** | **CRUD & Mobile Forms** | Implement all **CRUD (Create/Update/Delete)** routes securely; finalize the mobile input forms. | 35 hrs (4L / 31D) |
| **Week 4** | **Web Admin & Auth Foundation** | Build the Web Admin view; start **User Authentication** logic; finalize the local MVP for hand-off. | 35 hrs (6L / 29D) |
| **OVERALL** | | | **139 hrs (38L / 101D)** |

## WEEK 1: JavaScript Mastery & React Native Core (Target: Frontend Shell)

| Day | Focus Area | Detailed Topics (Learn JIT) | Hours (L) Learning | Hours (D) Development | Daily Goal |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mon** | **JS Fundamentals 1** | `let`, `const`, Scoping, Arrow Functions. `export`/`import` (Modules). | 4 | 0 | Understand Modern JS variable & function syntax. |
| **Tue** | **JS Fundamentals 2** | Array Methods (`.map()`, `.filter()`, `.find()`). **(D) 1 hr:** Practice `map` on array of objects. | 4 | 1 | Master Array transformation (lists). |
| **Wed** | **JS Asynchronicity** | Promises, `async`/`await`. **(D) 1 hr:** Write a function that *simulates* API fetch. | 4 | 1 | Write functions to handle delayed data (API prep). |
| **Thu** | **React Component Core** | JSX Syntax, Functional Components, `Props`. **(D) 2 hrs:** Create first simple functional component. | 3 | 2 | Display a simple, hardcoded component list. |
| **Fri** | **State Management 1** | The `useState` Hook (State: the *changing* data). **(D) 3 hrs:** Create a simple counter and a text input field using state. | 2 | 3 | Master local component state and updates. |
| **Sat** | **Project Setup (MVP)** | **(D) 5 hrs:** Install Node/npm, Expo CLI. Initialize new Expo/RN project. Create Screen structure (`PatientList`, `AdmissionForm`). | 0 | 5 | **Project Milestone 1:** App is running on your phone via Expo Go; basic screens exist. |
| **Sun** | **Catch-up & Review** | **(L/D) 5 hrs:** Review Week 1 topics. Refactor component code. Apply basic layout to main screen. | 0 | 5 | Clean code; ensure main list screen mock-up looks good. |

## WEEK 2: Express API & MySQL Integration (Target: Secure Read Access)

| Day | Focus Area | Detailed Topics (L/D Focus) | Hours (L) Learning | Hours (D) Development | Daily Goal |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mon** | **Node.js/Express Setup** | **(L) 3 hrs:** Setting up Express: basic server, routes. **(D) 2 hrs:** Initialize Node project; install `express`, `cors`, `mysql2`. | 3 | 2 | Express server is running locally (e.g., on port 5000). |
| **Tue** | **Express-MySQL Connect** | **(L) 2 hrs:** Connect Express to local MySQL DB. **(D) 3 hrs (DB/Backend):** Write the initial **`SELECT * FROM patients`** route. | 2 | 3 | Express API successfully reads data from your local MySQL DB. |
| **Wed** | **Effects & Axios Fetching** | **(L) 1 hr:** The `useEffect` Hook. **(D) 4 hrs:** Implement the **Axios** library in RN to fetch data from your **local Express API**. | 1 | 4 | React Native successfully fetches data from the local Express server. |
| **Thu** | **Global State & Local Tunnel**| **(L) 2 hrs:** Context API / Zustand for global state. **(D) 3 hrs:** Move fetching logic to global state; test on a **physical phone** using Expo tunnel/local IP. | 2 | 3 | Mobile app displays live data reliably on a physical device. |
| **Fri** | **Data Display & Styling** | **(L) 1 hr:** React Native `FlatList`. **(D) 4 hrs:** Display live patient data in the `PatientList` screen; apply core styling. | 1 | 4 | Display the **first live list of data** (MVP Core 1). |
| **Sat** | **Navigation Implementation** | **(L) 2 hrs:** React Navigation (Stack). **(D) 3 hrs:** Implement navigation between `PatientList` and `AdmissionForm` screens. | 2 | 3 | User can move between the two main screens. |
| **Sun** | **Catch-up & Review** | **(L/D) 5 hrs:** Refactor code; ensure the **MySQL connection code is secure** and protected by a **`.env`** file. | 0 | 5 | **Project Milestone 2:** All data is displayed on mobile via the local, secure API. |

## WEEK 3: Data Input, CRUD, & Validation (Target: Secure Patient Admission)

| Day | Focus Area | Detailed Topics (L/D Focus) | Hours (L) Learning | Hours (D) Development | Daily Goal |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mon** | **Forms Library** | **(L) 2 hrs:** `react-hook-form` (basic usage). **(D) 3 hrs:** Setup basic form structure on `AdmissionForm`. | 2 | 3 | Simple form template ready with the library. |
| **Tue** | **Express: POST Route** | **(D) 5 hrs (DB/Backend):** Create the **POST** route (`/api/patients/add`). Implement robust **server-side validation** and sanitation. | 0 | 5 | Express endpoint securely accepts new patient data. |
| **Wed** | **Mobile Data Submission** | **(D) 5 hrs:** Write the `handleSubmit` function to **POST** data to the Express API. Clear the form/navigate back on success. | 0 | 5 | **MVP Core 2:** Successfully submit a new patient admission record. |
| **Thu** | **Update/Delete API** | **(D) 5 hrs (DB/Backend):** Implement **PUT/PATCH** (Update Status) and **DELETE** routes. Use **parameterized SQL queries** to prevent SQL Injection. | 0 | 5 | All server-side CRUD routes are secure and functional. |
| **Fri** | **Mobile Update/Delete** | **(D) 5 hrs:** Implement UI element (e.g., a swipe action or button) to trigger the Update/Delete API calls from the `PatientList`. | 0 | 5 | Admin can manage (Update/Delete) records from the mobile app. |
| **Sat** | **Styling & UX Polish** | **(L) 1 hr:** Advanced React Native Styling (Flexbox). **(D) 4 hrs:** Apply final Figma styling to the `AdmissionForm` screen (inputs, buttons). | 1 | 4 | App UI is professional; form looks complete. |
| **Sun** | **Catch-up & Review** | **(L/D) 5 hrs:** Thorough end-to-end testing (Create $\rightarrow$ Read $\rightarrow$ Update $\rightarrow$ Delete). Check API error handling. | 0 | 5 | **Project Milestone 3:** Full CRUD working on Mobile. Ready for Web Admin. |

## WEEK 4: Web Admin & Auth Foundation (Target: Local MVP Hand-off)

| Day | Focus Area | Detailed Topics (L/D Focus) | Hours (L) Learning | Hours (D) Development | Daily Goal |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mon** | **Web Admin View** | **(L) 2 hrs:** Setting up **`react-native-web`**. **(D) 3 hrs:** Replicate the `PatientList` screen for web admin access (Local browser). | 2 | 3 | Web admin panel displays live patient data in the local browser. |
| **Tue** | **Security & Keys** | **(L) 2 hrs:** Environment Variables (`.env`) usage in production. **(D) 3 hrs:** Ensure all paths point to `http://localhost:5000` or the local IP address for stability. | 2 | 3 | All local credentials are secure and abstracted via `.env`. |
| **Wed** | **Final Testing & Debugging** | **(D) 5 hrs:** Manual testing on all platforms (iOS, Android, Chrome, Edge). Fix all remaining UI/API bugs. | 0 | 5 | App is stable on all local target platforms. |
| **Thu** | **Auth Foundation: DB/API** | **(L) 2 hrs:** Basics of Token-based Auth (JWT). **(D) 3 hrs (DB/Backend):** Create **`Users`** table in MySQL. Add **POST `/api/register`** route in Express. | 2 | 3 | **Auth Milestone 1:** Backend can securely register a new user locally. |
| **Fri** | **Auth Foundation: Frontend** | **(D) 5 hrs:** Create **Login/Register** screens in React Native. Implement frontend logic to send credentials to the local **`/api/register`** route. | 0 | 5 | Frontend screens are ready to interact with the new local Auth routes. |
| **Sat** | **Demo Prep & Documentation** | **(D) 5 hrs:** Conduct a dry-run of the stakeholder presentation. **Create Deployment README** (SQL dump, `.env` guide, API hosting links). | 0 | 5 | Demo materials polished; all deployment docs created. |
| **Sun** | **MVP Finalization & Hand-off** | **(D) 5 hrs:** Final code cleanup. Package all files for local hand-off. **Prepare plan for the next iteration (User Login/Auth completion).** | 0 | 5 | **MVP is 100% complete locally.** Ready for the single "go-live" step next week. |
