ARG VERSION

FROM ultralytics/ultralytics:$VERSION

ARG NB_USER=jovyan
ARG NB_UID=1000
ARG NB_GID=100

USER root
RUN pip install --no-cache-dir \
    jupyterhub \
    jupyterlab \
    notebook \
    roboflow

RUN useradd -m -s /bin/bash -u $NB_UID -g $NB_GID $NB_USER

RUN chown -R $NB_USER:$NB_GID /home/$NB_USER

USER $NB_UID

WORKDIR /home/$NB_USER

CMD ["jupyterhub-singleuser"]