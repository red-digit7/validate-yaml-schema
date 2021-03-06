# Validate YAML Schema

This action validates YAML files using the `yaml.schemas` settings for the [VS Code YAML Extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

All you need is a **.vscode/settings.json** document at the root of the repository that contains the `yaml.schemas` setting

## Outputs

### `invalidFiles`

A comma separated list of files that failed the schema validation.  

 > Schema validation fails if any results are returned from the YAML Language Server

## Example usage
 You'll need to precede the action with `actions/checkout@v2` as this action will read files from the [GITHUB_WORKSPACE directory](https://help.github.com/en/actions/configuring-and-managing-workflows/using-environment-variables)

    steps:
      - uses: actions/checkout@v2
      - uses: nwisbeta/validate-yaml-schema@v1.0

## Thanks
This action has been made by 're-mixing' logic from these repos: 
 - https://github.com/OrRosenblatt/validate-json-action 
 - https://github.com/redhat-developer/yaml-language-server
