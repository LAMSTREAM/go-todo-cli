
# Go Todo CLI App

A simple command-line Todo list application written in Go. This CLI app allows you to manage your tasks by adding, completing, deleting, and listing todos. The todos are stored in a local `.todo.json` file.

## Features

- **Add a new task**: Add a new todo to the list.
- **Mark a task as completed**: Mark a specific todo by its index as completed.
- **Delete a task**: Delete a todo by its index.
- **List all tasks**: View all your tasks, including their statuses.

## Prerequisites

- Go 1.18 or higher installed on your system.

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/go-todo-cli.git
   cd go-todo-cli
   ```

2. Build the app:

   ```bash
   go build -o todo-cli
   ```

   This will generate an executable file named `todo-cli`.

## Usage

### Adding a Task

To add a new todo task, use the `--add` flag followed by the task description. If you don't provide the task description as a flag argument, you will be prompted to enter it.

```bash
./todo-cli --add "Buy groceries"
```

### Completing a Task

To mark a todo as completed, use the `--complete` flag followed by the index of the task you want to complete. For example, to complete the first task:

```bash
./todo-cli --complete 1
```

### Deleting a Task

To delete a task, use the `--del` flag followed by the index of the task to delete:

```bash
./todo-cli --del 2
```

### Listing All Tasks

To view all tasks and their statuses, use the `--list` flag:

```bash
./todo-cli --list
```

## File Storage

Todos are saved in the `.todo.json` file in the same directory. Each task includes a description and a status (completed or not).

## Error Handling

- If a task description is empty when adding a new task, an error will be thrown.
- If the index provided for completing or deleting a task is invalid, an error will be thrown.

## Example Workflow

1. Add a new task:

   ```bash
   ./todo-cli --add "Complete Go project"
   ```

2. List tasks:

   ```bash
   ./todo-cli --list
   ```

3. Complete the task:

   ```bash
   ./todo-cli --complete 1
   ```

4. List tasks again:

   ```bash
   ./todo-cli --list
   ```

5. Delete a task:

   ```bash
   ./todo-cli --del 1
   ```
