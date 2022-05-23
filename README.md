# Tekton is Groovy

This is the supporting code repository for the blog post located at https://blog.kywa.io/tekton-is-groovy

## Using the `buildah` Task

The `buildah` Task has 2 `Secret` requirements:

* The `git` repository (SSH)
* The Container registry auth

With each of these in the namespace, the `PipelineRun` can be applied

## `tkn` CLI commands

### Run `basic-task`
To run the `basic-task` Tekton `Task`, you can run the following:

```sh
tkn task start basic-task -p URL=https://github.com
```

### Run `basic-pipeline`
To run the `basic-pipeline` which calls a single `Task`, `basic-task`:

```sh
tkn pipeline start basic-pipeline -p URL=https://github.com
```
