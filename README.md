# Lean 4 Project Template

A minimal, simple template for Lean 4 development with mathlib support and GitHub Codespaces configuration.

## Features

- ✅ Lean 4 with latest stable version
- ✅ mathlib integration
- ✅ GitHub Codespaces support
- ✅ VS Code configuration
- ✅ Example theorems and proofs
- ✅ Minimal project structure

## Quick Start

### Option 1: GitHub Codespaces (Recommended)

1. Click the "Code" button on this repository
2. Select "Create codespace on main"
3. Wait for the environment to set up automatically
4. Open `main.lean` to start coding

### Option 2: Local Development

1. Install Lean 4:
   ```bash
   curl -L https://raw.githubusercontent.com/leanprover/elan/master/elan-init.sh -sSf | sh -s -- -y --default-toolchain leanprover/lean4:stable
   ```

2. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd lean-project-template
   ```

3. Build the project:
   ```bash
   lake build
   ```

4. Open in VS Code with the Lean 4 extension

## Project Structure

```
lean-project-template/
├── .devcontainer/           # Dev container setup scripts
├── lakefile.lean           # Lake build configuration
├── lean-toolchain          # Lean version specification
├── main.lean              # Main library file
├── README.md               # This file
└── .gitignore             # Git ignore rules
```

## Development

- **Main file**: `main.lean` contains example theorems and proofs
- **Dependencies**: mathlib is automatically included via `lakefile.lean`
- **Build**: Use `lake build` to compile the project
- **Clean**: Use `lake clean` to remove build artifacts

## Example Code

The template includes a simple example from the Lean documentation:

```lean
theorem and_commutative (p q : Prop) : p ∧ q → q ∧ p :=
  fun hpq : p ∧ q =>
  have hp : p := And.left hpq
  have hq : q := And.right hpq
  show q ∧ p from And.intro hq hp
```

## VS Code Configuration

The Codespace is pre-configured with:
- Lean 4 extension
- Proper workspace settings
- Git integration

## Contributing

1. Fork this template
2. Create your feature branch
3. Make your changes
4. Test with `lake build`
5. Commit and push

## Resources

- [Lean 4 Documentation](https://leanprover.github.io/lean4/doc/)
- [mathlib Documentation](https://leanprover-community.github.io/mathlib4_docs/)
- [Lean 4 Tutorial](https://leanprover.github.io/lean4/doc/tutorial.html)
- [Lean Community](https://leanprover-community.github.io/)

## License

This template is open source and available under the MIT License.