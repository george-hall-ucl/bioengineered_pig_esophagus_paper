First, download (from [here](https://doi.org/10.5522/04/27303705)) and extract the pipeline contained in `bioeng_oeso_pipeline.tar.gz`. Load the docker image with `docker load -i bioeng_oeso_docker_5_d386af43e8f4.tar`.

Run the entire notebook from this directory with:

```bash
docker run --interactive \
           --tty \
           --rm \
           --volume /var/run/docker.sock:/var/run/docker.sock \
           --volume "$(pwd):/tmp/in_mnt" \
           --workdir /tmp/in_mnt \
           --env HOST_MOUNT_PATH="$(pwd)" \
           --oom-score-adj -1000 \
           bioeng_oeso_docker_5 \
           bash
```

## Licensing

The software component of this release is released under the MIT License:

Copyright 2026 University College London

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
