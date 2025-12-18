# Homebrew: Code Collector Tap

Homebrew tap for installing [Code Collector](https://github.com/MikhailOnyanov/code-collector), a CLI that recursively gathers source files into a single text file for sharing with LLMs or other tools that need project context.

## Installation
- Add the tap: `brew tap MikhailOnyanov/brew-code-collector`
- Install the CLI: `brew install code-collector`

## Usage
- Run the tool after installation with `collect-code ...` (it is symlinked into your `PATH` by Homebrew).
- See available flags and examples: `collect-code --help`
- Typical flow: point the command at a directory and write the collected output to a file you can paste into your LLM of choice.

## Maintenance
- Upgrade to the latest release: `brew upgrade code-collector`
- Remove if you no longer need it: `brew uninstall code-collector`

## Development Notes
- This tap installs the Python-based `collect-code` script shipped with the upstream project (Python 3.12 is declared as a dependency in the formula at `Formula/code-collector.rb`).
- To verify the formula locally you can run Homebrew checks:
  - `brew test code-collector` to execute the formula’s test block.
  - `brew audit --strict code-collector` to lint the formula.

## Feedback
Issues or feature requests for the CLI itself should go to the upstream repository: [MikhailOnyanov/code-collector](https://github.com/MikhailOnyanov/code-collector). Formula or tap problems can be opened here via GitHub issues or pull requests.
