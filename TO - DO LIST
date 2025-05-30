class Task:
    def __init__(self, description, completed=False):
        self.description = description
        self.completed = completed

    def __str__(self):
        status = "✓" if self.completed else " "
        return f"[{status}] {self.description}"

    def toggle_completion(self):
        self.completed = not self.completed

class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, description):
        task = Task(description)
        self.tasks.append(task)

    def remove_task(self, index):
        if 0 <= index < len(self.tasks):
            del self.tasks[index]

    def complete_task(self, index):
        if 0 <= index < len(self.tasks):
            self.tasks[index].toggle_completion()

    def show_tasks(self):
        if not self.tasks:
            print("No tasks.")
        else:
            for i, task in enumerate(self.tasks):
                print(f"{i + 1}. {task}")

    def save_tasks(self, filename):
        with open(filename, 'w') as f:
            for task in self.tasks:
                f.write(f"{task.description},{task.completed}\n")

    def load_tasks(self, filename):
        self.tasks = []
        with open(filename, 'r') as f:
            for line in f:
                description, completed = line.strip().split(',')
                completed = completed == 'True'
                self.tasks.append(Task(description, completed))

def main():
    todo_list = ToDoList()

    while True:
        print("\n==== To-Do List Menu ====")
        print("1. Add Task")
        print("2. Remove Task")
        print("3. Complete Task")
        print("4. Show Tasks")
        print("5. Save Tasks")
        print("6. Load Tasks")
        print("0. Exit")

        choice = input("Enter your choice: ")

        if choice == "0":
            print("Goodbye!")
            break
        elif choice == "1":
            description = input("Enter task description: ")
            todo_list.add_task(description)
        elif choice == "2":
            index = int(input("Enter task number to remove: ")) - 1
            todo_list.remove_task(index)
        elif choice == "3":
            index = int(input("Enter task number to complete: ")) - 1
            todo_list.complete_task(index)
        elif choice == "4":
            todo_list.show_tasks()
        elif choice == "5":
            filename = input("Enter filename to save tasks: ")
            todo_list.save_tasks(filename)
            print("Tasks saved successfully.")
        elif choice == "6":
            filename = input("Enter filename to load tasks from: ")
            todo_list.load_tasks(filename)
            print("Tasks loaded successfully.")
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
