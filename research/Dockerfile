# Template based on https://github.com/jupyter/docker-stacks/tree/master/base-notebook
FROM jupyter/base-notebook

USER jovyan

WORKDIR /mnt/code

COPY requirements.txt requirements.txt
RUN python -m pip install --upgrade pip
RUN python -m pip install -r requirements.txt

RUN cp /etc/jupyter/jupyter_notebook_config.py /home/jovyan/.jupyter/jupyter_notebook_config.py
RUN echo '\nc.NotebookApp.port = 8888' >> /home/jovyan/.jupyter/jupyter_notebook_config.py