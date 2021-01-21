FROM scratch
COPY build/k3os/system/ /k3os/system/
ENV PATH /k3os/system/k3os/current:/k3os/system/rke2/current:${PATH}
ENTRYPOINT ["k3os"]
CMD ["help"]
