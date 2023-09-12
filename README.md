# AWS CloudFormation Sample Template - Infraestrutura de Rede e Servidores

Este repositório contém um modelo AWS CloudFormation para provisionar uma infraestrutura de rede básica na AWS, juntamente com instâncias de servidores Web e de banco de dados. O modelo cria uma Virtual Private Cloud (VPC) com sub-redes públicas e privadas, um NAT Gateway, instâncias EC2 para servidores Web e de banco de dados, bem como grupos de segurança correspondentes.

## Como Usar

Para usar este modelo, siga as instruções abaixo:

### Pré-requisitos

Antes de usar este modelo, certifique-se de que você tenha:

- Uma conta AWS configurada.
- Permissões adequadas para criar recursos especificados no modelo.

### Passos para Implantação

1. Faça o download do arquivo `sample-template-infra.yml` deste repositório.

2. Use o AWS CloudFormation para criar uma pilha de rede a partir do modelo.

### Recursos Criados

#### Recursos de Rede:
Uma Virtual Private Cloud (VPC) com um bloco CIDR de 10.100.0.0/16.
Duas sub-redes: uma pública (10.100.1.0/24) e uma privada (10.100.10.0/24).
Um Internet Gateway para permitir a comunicação com a Internet.
Um NAT Gateway para permitir que as instâncias nas sub-redes privadas acessem a Internet.
Tabelas de roteamento para direcionar o tráfego de forma apropriada.

#### Recursos de Servidores:
Um grupo de segurança para servidores Web (WebServers-SG) que permite o tráfego nas portas 22, 80 e 443.
Um grupo de segurança para servidores de banco de dados (Databases-SG) que permite o tráfego nas portas 22 e 3306.
Instâncias EC2 para servidores Web e de banco de dados, com volumes EBS associados.
