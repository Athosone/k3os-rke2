ARG REPO
ARG TAG
FROM ${REPO}/k3os-base:${TAG}

ARG ARCH
ENV ARCH ${ARCH}
ENV VERSION v1.19.7+rke2r1
ADD https://raw.githubusercontent.com/rancher/rke2/${VERSION}/install.sh /output/install.sh

ENV INSTALL_RKE2_VERSION=${VERSION} \
  INSTALL_RKE2_TYPE="server"

RUN chmod +x /output/install.sh
RUN /output/install.sh
ENV VERSION="v1.20.0"

RUN echo "${VERSION}" > /output/version