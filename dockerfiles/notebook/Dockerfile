FROM jupyterhub/k8s-singleuser-sample:0.7.0
# Do the pip installs as the unprivileged notebook user
USER $NB_USER
ADD jupyter_notebook_config.py /etc/jupyter/jupyter_notebook_config.py
# Install NB2KG
RUN pip install --upgrade nb2kg && \
    jupyter serverextension enable --py nb2kg --sys-prefix

