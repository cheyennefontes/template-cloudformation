# AWS CloudFormation Sample Template - Rede Básica

Este repositório contém um modelo AWS CloudFormation para provisionar uma infraestrutura de rede básica na AWS. O modelo cria uma Virtual Private Cloud (VPC) com sub-redes públicas e privadas, bem como um NAT Gateway para permitir que as instâncias nas sub-redes privadas acessem a Internet.

## Como Usar

Para usar este modelo, siga as instruções abaixo:

### Pré-requisitos

Antes de usar este modelo, certifique-se de que você tenha:

- Uma conta AWS configurada.
- Permissões adequadas para criar recursos especificados no modelo.

### Passos para Implantação

1. Faça o download do arquivo `sample-template-network.yml` deste repositório.

2. Use o AWS CloudFormation para criar uma pilha a partir do modelo.

Recursos Criados
Este modelo cria os seguintes recursos na sua conta AWS:

Uma Virtual Private Cloud (VPC) com um bloco CIDR de 10.100.0.0/16.
Duas sub-redes: uma pública (10.100.1.0/24) e uma privada (10.100.10.0/24).
Um Internet Gateway para permitir a comunicação com a Internet.
Um NAT Gateway para permitir que as instâncias nas sub-redes privadas acessem a Internet.
Tabelas de roteamento para direcionar o tráfego de forma apropriada.
