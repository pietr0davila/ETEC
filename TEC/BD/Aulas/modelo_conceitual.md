# Modelo de dados conceitual

Representação dos dados que um sistema vai armazenar sem usar nenhuma tecnologia, linguagem SQL ou local físico. Define **Entidades, atributos e relacionamentos**. Uma entidade pode ser física (funcionário) ou abstrata (Conta bancária)

## Entidade

Representação de objetos do mundo real que vão ser armazenados no banco de dados futuramente

E.g:

Cliente = Usuário que compra
Produto = Item à venda
Pedido = compra feita pelo cliente

### Tipos de entidades

Entidade independente - Existem por si só e tem uma primary key
e.g: Cliente = Existe sem outra entidade

Entidade dependente - Não existem se não associadas a outra entidade
Precisam de chave estrangeira para identificar a relação com outra entidade
E.g: item_pedido = só existe se houver pedido

## Atributos

Atributos são caracteristicas que descrevem entidades. Cada entidade pode ter vários atributos e um deles vai ser a **Primary key** - Chave primária

#### Tipos de atributo

Atributo simples - Um valor por entidade
E.g: Nome

Atributo composto - São divididos em sub-partes
e.g: Endereço (que tem rua, Cidade, CEP...)

Atributo Multi-valorado - Multiplos valores para a mesma entidade
E.g: Aluno (Pode ter mais de um telefone)

Atributo derivado - Calculado a partir de outros atributos
E.g: Idade é derivada de data de nascimento

Primary Key - Identifica cada entidade
E.g: CPF identifica cliente

Atributos para um cliente:

[Cliente]
├── Nome
├── CPF (Chave Primária)
├── Data de Nascimento
├── Endereço (Composto: Rua, Número, Cidade, Estado)
├── Telefone (Multivalorado)
├── Idade (Derivado de Data de Nascimento)

## Relacionamentos

Mostram como cada entidade se conecta a outra
E.g:
Um **cliente** faz um **Pedido**
um **pedido** contém **produtos**

### Tipos de relacionamento:

1:1 - **um** usuáro com **um** CPF
1:N - Um cliente pode fazer **vários** pedidos mas **um** pedido pertence a um cliente
N:N - Um Aluno pode estar em **várias** turmas e uma turma pode ter **vários** alunos
