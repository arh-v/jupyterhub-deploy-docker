
ARG VERSION
FROM ultralytics/ultralytics:$VERSION
RUN pip install --no-cache-dir \
    jupyterhub \
    jupyterlab \
    notebook
CMD ["jupyterhub-singleuser", "--allow-root"]