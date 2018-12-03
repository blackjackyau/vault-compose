## This vault compose will setup secret api v1 instead of v2
- Credit to input from https://github.com/hashicorp/docker-vault/issues/111
- `docker-compose up` to run
- To create an entry
    - Method: POST
    - Path: http://${dockerhostname}:8200/v1/secret/my-secret
    - Headers: "Content-Type: application/json", "X-Vault-Token: $VAULT_TOKEN"
    - Body: {"first": "you found me"}
- To query secret
    - Method: GET
    - Path: http://${dockerhostname}:8200/v1/secret/my-secret
    - Headers: "X-Vault-Token: $VAULT_TOKEN"