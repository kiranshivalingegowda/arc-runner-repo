FROM quay.io/buildah/stable:latest
RUN echo "export BUILDAH_ISOLATION=chroot" >> /home/build/.bashrc && \
    # Use VFS since fuse does not work
    mkdir -p /home/build/.config/containers && \
    (echo '[storage]';echo 'driver = "vfs"') > /home/build/.config/containers/storage.conf 
USER build
WORKDIR /home/build
