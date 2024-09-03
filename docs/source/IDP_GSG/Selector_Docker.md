
## Docker
1.	If you don’t have Docker installed on your machine, follow [these instructions](https://docs.docker.com/engine/install/) to install it.
2.	Pull the image from [DockerHub](https://hub.docker.com/r/intel/python) using the following command:
```bash
docker pull intel/python:latest 
```
3.	Run a performance sample by running the following commands:
```bash
git clone https://github.com/intel/ai-containers
cd ai-containers/python
docker run --rm -it \
    -v $PWD/tests:/tests \
    intel/python:latest \
    python /tests/perf_sample.py
```
4. Verify installation.
```bash
conda list
```

[Selector - Get Started Guide](https://github.com/raistefintel/intelpython.github.io/blob/master/docs/source/IDP_GSG.md)
[Intel® Distribution for Python* Installation Selector](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html)