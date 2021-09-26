## Script para configuração do StrongSwan no Provedor AWS

### Descrição do Projeto
Instruções para instalação e configuração do StrongSwan na AWS.

### Pré-requisitos
- par de chaves na AWS
- Instância EC2 ubuntu 20.04

### 🚀 Execução
1. Acesse o diretório script e copie o algoritmo.

2. Na etapa de **Configure Instance** em **User data**, você deve colocar o script

Vai aparecer dessa forma
<p>
    <img alt="User Data" src="images/user-data.png">
</p>

Após inserir o código
<p>
    <img alt="User Data" src="images/user-data2.png">
</p>

Agora pode continuar a criação da instância.

4. Agora você deve desabilitar o serviço de source/destination na instância.
<p>
    <img alt="User Data" src="images/source-destination01.png">
</p>

Deve ficar dessa forma e salve a configuração

<p>
    <img alt="User Data" src="images/source-destination02.png">
</p>

5. Por fim, é necessário configurar as rotas apontando diretamente para instância

Abaixo temos um exemplo (Rede 192.168.0.0/24)

<p>
    <img alt="User Data" src="images/route.png">
</p>

<p>
    <img alt="User Data" src="images/route01.png">
</p>

<p>
    <img alt="User Data" src="images/route02.png">
</p>


### **:books: REFERÊNCIAS**

- [StrongSwan - Public Cloud VPC](https://wiki.strongswan.org/projects/strongswan/wiki/AwsVpc)
- [AWS - Source/Destination](https://docs.aws.amazon.com/pt_br/vpc/latest/userguide/VPC_NAT_Instance.html)


