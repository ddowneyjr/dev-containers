## Salesforce Dev Container

Using the official salesforce cli container with a few tweaks

### Updated Java version
Using OpenJDK 21 instead of 11 that comes with the container

### Windows vs MAC
In `devcontainer.json` in mounts
- #### Windows
  - `source=${localEnv:USERPROFILE}/`
- #### Unix
  - `source=${localEnv:HOME}/`

