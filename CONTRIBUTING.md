# Contributing to PurgeBot

Thank you for taking the time to contribute! Here's how to get involved.

## Reporting bugs

Join the [support server](https://support.purgebot.net) and report the bug there. Include steps to reproduce, what you expected, and what actually happened.

## Suggesting features

Join the [support server](https://support.purgebot.net) and share your idea. Describe the use case clearly — the more context, the better.

## Contributing code

1. **Fork** the relevant repository and create a branch from `main`.
2. Follow the existing code style — run `go fmt ./...` before committing.
3. Keep changes focused. One concern per PR.
4. Don't add `replace` directives to `go.mod`.
5. Open a pull request against `main` and fill in the PR template.

All pull requests require review from `@PurgeBot-net/devs` before merging.

## Development setup

Each service is a standalone Go module. See the `README.md` in the relevant service directory for its specific configuration.

For local development across services, clone the repositories side by side. Then create a Go workspace in the folder that holds them, listing the ones you cloned:

```
go work init ./common ./database ./locale ./gateway
```

The service then builds against your local copies of `common`, `database`, and `locale`. The `go.work` file sits outside every repository, so it never gets committed. CI builds each repository on its own, against the versions pinned in `go.mod`.

## Questions?

Join the [support server](https://support.purgebot.net) and ask in the relevant channel.
