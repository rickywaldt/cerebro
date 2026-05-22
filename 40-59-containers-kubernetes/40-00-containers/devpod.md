## Port forward

```
kubectl port-forward deployment/test 8080:8080
```

This means that port 8080 in the container running in the pod that's managed by the deployment is reachable from port 8080 on the localhost. Curl works great, but when you need to authenticate via a browser in a devpod cli, you're out of luck. The fix is to run the following:

```
devpod ssh <workspace> -L 8080:localhost:8080
```

Essentially adding another port-forward to the devpod. This way you can open a browser on your host machine and go to localhost:8080 to get to localhost:8080 from in the devpod.

In my case: Mac > devpod > container
