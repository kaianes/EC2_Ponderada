# Ponderada de Programação

### Módulo 05 - semana 03.

## Introdução

A Amazon Web Services (AWS) é uma das principais provedoras de serviços em nuvem, oferecendo serviços como o Amazon Elastic Compute Cloud (EC2), que permite a criação e gerenciamento de instâncias de máquinas virtuais escaláveis. Este relatório descreve o processo de criação de uma instância EC2 na AWS e o acesso a essa máquina virtual por meio do PuTTY e SSH.

## Objetivo

O objetivo deste relatório é fornecer um guia passo a passo para a criação de uma instância EC2 na AWS e demonstrar como acessá-la remotamente utilizando o PuTTY e SSH. 

## Materiais

•	Conta na AWS Academy;
•	Acesso à internet;
•	Um computador local com o PuTTY instalado;
•	Chave de acesso SSH (pública/privada).

## Método

### 1. Criar intância EC2

#### 1.1 Ativar o Learner Lab

Dentro da [AWS Academy](https://awsacademy.instructure.com/),   iniciar o "Learner Lab".

<div align="center">
  <sub>Figura 1: Learner Lab</sub>
  <img src="./imagens/learner-lab.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.2 Dentro de "EC2", executar uma instância

<div align="center">
  <sub>Figura 2: Criar uma instância</sub>
  <img src="./imagens/executar-instancia.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.3 Definir o nome do servidor

(no exemplo foi usado "seervidor-ponderada-kaiane")

<div align="center">
  <sub>Figura 3: Definir nome da instância</sub>
  <img src="./imagens/nome.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.4 Escolher uma imagem de máquina virtual (AMI), tipo de instância, configurações de rede e outras opções conforme necessidade.

<div align="center">
  <sub>Figura 4: Definir imagem da instância</sub>
  <img src="./imagens/imagem.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.5 Definir tipos e chaves.

Qual o porte necessário para a sua instância criada? 

Defina um par de chaves de acesso (ou use o *defalt*)

(ao configurar uma nova chave, ela é baixada na sua máquina local) --- será usada depois!

<div align="center">
  <sub>Figura 5: Tipo de instância e Par de chaves</sub>
  <img src="./imagens/chaves.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.6 Finalizar

<div align="center">
  <sub>Figura 8: Executar</sub>
  <img src="./imagens/executar.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.7 Conferir êxito ao criar uma instância :)

<div align="center">
  <sub>Figura 9: Êxito ao criar uma instância EC2</sub>
  <img src="./imagens/exito.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 1.8 Verificar informações sobre a sua instância.

Informações importantes sobre a sua máquina como a chave pública estão aqui.

<div align="center">
  <sub>Figura 10: Verificar informações</sub>
  <img src="./imagens/informacoes.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

### 2. Conectar á instância por meio do PuTTY 

#### 2.1 Inserir nome de usuário e DNS IPv4 público

<div align="center">
  <sub>Figura 11: Conectar á instância por meio do PuTTY</sub>
  <img src="./imagens/session.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 2.2 Escolher o arquivo .ppk de chave privada

<div align="center">
  <sub>Figura 12: Credenciamento com a chave</sub>
  <img src="./imagens/credentials.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 2.3 Confiar na conexão

<div align="center">
  <sub>Figura 13: "Accept"</sub>
  <img src="./imagens/accept.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>

#### 2.4 FIM!  


<div align="center">
  <sub>Figura 14: Conectado com sucesso</sub>
  <img src="./imagens/authentication.png" width="100%">
  <sup>Fonte: O autor (2024)</sup>
</div>


## Resultados

Após seguir o método descrito acima, foi possível criar com sucesso uma instância EC2 na AWS e acessá-la remotamente utilizando o PuTTY e SSH. A conexão foi estabelecida com êxito, permitindo a interação com a máquina virtual de forma remota.

## Conclusão

A criação de uma instância EC2 na AWS e o acesso a ela por meio do PuTTY e SSH são processos fundamentais para aproveitar os benefícios da computação em nuvem de forma eficiente e segura. Essa abordagem oferece flexibilidade, escalabilidade e facilidade de gerenciamento de recursos computacionais, contribuindo para a otimização de operações e desenvolvimento de projetos em diversos contextos.
