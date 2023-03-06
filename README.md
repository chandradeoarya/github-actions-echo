# Bash Echo & cli Workflow in Github Actions
This is a simple Github Actions workflow using the Bash echo command. This workflow will trigger on any push or pull request to the main branch, and simply print a message to the console using echo.


## Steps

These steps will teach how to write a basic bash echo workflow in Github Actions.

### **Step 1: Create a New Workflow**

1. Navigate to your Github repository and click on the "Actions" tab.
2. Click on the "Set up a workflow yourself" button.
3. This will open a new file in the **`.github/workflows`** directory of your repository.
4. Name the file **`echo-workflow.yml`**.

### **Step 2: Define the Workflow**

1. Copy and paste the following code into the **`echo-workflow.yml`** file:
```
name: Echo Workflow

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  echo-job:
    runs-on: ubuntu-latest
    steps:
    - name: Echo Message
      run: echo "Hello, DevOps!"
		- name: Multi line step
        run: |
          pwd
          ls

```
### Explaining the workflow file:

This workflow has a few different parts:

- **`name`** is the name of the workflow.
- **`on`** defines the event that triggers the workflow. In this case, the workflow will be triggered on any push or pull request to the **`main`** branch.
- **`jobs`** defines the different jobs that will run as part of the workflow.
- **`echo-job`** is the name of the job we are defining.
- **`runs-on`** specifies the operating system that the job will run on. In this case, we are using **`ubuntu-latest`**.
- **`steps`** defines the different steps that will be executed as part of the job.
- **`name`** is the name of the step.
- **`run`** specifies the command that will be run as part of the step. In this case, we are using the **`echo`** command to print a message to the console.

### **Step 3: Commit and Push the Workflow**

1. Once you have defined the workflow, commit and push the changes to your repository.
2. Navigate back to the "Actions" tab in your repository to view the status of your workflow.
3. You should see a new workflow called "Echo Workflow" that has been triggered by your push or pull request.

### **Step 4: View the Output**

1. Click on the "Echo Message" step in the workflow to view the output of the **`echo`** command.
2. You should see the message "Hello, DevOps!" printed to the console.
