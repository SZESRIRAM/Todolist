# Ex03 To-Do List using JavaScript
## Date:08/08/26

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EXP 3</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="todo-container">
        <h1>My To Do List</h1>

        <div class="input-section">
            <input type="text" id="taskInput" placeholder="Enter a task">
            <button onclick="addTask()">Add Task</button>
        </div>

        <ul id="taskList"></ul>
    </div>

    <script>
        function addTask() {
            let input = document.getElementById("taskInput");
            let taskText = input.value.trim();

            if (taskText === "") {
                alert("Please enter a task!");
                return;
            }

            let li = document.createElement("li");

            li.innerHTML = `
                <span onclick="completeTask(this)">${taskText}</span>
                <button onclick="deleteTask(this)">Delete</button>
            `;

            document.getElementById("taskList").appendChild(li);

            input.value = "";
        }

        function completeTask(task) {
            task.classList.toggle("completed");
        }

        function deleteTask(button) {
            button.parentElement.remove();
        }
    </script>
</body>
</html>
```
style.css
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body {
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #667eea, #764ba2);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
.todo-container {
    background: white;
    width: 450px;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}
h1 {
    text-align: center;
    margin-bottom: 25px;
    color: #333;
}
.input-section {
    display: flex;
    gap: 10px;
}
#taskInput {
    flex: 1;
    padding: 12px;
    border: 2px solid #ddd;
    border-radius: 8px;
    font-size: 16px;
    outline: none;
}
#taskInput:focus {
    border-color: #667eea;
}
.input-section button {
    padding: 12px 18px;
    background: #667eea;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-size: 15px;
}
.input-section button:hover {
    background: #5568d9;
}
#taskList {
    list-style: none;
    margin-top: 25px;
}
#taskList li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #f5f5f5;
    padding: 12px 15px;
    margin-bottom: 10px;
    border-radius: 8px;
    font-size: 16px;
}
#taskList li span {
    cursor: pointer;
    flex: 1;
}
.completed {
    text-decoration: line-through;
    color: #888;
}
#taskList li button {
    background: #ff4d4d;
    color: white;
    border: none;
    padding: 8px 12px;
    border-radius: 6px;
    cursor: pointer;
}
#taskList li button:hover {
    background: #e63939;
}
```
## OUTPUT
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/68878917-4a08-43e3-9cde-bbe229592d8b" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
