# Docker Image
This docker image is based on the `rocker/rstudio` image and adds several R packages. Also the [rethinking](https://github.com/rmcelreath/rethinking) package is installed which is not available on CRAN.

# Run Container
Make sure you are in the `docker-image` directory before running the following commands.
```bash
docker compose up
```
You can now run attach to the container witch vscode if you want.

# Create Image
```bash
docker commit r-stuff r-stuff:latest
```

# Push the image to our registry
Via vscode you can right click on the image and push it to the registry. You will need to create a personal access token to be able to push.
