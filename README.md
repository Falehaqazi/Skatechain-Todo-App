# Skatechain To-Do App

This project is a simple to-do list application built using Skatechain's stateless infrastructure. The app will allow users to add, complete, and delete tasks without relying on a centralized server.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Skatechain To-Do List</title>
    <script>
        function addTask() {
            var taskText = document.getElementById("new-task").value;
            if (taskText !== "") {
                var taskList = document.getElementById("task-list");
                var newTask = document.createElement("li");
                newTask.innerHTML = '<input type="checkbox"> ' + taskText + ' <button onclick="deleteTask(this)">Delete</button>';
                taskList.appendChild(newTask);
                document.getElementById("new-task").value = ""; // Clear the input box
            }
        }

        function deleteTask(button) {
            var task = button.parentElement;
            task.remove();
        }
    </script>
</head>
<body>
    <h1>Skatechain To-Do List</h1>
    <input type="text" id="new-task" placeholder="What do you need to do?">
    <button onclick="addTask()">Add Task</button>
    <ul id="task-list"></ul>
</body>
</html>

