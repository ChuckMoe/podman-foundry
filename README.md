# Image
The image used was created by [felddy](https://hub.docker.com/r/felddy/foundryvtt). For all variable descriptions, go there.

# Volumes
Change the volumes.hostPath.path to the directory where you want to save and access all the data available to Foundry. If you do not want or need direct access, you can instead use:

```yaml
volumes:
  - name: data
    persistentVolumeClaim:
          claimName: foundry-data
```

# Commands

Start Foundry
```bash
podman play kube --configmap=secrets.yaml pod.yaml
```

Stop Foundry
```bash
podman play kube --down pod.yaml
```

To update Foundry, aka. use the newest container, just stop and start again.
