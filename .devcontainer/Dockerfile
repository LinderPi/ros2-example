FROM ros:rolling

ARG USERNAME
ARG USER_UID=1001
ARG USER_GID=$USER_UID

RUN apt update && apt upgrade -y
RUN echo "source /opt/ros/rolling/setup.bash" >> /etc/bash.bashrc

RUN groupadd -g ${USER_GID} ${USERNAME} && useradd -u ${USER_UID} -g ${USER_GID} -m -s /bin/bash ${USERNAME}

USER ${USERNAME}
