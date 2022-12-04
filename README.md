# Ansible Cisco UCS template 

Segue exemplo de modelo de como criar um PlayBook de configuração para Cisco UCS Manager

Contendo as seguints opções de configuração:

- Criação de template(Service Profile Template) base para criação de profiles novos conforme demanda.
- Criação de IP Pool para gerenciamento(KVM) de IP em todos os servidores do ambiente.
- Criação de MAC Pool para gerenciamento de MAC para todos os servidores do ambiente.
- Criação de UUID Pool para gerenciamento de UUID para todos os servidores do ambiente.
- Criação de politica de midia virtual para Boot via ISO, neste exemplo utilizamos a imagem de um CentOS 7.2
- Criação de politicia de Boot para os servidores com ordenamento de boot para todas os servidores do ambiente.
