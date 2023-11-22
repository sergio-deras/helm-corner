`helm repo add <repo_name> <repo>`: Add a repository of charts

`helm repo update`: Refresh your repo

`helm repo remove <repo_name>`

`helm fetch <chart>`: Get a chart in

`helm search repo <chart>`: Search for a chart in a repo

`helm install <release_name> <chart>`

`helm install <repo/chart> --generate-name`

`helm show chart <chart>`

`helm show all <chart>`

`helm ls`: see what has been released

`helm status`

`helm upgrade <release_name> <path>`:  Apply changes to a chart

`helm rollback`: Revert previous release

`helm delete <release_name>` || `helm uninstall <release_name>` (alias)


`helm package --sign --key <name> --keyring <signed_key_path> <chart_path>`

`helm verify <file_path>`


`helm test <name>`


*release_name is the ID