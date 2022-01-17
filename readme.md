# spaCy VSCode Utils

This repo contains some files that should help when working with spaCy inside VSCode.

## Validating project.yml with JSON Schema

This repo includes a JSON Schema for spaCy Projects, which allows you to validate your `project.yml` files using the [YAML extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml). This will also enable autocomplete and hover tool tips for the 

Eventually this will be included in [JSON Schema Store](https://www.schemastore.org/json/), which allows you to referece it by name in VSCode. Until then, you can install via the following:

```
curl -O https://raw.githubusercontent.com/pmbaumgartner/spacy-vscode-utils/main/spacy-project.json
```

And then reference the file like this in the `./vscode/settings.json` file:

```
{
    // Requires the YAML (redhat.vscode-yaml) VSCode Extension 
    // Once this schema is in schema store, you'll change this
    "yaml.schemas": {
        "./spacy-project.json": "project.yml"
    },
}
```

## WIP: Tasks

The `./vscode/tasks.json` file includes common spaCy CLI commands as VSCode Tasks so they can be excuted from the command palette.
