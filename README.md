# Ansible Cisco UCS template 

Segue exemplo de modelo de como criar um PlayBook de configuração para Cisco UCS Manager

Contendo as seguints opções de configuração:

- Criação de template(Service Profile Template) base para criação de profiles novos conforme demanda.
- Criação de IP Pool para gerenciamento(KVM) de IP em todos os servidores do ambiente.
- Criação de MAC Pool para gerenciamento de MAC para todos os servidores do ambiente.
- Criação de UUID Pool para gerenciamento de UUID para todos os servidores do ambiente.
- Criação de politica de midia virtual para Boot via ISO.
Obs: neste exemplo utilizamos a imagem de um CentOS 7.2
- Criação de politica de Boot para os servidores com ordenamento de boot para todas os servidores do ambiente.

--------------------------------------------------------------------

### 1º Primeiramente é necessário configurar o arquivo inventory com as informação de Hostname IP do UCSM juntamente com Usuário e Senha conforme exemplo:

[ucs]

192.168.25.163

[ucs:vars]

username=ucspe

password=ucspe

### 2º Criar uma estrutura de arquivos contendo as roles, com os arquivos contendo as politicas de configuração para os servidores e templates.

### 3º Rodar um ansible-playbook citando o arquivo de inventário relacionado a estrutura que irá receber as configurações setadas no arquivo server_deploy

ansible-playbook -i inventory server_deploy.yml

PLAY [ucs] **********************************************************************************************************************************************************************************************************************************

TASK [servers/defaults : Configure default IP Pool] *****************************************************************************************************************************************************************************************

....

### Após isso, as configuração estarão disponíveis no UCSM!
