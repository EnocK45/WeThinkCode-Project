# Task Manager Assignment

---

## Exercise 1: Function Understanding

### Prompt
Explain the following Python function in simple terms. Focus on:
1. What the function does  
2. The purpose of each parameter  
3. What it returns  
4. Any important logic or validation  

### Response
The `create_task` function is used to create a new task in the system. It takes inputs such as title, description, priority, due date, and tags.

- title: The name of the task  
- description: Extra details about the task  
- priority_value: The importance level of the task  
- due_date_str: The due date in string format (YYYY-MM-DD)  
- tags: A list of labels for the task  

The function converts the priority into a priority object and attempts to convert the due date string into a date format. If the date format is incorrect, it prints an error and returns None.

If everything is valid, a new Task object is created and saved using the storage system. The function then returns the unique ID of the created task.

---

## Exercise 2: API Documentation

### Prompt
Please create comprehensive documentation for this API endpoint.

### Response

Endpoint: POST /tasks  

Description:  
This endpoint creates a new task in the task management system.

Request Parameters:
- title (string): Task title  
- description (string): Task description  
- priority_value (int): Priority level  
- due_date_str (string): Due date (YYYY-MM-DD)  
- tags (list): Task tags  

Response (Success):
{
  "task_id": 1,
  "message": "Task created successfully"
}

Response (Error):
{
  "error": "Invalid date format. Use YYYY-MM-DD"
}

Authentication:
No authentication is required.

---

## Exercise 3: Code Logic Analysis

### Prompt
Explain the intent and logic behind this code.

### Response

The code defines a TaskManager class that manages tasks in a task management system.

- It allows creating, updating, deleting, and viewing tasks.
- The create_task method creates new tasks and saves them.
- The list_tasks method retrieves tasks.
- The update_task_status method updates task status.

The system uses a storage component (TaskStorage) to store tasks.

Assumptions and Edge Cases:
- Date must be in YYYY-MM-DD format  
- Invalid date returns error  
- Task must exist to update/delete  

Improvements:
- Better error handling  
- Input validation  
- Use logging instead of print  

---