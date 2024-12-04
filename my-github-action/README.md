# My GitHub Action

This repository contains a GitHub Action that performs specific tasks when triggered. 

## Overview

The GitHub Action is designed to automate workflows in your GitHub repository. It is built using TypeScript and can be customized to fit your needs.

## Files

- **src/main.ts**: Contains the main logic for the GitHub Action. This file exports a function that will be executed when the action is triggered.
- **.github/workflows/action.yml**: Defines the workflow for the GitHub Action, specifying the event that triggers the action and the steps to execute.
  - Checks out the code
  - Creates a branch called `prr`
  - Creates a directory `.cai` and a file `prr.md` inside it
  - Checks if `.componentId` exists and extracts its value
  - Checks if `.component` exists and extracts its value
  - Calls a REST endpoint and stores the JSON response if the HTTP status code is 200
- **tsconfig.json**: Configuration file for TypeScript.

## Inputs

- **input_component**: Input component (required)
- **input_component_id**: Input component ID (required)

## Usage

To use this GitHub Action in your repository, include it in your workflow YAML file and specify the necessary inputs.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.