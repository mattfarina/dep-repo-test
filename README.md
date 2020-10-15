# Deprecated Repo Test

This is a test repository designed to test the idea of having a deprecated chart version that doesn't break an installed application but tells you the repository is deprecated and you can't install the upgrade.

Here's how you can test it....

## For Helm v3

```
helm repo add deprecated https://mattfarina.github.io/dep-repo-test/
helm install foo deprecated/wordpress --version 9.0.3
# Wait for it to come up if you want
helm upgrade foo deprecated/wordpress
```

You should get an error but the existing service running in Kubernetes is untouched.

## For Helm v2

```
helm repo add deprecated https://mattfarina.github.io/dep-repo-test/
helm install --name foo deprecated/wordpress --version 9.0.3
# Wait for it to come up if you want
helm upgrade foo deprecated/wordpress
```

You should get an error but the existing service running in Kubernetes is untouched.
