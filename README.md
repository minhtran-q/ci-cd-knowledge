# CI/CD Knowledge

## Git flow
## Github Action
### Architecture

<details>
  <summary>Overview</summary>
  <br/>
  
  ![github_action_architecture](images/github_architecture.png)
  
</details>

<details>
  <summary>Key concepts</summary>
  <br/>

  + **Workflow:** A workflow is a configurable automated process that consists of one or more jobs.
  + **Events:** Events are specific activities in a repository that trigger workflows.
  + **Step:** Steps are individual tasks within a job. They can run commands or actions (reusable extensions).
  + **Actions:** Actions are reusable units of code that perform specific tasks. They can be used within steps to simplify workflows.
  + **Jobs:** A job is a set of steps that run as part of your workflow. Recall that a step can run a task, a command, or an action.
  + **Runner:** A runner is a machine, either hosted by GitHub or self-hosted, that executes the jobs in a workflow.
  
</details>

### Using Github Actions
