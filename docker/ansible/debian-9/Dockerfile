#+++++++++++++++++++++++++++++++++++++++
# Dockerfile for webdevops/ansible:debian-9
#    -- automatically generated  --
#+++++++++++++++++++++++++++++++++++++++

FROM webdevops/bootstrap:debian-9

# Install ansible
RUN /usr/local/bin/apt-install \
        # Install ansible
        python-minimal \
        python-setuptools \
        python-pip \
        python-paramiko \
        python-jinja2 \
        python-dev \
        libffi-dev \
        libssl-dev \
        build-essential \
    && pip install --upgrade pip \
    && hash -r \
    && pip install --no-cache-dir ansible \
    && chmod 750 /usr/local/bin/ansible* \
    # Cleanup
    && apt-get purge -y -f --force-yes \
        python-dev \
        build-essential \
        libssl-dev \
        libffi-dev \
    && docker-image-cleanup
