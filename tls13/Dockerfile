FROM ocaml/opam
RUN sudo -u opam sh -c "opam remote add tls13 https://github.com/mirleft/tls13-opam.git" && \
  sudo -u opam sh -c "opam depext -u tlstools" && \
  sudo -u opam sh -c "opam install -y -j 2 -v tlstools"
WORKDIR /home/opam
RUN sudo -u opam sh -c "opam source --dir tlstools tlstools"
COPY cs.txt /home/opam/tlstools
WORKDIR /home/opam/tlstools
EXPOSE 8000
CMD ["tlsweb","cs.txt"]
