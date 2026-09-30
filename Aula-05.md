## 1. Identificação
- Nome completo: Daniel Costa Alencar
- Curso: Sistemas de Informação
- Turma 2023.1
- Data: 28/09/2026
- Título da prática: Aula 05 - Acesso Remoto SSH via Redirecionamento de Portas no VirtualBox e Diagnóstico de Rede


## 2. Objetivo
Essa aula teve como objetivo aprender a verificar rotas de rede, usar o `netstat` para acompanhar as portas e conexões ativas, e criar conexões remotas através do SSH entre o Windows e o Ubunto Server, usando o NAT do VirtualBox.

## 3. Ambiente
- Hardware Físico : IdeaPad Slim 3 15IRH10  
- Virtualizador: Oracle VM VirtualBox versão 7.1.18r173720  
- Imagem ISO Utilizada: `ubuntu-22.04.5-live-server-amd64.iso`  
- Configurações da Máquina Virtual:  
- Nome da VM: `ubuntu_server`  
- Tipo / Versão: Linux / Ubuntu (64-bit)  
- Processador: 1 vCPU  
- Memória RAM: 2048 MB   
- Armazenamento: Disco rígido virtual de 32 GB   
- Controladora de Rede: Interface em modo NAT (`enp0s3`) com DHCP ativo  


## 4. Procedimento
   Instalei os programas `traceroute` e `net_tools`, e chequei se o `òpenssh-server` já estava instalado, depois que essas instalações inicias foram devidamente concluidas alguns comandos para verificar o estado da rede e das conexões foram executados, sendo eles `ipconfig`, `w`, `route -n` e `netstat -an`.  
 Depois de instalar os programas iniciasi e checar o estado das redes e conexões, o redirecionamento da porta do Virtualbox foi configurado para permitir uma conexão SSH com o Ubunto Server.

---

## 5. Testes e Validação

### netplan

<img width="1000" height="746" alt="image" src="https://github.com/user-attachments/assets/29c04f47-4c98-4e76-92e5-9c0aabbe1ff2" />



### Ifconfig

<img width="981" height="437" alt="image" src="https://github.com/user-attachments/assets/1ab14e96-2616-48ee-bc51-12647f5753c1" />



### route -n

<img width="997" height="205" alt="image" src="https://github.com/user-attachments/assets/b728fa5b-7b15-4be5-a9b3-54c3981a5a37" />



### traceroute

<img width="990" height="422" alt="image" src="https://github.com/user-attachments/assets/0dc96c22-0bd0-4ed7-afd1-320200782164" />



### w

<img width="1000" height="183" alt="image" src="https://github.com/user-attachments/assets/4b3e11be-fee0-416b-9e7d-5449da715925" />



### netsh -an

<img width="701" height="137" alt="image" src="https://github.com/user-attachments/assets/9cc3012b-ece9-47c6-bead-7ce1fff5e0ad" />



### netstat

<img width="785" height="182" alt="image" src="https://github.com/user-attachments/assets/13c41307-089d-4d49-a280-232bc30e8966" />



### Conexão via SSH

<img width="840" height="868" alt="image" src="https://github.com/user-attachments/assets/262149d6-131c-4a49-81f1-0093f0f12db5" />




### Netsh 

<img width="877" height="246" alt="image" src="https://github.com/user-attachments/assets/a9068ae5-8000-4d57-b573-c5e2bf20066e" />



### w após a conexão ser estabelecida

<img width="808" height="215" alt="image" src="https://github.com/user-attachments/assets/77c64e21-f574-418e-835c-04f9c3d2eef7" />



## 6. Problemas e Soluções

Durante a execução da atividade eu me confundi na sequência dos comandos, mas depois de um tempo refazendo o passo a passo o problema foi retificado.

---

## 7. Conclusão

Essa aula me ajudou a entender melhor o funcionamento da comunicação entre a máquina virtual que foi criada e o Windows, mostrandos comandos que verificam essa conexão, e outros detalhes de rede.  
A aula também mostrou a maneira correta de configurar e redirecionar as portas, para assim conseguir usar o Ubunto Server através do SSh.
