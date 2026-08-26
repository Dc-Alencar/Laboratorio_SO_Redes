# Aula Prática 01: Introdução à Virtualização e Instalação do Ubuntu Server 26.04
## 1. Indentificação  
Nome completo: Daniel Costa Alencar  
Matrícula: 2023000622  
Turma: 7° Período  
Data de entrega: 26/08/2026  
## 2. Objetivo
- Compreender os conceitos básicos de virtualização (Hipervisor, Máquina Virtual, Isolamento de Recursos).
- Preparar o ambiente de trabalho local utilizando o Oracle VM VirtualBox.
- Realizar a instalação limpa e personalizada do sistema operacional de rede Ubuntu Server 26.04 LTS utilizando particionamento LVM.
- Validar a instalação por meio do primeiro login e atualização dos repositórios de pacotes.
## 3. Ambiente
* Hardware usado: IdeaPad Slim 3 15IRH10
* Imagem usada: ubuntu-22.04.5-live-server-amd64.iso
* <img width="1018" height="627" alt="image" src="https://github.com/user-attachments/assets/7008da6c-645d-478d-b783-0f20793022dc" />
## 4. Procedimentos
A máquina foi criada seguindo os passos passados na atividade, o idioma escolhido foi o Inglês, mas o teclado está com o padrão ABNT2, para não ocorrer nenhum erro de digitação.
## 5. Teste e validação
* ip addr
  <img width="801" height="276" alt="image" src="https://github.com/user-attachments/assets/dd78e97b-dd29-4c10-a83c-a588d244d106" />
* sudo apt-get update
  <img width="797" height="132" alt="image" src="https://github.com/user-attachments/assets/7a6cbd8c-2ead-4c17-a953-cb646ffb11e6" />
  # 6. Problemas e soluções
  Ao tentar fazer a máquina virutal com apenas 512 mb de RAM, um problema de Kernel impedia a continuação da instalação, para resolver isso foi aumentada a quantidade de RAM para 2GB.
  # 7. Conclusão
  Com essa atividade inicial, foi possível criar uma máquina virtual Ubunto de forma rápida e compreensivel, e expandiu meus conhecimentos na área, já que só tinha costume de preparar máquinas ou usando Windows 11 ou Linux Mint. 
