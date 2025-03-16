FROM ubuntu:22.04

USER root

RUN [ -d /mnt ] && echo "/mnt existiert" || echo "/mnt existiert nicht"
RUN chmod -R a+w /mnt || true

RUN rm -rf /mnt/* || true

CMD ["sleep", "5"]
