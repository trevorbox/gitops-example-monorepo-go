FROM registry.access.redhat.com/ubi9/ubi:latest
ARG tkn_dl_link=https://mirror.openshift.com/pub/openshift-v4/clients/pipeline/latest/tkn-linux-amd64.tar.gz
ARG oc_dl_link=https://mirror.openshift.com/pub/openshift-v4/clients/ocp/stable-4.11/openshift-client-linux.tar.gz
COPY build.sh /usr/bin/build.sh
RUN dnf -y install jq tar
RUN dnf clean all -y
RUN curl -s $tkn_dl_link | tar xvz -C /usr/bin --no-same-owner tkn
RUN curl -s $oc_dl_link | tar xvz -C /usr/bin --no-same-owner oc
RUN chmod 755 /usr/bin/build.sh
ENTRYPOINT [ "/usr/bin/build.sh" ]
