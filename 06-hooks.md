Pre and Post actions in Helm life action
* Run pods to perform some job
* Defined in the template
* Parents cannot override the subchart's hooks
* If a hook fails, everything fails
* You can have many


Samples:
* Load data
* Manipulate data
* Stage environments

When
* Pre/Post Install
* Pre/Post Delete
* Pre/Post Upgrade
* Pre/Post Rollback



```
apiVersion: v1
kind: Pod
metadata:
  name: posthooktainer
  annotations:
    "helm.sh/hook": "post-install"
    "helm.sh/hook-weight": "-5"
    "helm.sh/hook-delete-policy": hook-succeeded
spec:
  containers:
  - name: hooktainer
    image: busybox
    imagePullPolicy: IfNotPresent
    command: ['sh', '-c', 'echo post-install hook Pod is running && sleep 10']
  restartPolicy: Never
  terminationGracePeriodSeconds: 0
```