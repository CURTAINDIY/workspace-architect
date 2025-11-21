# GitHub Copilot Packed

A collection of instructions, prompts, and chat modes for GitHub Copilot, accessible via CLI.

## Usage

You can use this tool directly with `npx` without installing it:

```bash
npx github-copilot-packed download instructions:basic-setup
```

### Commands

#### List Available Assets

```bash
npx github-copilot-packed list
# or list specific type
npx github-copilot-packed list instructions
```

#### Download an Asset

```bash
npx github-copilot-packed download <type>:<name>
```

Example:
```bash
npx github-copilot-packed download prompts:code-review
```

Options:
- `-d, --dry-run`: Simulate the download without writing files.
- `-f, --force`: Overwrite existing files without asking.
- `-o, --output <path>`: Specify the output path (default: `.github/<type>`).

## Development

### Local Testing

1. Install dependencies:
   ```bash
   npm install
   ```

2. Run the CLI locally:
   ```bash
   node bin/cli.js list
   ```

3. Link the package to test `npx` behavior locally (simulated):
   ```bash
   npm link
   npx github-copilot-packed list
   ```

## Adding New Assets

1. Create a new markdown file in `assets/instructions`, `assets/prompts`, or `assets/chatmodes`.
2. The file name will be the ID used for downloading (e.g., `assets/instructions/my-guide.md` -> `instructions:my-guide`).
