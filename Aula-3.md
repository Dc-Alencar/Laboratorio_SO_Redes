# Aula 03: Estrutura de Diretórios, Pastas do Sistema (FHS) e Permissões Avançadas no Linux Server
## 1. Indentificação  
Nome completo: Daniel Costa Alencar  
Matrícula: 2023000622  
Turma: 7° Período  
Data de entrega: 26/08/2026

## 2. Objetivo
Essa aula teve como objetivo principal explorar a arvore de diretórios do Linux. Foram ensinadas maneiras de navegar os diretórios, a criação de pastas em locais específicos, e o uso de permissões para aplicar politicas de isolamento.

## 3. Ambiente
* Versão do Ubuntu Server: Ubuntu Server (ISO: ubuntu-22.04.5-live-server-amd64)
* Hardware virtual: 1 vCPU, 2048 MB de RAM e 32 GB de disco.
* Diretórios de trabalhos locais: Pastas de serviço dentro do caminho /srv.

## 4. Procedimentos
* Visualização de pastas: A terceira aula se inicia com a visualização do diretório **/etc*, que guarda certas configurações do sistema, e depois passamos para pasta **/var/log**, para visualizar certos logs do sistema.
* Criação de pastas de departamentos: Usando o comando **sudo mkdir -p** criamos pastas de departamentos, as pastas **/srv/ti-dept/projetos** e **/srv/vendas-dept/relatorios**
* Administrando grupos departamentais: Foram criados os grupos "ti-group" e "vendas-group" através do comando **groupadd**, e usando o comando **usermod -aG** o usuário "fulano" foi alocado ao grupo de TI e o usuário "cicrano" foi alocado ao grupo de vendas.
* Gerindo as permissões dos grupos: Usando o comando **chown**, definimos que o usuário administrador e os grupos de departamentos seriam os donos de suas respectivas pastas no diretório raiz(/srv), e usamos o comando **chmod 770** para garantir que apenas o usuário Administrador e os grupos corretos consigam acessar as pastas, melhorando a segurança e privacidade.
* Desafio prático: Usando o que foi ensinado nessa aula, foi criado uma pasta chamada "diretoria-dept", um grupo chamado "diretoria-group", o usuário "beltrano" foi alocado nele, e com o gerenciamento de politica de permissão, o beltrano é o único com acesso a pasta "/srv/diretoria-dept"

# 5. Testes e validação
* fulano acessando as pastas do grupo de TI
  <img width="862" height="221" alt="image" src="https://github.com/user-attachments/assets/e5522535-4bad-4ebc-ae4a-472eefb3b366" />
* cicrano sendo bloqueado de entrar nas pastas do grupo de TI
  <img width="858" height="212" alt="image" src="https://github.com/user-attachments/assets/7b2b21a4-6908-4ed4-8b6c-81d0d972c6d3" />


# 6. Problemas e soluções
Nenhum problema se apresentou enquanto eu seguia o roteiro da aula

# 7. Conclusão
Gerenciar com precisão a infraestrutura Linux exige dominar a estrutura do sistema (FHS) e o controle de permissões. A verdadeira segurança vai além dos firewalls e depende da proteção interna: ao revogar totalmente o acesso de terceiros aos diretórios de cada setor, previne-se a consulta e a alteração não autorizada de dados críticos.
