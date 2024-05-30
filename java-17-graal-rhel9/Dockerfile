FROM redhat/ubi9
RUN yum install -y gcc zip unzip wget curl git zlib-devel --skip-broken
RUN curl -s "https://get.sdkman.io" | bash
RUN source "$HOME/.sdkman/bin/sdkman-init.sh" && sdk install java 17.0.8-graalce
ENV JAVA_HOME="$SDKMAN_CANDIDATES_DIR/java/current"
