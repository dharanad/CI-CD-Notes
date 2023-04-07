# Notes
GitHub Actions is a continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline.

GitHub Actions goes beyond just DevOps and lets you run workflows when other events happen in your repository. For example, you can run a workflow to automatically add the appropriate labels whenever someone creates a new issue in your repository.

Your workflow contains one or more jobs which can run in sequential order or in parallel.
Each job will run inside its own virtual machine runner, or inside a container, and has one or more steps that either run a script that you define or run an action, which is a reusable extension that can simplify your workflow.

![Components of Github Actions](https://docs.github.com/assets/cb-25535/mw-1000/images/help/actions/overview-actions-simple.webp)

### Workflow
A workflow is a configurable automated process that will run one or more jobs. Workflows are defined by a YAML file checked in to your repository and will run when triggered by an event in your repository, or they can be triggered manually, or at a defined schedule.

Workflows are defined in the `.github/workflows` directory in a repository, and a repository can have multiple workflows, each of which can perform a different set of tasks.


### Events
An event is a specific activity in a repository that triggers a workflow run.
You can also trigger a workflow to run on a schedule, by posting to a REST API, or manually.
[Events that trigger workflows](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows)

### Jobs
A job is a set of steps in a workflow that is executed on the same runner. Each step is either a shell script that will be executed, or an action that will be run.
Since each step is executed on the same runner, you can share data from one step to another. For example, you can have a step that builds your application followed by a step that tests the application that was built.
You can configure a job's dependencies with other jobs; by default, jobs have no dependencies and run in parallel with each other. When a job takes a dependency on another job, it will wait for the dependent job to complete before it can run.

### Action
An action is a custom application for the GitHub Actions platform that performs a complex but frequently repeated task. Use an action to help reduce the amount of repetitive code that you write in your workflow files.

An action can pull your git repository from GitHub, set up the correct toolchain for your build environment, or set up the authentication to your cloud provider.
[Creating actions](https://docs.github.com/en/actions/creating-actions)

### Runners
A runner is a server that runs your workflows when they're triggered. Each runner can run a single job at a time. GitHub provides Ubuntu Linux, Microsoft Windows, and macOS runners to run your workflows; each workflow run executes in a fresh, newly-provisioned virtual machine.

## Appendix
Demo Action [Logs](https://pipelines.actions.githubusercontent.com/serviceHosts/de1dfcc8-5828-4b3b-9430-d46aa4935886/_apis/pipelines/1/runs/2/signedlogcontent/2?urlExpires=2023-04-07T17%3A57%3A53.7512026Z&urlSigningMethod=HMACV1&urlSignature=wIn%2Fc1KpWSuW%2FLnKrc%2BGqommlbfJu7M3Wh6nOUN%2FclM%3D)