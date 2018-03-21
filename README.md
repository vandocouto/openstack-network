# Openstack - Criando uma Network

* Para criar uma network é necessário que já tenha um projeto definido dentro do Openstack.

### Exportando as variavéis de ambiente:

* Login do usuário
* Password do usuário
* Endereço da API do Openstack 
* Nome do Projeto

```bash
export OS_USERNAME=user
export OS_PASSWORD=pass
export OS_AUTH_URL=http://openstack.tutoriaisgnulinux.com:5000/v2.0
export OS_TENANT_NAME=project1
```

### Definindo as variavéis de ambiente:

* Nome do Projeto
* Subnet do Projeto

```bash
export TF_VAR_Project=project1
export TF_VAR_Subnet=10.0.0.0/24
```

### Para construir/destruir a Network basta utilizar o [Terraform](https://www.terraform.io/) (plan - apply - destroy).

*  Construindo a Network:

```bash
./build.sh terraform/ plan
./build.sh terraform/ apply
```

*  Destruindo a Network:

```bash
./build.sh terraform/ destroy
```
