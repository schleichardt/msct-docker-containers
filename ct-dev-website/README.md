## Provide the web page

```bash
docker run --volume=$(pwd):/srv/jekyll -t -p 4004:4004 msct/ct-dev-website rake serve
```

## Enter a shell

```bash
docker run --volume=$(pwd):/srv/jekyll -t -p 4004:4004 msct/ct-dev-website rake serve
#looks like stuck because promt is missing
```

## Open the website on mac

```bash
open "http://$(docker-machine ip default):4004"
```