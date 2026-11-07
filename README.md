# Devcontainers

A collection of lightweight, reusable development container images for consistent development environments across projects and machines.

## Available Environments

| Environment | Description | Image |
|---|---|---|
| Typst | Typst compiler and Tinymist language server | `ghcr.io/NicolaiKuertoes/typst:latest` |

## Usage

Add a `.devcontainer/devcontainer.json` file to your project:

```json
{
  "name": "Typst",
  "image": "ghcr.io/NicolaiKuertoes/typst:latest",
  "customizations": {
    "vscode": {
      "extensions": [
        "myriad-dreamin.tinymist"
      ]
    }
  }
}
```

Open your project in Visual Studio Code and select **Dev Containers: Reopen in Container**.

## Automatic Updates

Images are automatically built and published to GitHub Container Registry using GitHub Actions.

- **Scheduled builds:** Weekly.
- **Manual builds:** Available through GitHub Actions.
- **Triggered builds:** When relevant Dockerfiles or workflow files change.
- **Image registry:** [GitHub Container Registry](https://ghcr.io/)

The `latest` tag always points to the most recently published image.

## Repository Structure

```text
.
├── .github/
│   └── workflows/
│       └── typst.yml
└── typst/
    └── Dockerfile
```

## Contributing

Contributions, improvements, and suggestions are welcome. Feel free to open an issue or submit a pull request.

## License

See [LICENSE](LICENSE) for details.