
```shell
wget https://github.com/kubernetes-sigs/kustomize/releases/download/v3.2.0/kustomize_3.2.0_linux_amd64
chmod +x kustomize_3.2.0_linux_amd64
mv kustomize_3.2.0_linux_amd64 /usr/local/bin/kustomize

while ! kustomize build example | kubectl apply -f -; do echo "Retrying to apply resources"; sleep 10; done
```
