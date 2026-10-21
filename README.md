# Task Manager

A simple task management system with a fully automated CI/CD pipeline on GitHub Actions:

- **Task management logic:** `todo.py` has the `Task` and `TaskPool` classes, which create tasks and track their status ("ToDo" or "Done").
- **Automated unit testing:** `todo-test.py` checks task creation, status updates, and filtering tasks by status.
- **index.html report:** `update_index.sh` writes the ToDo and Done task lists and the unit test results into `index.html`.
- **Docker:** the `Dockerfile` packages the application with everything the scripts need, and `entrypoint.sh` runs all the scripts.
- **Automated testing and deployment:** `ci.yml` builds the Docker image and runs it on every push to `main`, so the tests run and `index.html` is updated automatically.
- **Issue tracking automation:** when a pull request is merged, `tracker.yml` moves the issue it closes to "Done" on the GitHub Projects board.
