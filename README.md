# MyWildCloud.org

## Dev environment

- Install hugo.
- Install dart-sass.

```bash
hugo server
```

## Deploy

```bash
hugo build
docker build -t payneio/mywildcloud.org . --file ./Dockerfile
docker push payneio/mywildcloud.org

source load-env.sh

# First time...
# Add wildcloud deploy setup here.

# Update...
kubectl rollout restart deployment mywildcloud -n mywildcloud
```
