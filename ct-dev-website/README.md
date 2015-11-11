## Provide the web page

```bash
docker run --volume=$(pwd):/srv/jekyll -it -p 4004:4004 msct/ct-dev-website rake serve
```

## Enter a shell

```bash
docker run --volume=$(pwd):/srv/jekyll -it -p 4004:4004 msct/ct-dev-website sh
#looks like stuck because prompt is missing
```

## Open the website on mac

```bash
open "http://$(docker-machine ip default):4004"
```

## Notes to publish the container

```bash
docker build -t msct/ct-dev-website .
docker push msct/ct-dev-website
```