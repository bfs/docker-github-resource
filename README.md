# Github Resource Server

Docker with a simple nginx server that serves up a repo it pulls from github

Environment variables:

- GITHUB_REPO (required)
- GITHUB_SSH_KEY (required)
- REFRESH (default 300)

You can then run via

```bash
docker run -p 80:80  --name github -e GITHUB_REPO="git@github.com:myorg/myrepo.git" -e GITHUB_SSH_KEY="`cat path_to_my_github_key`" -e REFRESH=30 boritzio/docker-github-resource
```