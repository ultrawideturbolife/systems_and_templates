💡 *Although often desired not every bug or new functionality needs a fully filled out template. Some topics may not always apply or are too obvious to be filled in for that specific ticket. So, feel free to remove sections as needed or leave ‘N/A’ to indicate that it’s not applicable. Also please note that the structure of given subjects are mere guidelines, if you feel a subject would be better explained in plain sentences, drawings or a whole different way then by all means feel free to remove the initial structure and implement it as you see fit.*

# ⁉️ Questions

---

⛔ *Questions and/or pressing matters in here need to be resolved as soon as possible, preferably before or shortly after starting the ticket.*


- N/A

# 🔖 Description

---

💡 *A short and descriptive introduction of the problem we are going to solve.*


- N/A

# 🗣 User Story

---

💡 ***As a** ROLE **I want** BEHAVIOUR s**o that** REASON.*


- **What:**
    - N/A
- **Why:**
    - N/A

# ⚙️ Requirements

---

💡 *Functional requirements define what the system does or must not do, non-functional requirements specify how the system should do it. Do X (functional) within 5 seconds (non-functional).*


- **Functional:**
    - N/A
- **Non-Functional:**
    - N/A

# 💾 Data Model

---

💡 *Old and new data models that will be created and/or altered when this feature is added. Describe the new name and location of the model as well as any fields that are new or will be removed. Show a JSON for easy reference. Use [https://beta5.objgen.com/json?demo=true](https://beta5.objgen.com/json?demo=true) for quick JSON generation.*


- **Name:** ExampleName
    - **Description:** N/A
    - **ObjGen:**

        ```yaml
        
        ```

    - **JSON:**

        ```json
        
        ```


# 🔒 Security Rules

---

💡 *Old and new security rules with roles and access that will be created and/or altered when this feature is added.*


- **Collection:** ExampleCollection
    - **Access & Conditions**: ExampleAccessIfExampleCondition

    ```
        match /Collection/{documentId} {
          allow get, list: if request.auth != null;
        }
    ```


# 🐒 API

---

💡 *Anything related to new API calls. Copy/paste the template and/or components inside the template to cover all new endpoints, requests and responses. Use [https://beta5.objgen.com/json?demo=true](https://beta5.objgen.com/json?demo=true) for easy JSON generation.*


- **Name:** CreateExample
    - **Description:** N/A
    - **Type:** GetPutPostDelete
    - **Endpoint:** ExampleEndpoint
    - **Request body:**

        ```json
        
        ```

    - **200 response:**

        ```json
        
        ```

    - **Other responses 200/400/500:**

        ```json
        
        ```


# 📊 Analytics

---

💡 *Name preferably ends with a verb. The ‘When’ describes when this analytic is fired and ‘Properties’ describe the map of properties that’s sent along with the analytic. Use [https://beta5.objgen.com/json?demo=true](https://beta5.objgen.com/json?demo=true) for easy properties (JSON) generation.*


- **Name:** example_created
    - **When:** When.
    - **Properties:**

        ```json
        {
          "state": true,
          "days": "6,7",
          "time": "2021-08-29T18:06:13.051Z"
        }
        ```


# ⚡️ Integration Tests

---

💡 *Check out [https://cucumber.io/docs/gherkin/reference/](https://cucumber.io/docs/gherkin/reference/) for more info.*


- **What to test and why?**
    - N/A
- **Ideas for different scenarios?**
    - N/A
- **Ideas for different examples?**
    - N/A

# 👾 Unit Tests

---

💡 *Components that would benefit from separate unit tests and which scenario's should be tested.*


- **What to test and why?**
    - N/A
- **Ideas for different scenarios?**
    - N/A
- **Ideas for different examples?**
    - N/A

# **👨‍🔧 Current Tests**

---

💡 *Integration and/or unit tests components that need an upgrade when this feature is added.*


**Any existing tests that need to be updated?**

- N/A

# 🎨 UI/UX Behaviour

💡 *Anything to take note of regarding the behaviour of UI/UX elements (if applicable). Think of position, behaviour when elements do not fit the screen, feedback on elements and properties of animations.*


- N/A

# 📝 Suggested Approach

---

💡 *With knowledge of the current codebase, try to define a best suggested approach. Think of current components used, flow of data and UI elements.*


- [ ]  TODO

# 👉️ Final Remarks

---

⚠ *Anything to take note off that is not properly defined yet. Think of out of scope notes, dependencies, anything to be extra cautious about and/or information about related issues.*


- N/A
