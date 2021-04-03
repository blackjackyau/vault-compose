## Vault compose
- Run in server mode with persistent behaviour
- initialise vault, unseal and retrieve root token via the UI (http://localhost:8200) 
- set the secret threashold to 1 (only 1 unseal token is required upon restarting)
- `docker-compose down` to shutdown down container (data will still be persisted)
- `docker-compose down -v` to shutdown down container including volume (data will be gone)
