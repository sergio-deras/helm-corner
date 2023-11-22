`helm test <name>`
When the release is running

```
apiVersion: v1
kind: Pod
metadata:
  name: '{{ include "web.fullname" . }}-test-connection'
  annotations: "helm.sh/hook": test
spec:
  containers:
  - name: wget
    image: busybox
    command: ['wget']
    args: ['{{ include "web.fullname" . }}:{{ .Values.service.port }}']
  restartPolicy: Never
```
```
apiVersion: v1
kind: Pod
metadata:
  name: "{{ .Values.Blog.name }}-credentials-test"
  annotations:
    "helm.sh/hook": test
spec:
  containers:
    - name: wget
      image: busybox
      imagePullPolicy: Always
      command: ['wget']
      args: ['{{ .Values.Blog.name }}:{{ .Values.Service.port }}']
  restartPolicy: Never
```