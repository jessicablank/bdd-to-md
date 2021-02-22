# bdd-to-md

This cli tool scans for BDD feature spec files, written in Gherkin, and generates a markdown file out of them. Note this is converting the gherkin file itself and not the test output. 

## Dependencies

`npm i` to install dependencies. 

## Usage

Provide the generator command with a path containing the feature spec files, and the desired output filepath for the generated markdown.

Example:

```bash
node cli.js --featuresPath example-features --markdownFilePath FEATURES.md
```

This will result in the .feature files in the example-features folder being combined into one file. See the example result at [FEATURES.md](FEATURES.md)
