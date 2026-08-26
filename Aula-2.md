# Aula 02: Administração de Usuários, Grupos e Permissões no Linux
## 1. Indentificação  
Nome completo: Daniel Costa Alencar  
Matrícula: 2023000622  
Turma: 7° Período  
Data de entrega: 26/08/2026  
## 2. Objetivo
 Essa atividade teve como foco ensinar como criar e administrar grupos de usuários, mostrando e explicando vários comandos relacionados a permissões de acesso e edição no Ubunto Server.
## 3. Ambiente
* Sistema operacional hospedeiro: Windows 11
* Hipervisor: Oracle VM VirtualBox versão 7.1.18r173720
* Distribuição do Ubunto Server: Ubuntu Server (imagem ISO ubuntu-22.04.5-live-server-amd64.iso)
## 4. Procedimentos
  * Criação de usuários: Foram criados os usuários **fulano**, **cicrano**, **beltrano** e **novato**, através do comando **sudo adduser**, e foi alocada a senha "senha123" para cada um deles, esse comando também cria uma pasta para cada usuário.
  * Criação e gestão dos grupos: Foi criado o grupo de trabalho **devs** através do comando **sudo groupadd**. Depois do grupo ser criado, foi usado o comando **sudo usermod -aG devs** para associar os usuários fulano, cicrano e beltrano a este grupo. O usuário novato ficou fora do grupo, ele serve como exemplo de usuário externo.
  * Criação da pasta projeto: Foi criada a pasta "projeto" no diretório raiz , através do comando **sudo mkdir -p /srv/projeto**.
  * Definição de permissões: O dono da pasta "projeto" se tornou o administrador, através do comando **sudo chown** e o grupo proprietário dessa pasta se tornou "devs" utilizando o comando **sudo chgrp**.
  * Configuração de restrições: A política de segurança foi configurada através do comando **sudo chmod 770 /srv/projeto**. Concedendo acesso total ao administrador e aos integrantes do grupo devs, e bloqueando qualquer acesso de de outros usuários.
  * Criação do grupo e pasta financeiro: Como atividade de fixação foi criado um grupo de trabalho **financeiro**, com os usuários **cicrano** e **beltrano**. Também foi criada a pasta "projeto", e o dono dela é o administrador, e o grupo proprietário sendo o "financeiro". Também foi feita a mudança de polítca de segurança nessa pasta, proibindo o acesso de usuários externos.
## 5. Testes e validação
* Teste para o susuário "fulano" manipular a pasta "projeto"
<img width="995" height="252" alt="image" src="https://github.com/user-attachments/assets/873dabeb-d91e-4280-b4b5-a20d457474c4" />
* Teste para mostrar que o usuário "novato" é bloquear na pasta "projeto"
<img width="1006" height="192" alt="image" src="https://github.com/user-attachments/assets/cfa00212-6263-4be4-a4d5-0fa903e08821" />
* Usuário "cicrano" acessando "financeiro"
  <img width="1005" height="182" alt="image" src="https://github.com/user-attachments/assets/70847215-b5fc-496f-bc38-44ab4a1f8819" />
* Usuário "fulano" sendo bloqueado de entrar na pasta "financeiro"
  <img width="997" height="207" alt="image" src="https://github.com/user-attachments/assets/52c05c5d-bdae-464a-8be6-0ceeac13c8a9" />
* Usuário "novato" sendo bloqueado de entrar na pasta "financeiro"
<img width="1001" height="176" alt="image" src="https://github.com/user-attachments/assets/345353e4-96f3-46cf-b244-0a34d25a56cf" />


## 6. Problemas e soluções  
Nenhum problema se apresentou enquanto eu fazia essa segunda aula.
## 7. Conclusão  
 Essa aula mostrou os básicos da criação de usuários, pastas e grupos no Ubunto Server, e como administrar eles individualmente, melhorando a segurança e privacidade dentro do servidor. Essas divisões e configurações vão servir como alicerce para as próximas aulas, e devem ser feitas de maneira correta e documentada, para evitar problemas de segurança futuros.

