# docker-texlive-xetex

Docker image based on Ubuntu with texlive-xetex.

## What's inside

This Docker image contains `make`, `texlive-xetex` and `git`.

You can install additional packages with `apt install`.

## Pull the image

First pull the image either from Docker Hub or the GitHub Docker repository.

- To pull the image from Docker Hub run: 
    ```
    docker pull nevermendel/docker-texlive-xetex
    ```

- To pull the image from the GitHub Docker run: 
    ```
    docker pull ghcr.io/nevermendel/docker-texlive-xetex
    ```

## Run the image

You can choose whether you prefer to use the image interactively or not.

### Interactively

Start an instance of the image interactively

```
docker run --entry-point=/bin/bash -v $(pwd):/usr/app --rm nevermendel/docker-texlive-xetex
```

Then run XeLaTex to compile your files by executing `xelatex file.tex`

### Not interactively

Run the following command:

```
docker run -it -v $(pwd):/usr/app --rm nevermendel/docker-texlive-xetex "xelatex file.tex"
```

## License

[MIT License](LICENSE)