# AI-Based Task Manager Agent

This project implements an intelligent task management system that accepts tasks in natural language, categorizes them, organizes them based on priority and due dates, and manages them in a database.

## Features

- Natural language task processing
- Automatic categorization of tasks (work, personal, study, urgent)
- Priority determination based on language used
- Due date extraction from text
- Recurrence pattern recognition
- SQLite database for persistent storage
- Complete task lifecycle management (add, list, complete, delete)

## Architecture

The system is built using a modular architecture:

- **Database Layer**: Handles all database operations for storing and retrieving tasks
- **NLP Layer**: Processes natural language input to extract task properties
- **Task Manager**: Core business logic for task operations
- **User Interface**: (API endpoints for web/mobile applications or CLI interface)

## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/AI-Based-Task-Manager-Agent.git
cd AI-Based-Task-Manager-Agent
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

### Running the Application

```bash
python src/main.py
```

## Project Walkthrough Video

[Watch the project walkthrough video](https://vimeo.com/your-video-link)

## Usage Examples

```python
# Create a new task manager instance
manager = TaskManager()

# Add tasks using natural language
manager.add_task("Complete project report by tomorrow")
manager.add_task("Buy groceries every week")
manager.add_task("Study for exam on 05/15/2025")

# List all pending tasks
tasks = manager.list_tasks()
for task in tasks:
    print(f"ID: {task[0]}, Description: {task[1]}, Priority: {task[3]}, Due: {task[4]}")

# Complete a task
manager.complete_task(task_id)

# Delete a task
manager.delete_task(task_id)
```

## Project Structure

```
/
├── src/
│   ├── main.py                  # Application entry point
│   ├── database/
│   │   └── db_manager.py        # Database operations
│   ├── nlp/
│   │   └── processor.py         # Natural language processing
│   └── core/
│       └── task_manager.py      # Core business logic
├── utils/
│   └── logger.py                # Logging utilities
└── tests/
    └── test_task_manager.py     # Unit tests
```
