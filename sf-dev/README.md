# Salesforce Dev Container

Using the official salesforce cli container with a few tweaks

---

## Guide to using container
Create a sf project using sf cli outside of container

```sf project generate --name MyProject```

Authorize org outside terminal

```sfdx force:project:create --projectname MyProject```

Install and open Docker Desktop

Create ```.devcontainer``` folder and put in ```Dockerfile``` and ```devcontainer.json```

Create `.ssh` folder in project root directory

Open the project in VS Code and run the ```Dev Containers: Reopen in Container``` command

Allow the container access to your authorized orgs
```bash
chmod 700 /root/.sfdx
chmod 600 /root/.sfdx/key.json
chmod -R go-rwx /root/.sfdx
```

---
## Notes

### Updated Java version
Using OpenJDK 21 instead of 11 that comes with the container

---

### Windows vs MAC
In `devcontainer.json` in mounts
- #### Windows
  - `source=${localEnv:USERPROFILE}/`
- #### Unix
  - `source=${localEnv:HOME}/`

---

After dev container is setup install code-analyzer
`sf plugins install @salesforce/plugin-code-analyzer`