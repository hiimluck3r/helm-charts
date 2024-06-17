```bash
kubectl -n default create secret generic basic-auth \
--from-literal=redis-password=redis \
--from-literal=mariadb-password=maria \
--from-literal=mariadb-root-password=root \
--from-literal=mariadb-replication-password=replication \
--dry-run=client \
-o yaml > basic-auth.yaml
```

1. can't connect to headless service, switch to standalone?
2. castopod keeps failing
3. Can't reach via reverse-proxy (no route)