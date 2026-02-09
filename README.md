# example-csharp

[![view-action-graph](https://img.shields.io/github/actions/workflow/status/actionforge/example-csharp/workflow.yml?label=View%20Action%20Graph)](https://app.actionforge.dev/github/actionforge/example-csharp/main/.github/workflows/graphs/build.act)

A simple Hello World app in C#, built using an [Actionforge](https://actionforge.dev) graph as the CI/CD pipeline.

## Run

```bash
dotnet run
```

## Graph

The build pipeline is defined as an Actionforge graph in [`.github/workflows/graphs/build.act`](.github/workflows/graphs/build.act):

```
checkout -> run (dotnet publish -c Release -o build/) -> upload-artifact (build/)
```

It runs on every push to `main`, on pull requests, and on manual dispatch.
