Hosted docs URL: https://bosemangroup.github.io/weightless-slate-rest-docs

Framework docs: https://github.com/slatedocs/slate

#### Update docs
- Modify open api file: weightless.yaml
```
npm install -g widdershins
```
-  convert open api file: weightless.yaml to slate doc format:
```
widdershins --language_tabs 'ruby:Ruby' 'python:Python' 'javascript:JavaScript' 'go:Go' 'shell: cURL'  --summary weightless.yaml -o index.html.md\n
```
- Copy generated file: index.html.md to directory source/ 

#### Test locally
- Start docker engine
```
docker run --rm --name slate -p 4567:4567 -v $(pwd)/source:/srv/slate/source slatedocs/slate serve
```

- View docs in browser: http://localhost:4567/#weightless

#### Deploy

- Git commit
- Git push main
- ./deploy.sh --push-only
- View docs in browser: https://bosemangroup.github.io/weightless-slate-rest-docs

