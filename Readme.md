# Jupyter Notebook
This notebook is based on the official [jupyter/base-notebook](https://hub.docker.com/r/jupyter/base-notebook/)
and comes with the following extensions installed: 

* [RISE-Plugin by damianavila82](https://github.com/damianavila/RISE)
* [OpenJDK 11](https://openjdk.java.net)
* [IJava Kernel for Jupyter](https://github.com/SpencerPark/IJava)
* [Tex-Live](https://www.tug.org/texlive/) LaTeX/XeTeX-Support for exporting PDF files

## Usage 

Since this docker container extends the [jupyter/base-notebook](https://hub.docker.com/r/jupyter/base-notebook/), all 
environment parameters, options etc. are available here, too. To start the container with an externally mounted notebook directory, 
accessible on port 8888, use the following command line: 

```bash 
docker run -it --rm --user root -v /myNotebooks:/home/jovyan/work -p 8888:8888 jreichwald/jupyternb start-notebook.sh
``` 

To start the notebook without the need to use a token (_including all security aspects!_), use: 

```bash 
docker run -it --rm --user root -v /myNotebooks:/home/jovyan/work -p 8888:8888 jreichwald/jupyternb start-notebook.sh --NotebookApp.token=''
``` 
