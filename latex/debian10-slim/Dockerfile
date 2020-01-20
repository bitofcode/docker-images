FROM debian:10-slim

ENV LATEX_USER "latex-user"

RUN apt-get update && \
    apt-get upgrade -yq && \
    apt-get install -yq \
    texlive-full \
    git-all git \
    python3-pip python3-pygments \
    python-pip python-pygments \
    gnuplot make && \
    useradd --create-home --shell /bin/bash ${LATEX_USER}

USER ${LATEX_USER}

WORKDIR /home/${LATEX_USER}

CMD ["/bin/bash"]
