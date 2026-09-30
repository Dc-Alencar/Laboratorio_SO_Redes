## 1. Identificação
- Nome completo: Daniel Costa Alencar
- Curso: Sistemas de Informação
- Turma 2023.1
- Data: 30/09/2026
- Título da prática: Aula 06 - Configuração de Rede Estática com Netplan e Modo Placa em Ponte (Bridge Adapter) no VirtualBox

## 2. Objetivo
A mudança do modo NAT para Placa em Ponte torna a máquina virtual um elemento independente na rede física, permitindo que ela receba um IP próprio e seja acessada diretamente por outros dispositivos. Para manter essa conectividade estável e sem interrupções em serviços é necessário definir um endereço fixo através do netplan, evitando que o IP seja alterado dinamicamente por reinicializações ou expirações do DHCP.


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
O adaptador de rede do VirtualBox foi configurado novamente, saindo do modo NAT para o modo Bridge, depois um endereço de IP livre na rede do laboratório foi encontrado, usando o CMD do Windows.  
Depois desse processo de configurar a rede, o arquivo de configuração do Netplan no Ubunto Server foi editado, para definir o IP estático, os servidores DNSs e o gateway.

---

## 5. Testes e Validação

### ping 172.20.21.1

<img width="795" height="282" alt="image" src="https://github.com/user-attachments/assets/c91e96b3-4680-496d-91c9-dcd51ff1f0f9" />




### Configurando o VirtualBox

<img width="1102" height="632" alt="image" src="https://github.com/user-attachments/assets/051364d8-fc40-4c90-a58e-8dc21bf6cdbd" />




### Configurando o arquivo do Netplan

<img width="795" height="832" alt="image" src="https://github.com/user-attachments/assets/63cb9e03-ac19-4ecb-8b62-115d712613c3" />




### CAT mostrando o arquivo pós edição

<img width="788" height="513" alt="image" src="https://github.com/user-attachments/assets/212142c6-3d36-4cdd-b0cc-d5029d31d157" />




### ip addr show enp0s3

<img width="1002" height="247" alt="image" src="https://github.com/user-attachments/assets/a1038d6a-410e-43e6-a2c9-7e6820dfe383" />




### Ping do Windows para a máquina virtual

<img width="740" height="658" alt="image" src="https://github.com/user-attachments/assets/3189091a-ee9a-4126-9cf2-b8aa49883f68" />




### Ping da máquina virtual para o Windows

<img width="997" height="582" alt="image" src="https://github.com/user-attachments/assets/2ac20126-eecb-42fe-ae77-dbccaa3cba99" />




### traceroute

<img width="862" height="337" alt="image" src="https://github.com/user-attachments/assets/b8920e9e-a4a1-413c-9d89-1d852ced7d26" />



## 6. Problemas e Soluções

Nenhum problema foi encontrado enquanto eu seguia o passo a passo dessa aula.

---

## 7. Conclusão

O uso de IP estático e modo Bridge mostrou-se fundamental para a estabilidade e previsibilidade de servidores na rede física. Além disso, a prática reforçou a aplicação do Netplan e de comandos de diagnóstico no gerenciamento de ambientes Linux.
