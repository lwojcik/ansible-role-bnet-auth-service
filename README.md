# ansible-role-bnet-auth-service

Ansible role for installing and launching [bnet-auth-service](https://github.com/sc2pte/bnet-auth-service) instance on Debian-based server.

Requires Nginx, Redis, Node.js and pm2 installed on the server. It *does not* install them automatically.

It builds the app from Git repository and generates backup of the previous deployment if available.

## Variables

| Variable name | Sample value | Description |
|-  |-  |-
| `bas_deploy_directory` | `/home/deploy/bnet-auth-service` | Directory used to deploy project |
| `bas_backup_directory` | `/home/deploy/backups/bnet-auth-service` | Directory used to generate backups of previous deployments as tgz files |
| `BAS_NODE_ENV` | `production` | Environment type |
| `BAS_NODE_HOST` | `localhost` | Project host |
| `BAS_NODE_PORT` | `8888` | Project port |
| `BAS_REDIS_ENABLE` | `true` | Enable / disable Redis cache |
| `BAS_REDIS_HOST` | `127.0.0.1` | URL of Redis instance used to store cached data |
| `BAS_REDIS_PORT` | `6379` | Port of Redis instance used to store cached data |
| `BAS_REDIS_PASSWORD` | `some_password` | Redis password |
| `BAS_REDIS_TTL` | `999999` | Expiration time of Redis-stored keys |
| `BAS_REDIS_DB` | `0` | Id of Redis database |
| `BAS_REDIS_CACHE_SEGMENT` | `bnet-token` | Name of Redis cache segment used by the project |
| `BAS_BATTLENET_REGION` | `us` | Battle.net API region to get data from |
| `BAS_BATTLENET_KEY` | `some_key` | Battle.net client key |
| `BAS_BATTLENET_SECRET` | `some_secret` | Battle.net client secret |
