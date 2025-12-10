ARG VERSION
FROM vbti/onedl-mmdetection-cu129-torch280:$VERSION

RUN pip install --no-cache-dir \
    jupyterhub \
    jupyterlab \
    notebook \
    roboflow

CMD ["jupyterhub-singleuser", "--allow-root"]