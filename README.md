Framework docs: https://github.com/slatedocs/slate

#### Setup
- Install and run docker engine
```
npm install -g widdershins
```

#### Update docs
- Archive previous index.html.md in directory source/ by renaming file with date prefix 
- Modify open api file: weightless.yaml
- Convert open api file: weightless.yaml to slate doc format:
```
widdershins --language_tabs 'ruby:Ruby' 'python:Python' 'javascript:JavaScript' 'go:Go' 'shell: cURL'  --summary weightless.yaml -o index.html.md\n
```
- Copy generated file: index.html.md to directory source/ 

#### Update styling
- View framework wiki for detailed instructions: https://github.com/slatedocs/slate/wiki

#### Test locally
- Start docker engine
```
docker run --rm --name slate -p 4567:4567 -v $(pwd)/source:/srv/slate/source slatedocs/slate serve
```
- View docs in browser: http://localhost:4567/#weightless

#### Deploy
- Git commit and push to main branch
- ./deploy.sh --push-only
- View docs in browser: https://bosemangroup.github.io/weightless-slate-rest-docs
