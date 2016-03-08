FROM ocaml/opam:debian-stable_ocaml-4.02.3
RUN sudo -u opam sh -c "opam pin add -n git-lfs-server https://github.com/artemkin/git-lfs-server.git" && \
  sudo -u opam sh -c "opam update -u" && \
  sudo -u opam sh -c "opam depext -u git-lfs-server" && \
  sudo -u opam sh -c "opam install -y -j 2 -v git-lfs-server"