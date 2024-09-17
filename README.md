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

<details>
  <summary>Managing Secrets</summary>
  <br/>
  
  **Manage:**
  
  1. Go to your repository on GitHub.
  2. Click on the **Settings** tab.
  3. In the left sidebar, click on **Secrets and variables > Actions**.
  4. Click on **New repository secret**.
  5. Add a name for your secret and its value, then click Add secret.

  **Use:**

  To use a secret in your workflow, reference it in your YAML file like this:
  ```
  jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Use secret
      run: echo ${{ secrets.MY_SECRET }}
  ```

  _Note:_ Always use secrets for sensitive information like API keys, tokens, and passwords.
</details>

<details>
  <summary>Managing Environment Variables</summary>
  <br/>

  **Environment-Specific Variables:** Navigate to **Settings > Environments**, create an environment.
  **Environment Variables in Workflow:** You can define environment variables directly in your workflow file.

  ```
  jobs:
    build:
      runs-on: ubuntu-latest
      env:
        MY_VARIABLE: 'value'
      steps:
      - name: Checkout code
        uses: actions/checkout@v2
  
      - name: Use environment variable
        run: echo $MY_VARIABLE
  ```
</details>
<details>
  <summary>Caching</summary>
  <br/>


</details>
