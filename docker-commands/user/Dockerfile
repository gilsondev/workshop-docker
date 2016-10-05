FROM ubuntu:latest

# Criando uma pasta para o usuario root e basis
# poder escrever normalmente
RUN mkdir -p /var/whoami
RUN chmod -R 777 /var/whoami

RUN whoami >> /var/whoami/root.txt

# Criando usuario para executar o whoami corretamente
# devido a esse erro reportado:
#
# https://github.com/docker/docker/issues/22323
RUN useradd basis -p 1234

USER basis

RUN whoami >> /var/whoami/basis.txt

CMD ["/bin/bash"]
