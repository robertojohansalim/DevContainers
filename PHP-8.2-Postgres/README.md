## How to Use:
(MONO REPO APPROACH)
1. Put the `.devcontainer` at the top level of all the project directories
    ```
    /my-workspace
        ├── /project-1
        │   ├── node_modules
        │   └── package.json
        ├── /project-2
        │   ├── node_modules
        │   └── package.json
        └── /.devcontainer
            ├── devcontainer.json
            ├── compose.yaml
            └── Dockerfile
    ```
