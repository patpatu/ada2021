# ada2021

To run jekyll :

```sh
docker run --rm --volume="$PWD:/srv/jekyll" --publish 127.0.0.1:4000:4000 jekyll/jekyll jekyll serve
```