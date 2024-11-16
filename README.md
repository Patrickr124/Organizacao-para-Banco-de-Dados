# Organização do Banco de Dados para Novo Airbnb

## Tabelas e Colunas

### Usuários
- `id_usuario` (PK)
- `nome`
- `email`
- `senha`
- `data_criacao`
- `telefone`
- `endereco`

### Lugares
- `id_lugar` (PK)
- `id_usuario` (FK)
- `nome`
- `descricao`
- `endereco`
- `preco_por_noite`
- `data_criacao`

### Hospedagens
- `id_hospedagem` (PK)
- `id_usuario` (FK)
- `id_lugar` (FK)
- `data_inicio`
- `data_fim`
- `preco_total`
- `status`

### Avaliações
- `id_avaliacao` (PK)
- `id_hospedagem` (FK)
- `id_usuario` (FK)
- `nota`
- `comentario`
- `data_avaliacao`

## Relacionamentos

- **Usuários** e **Lugares**: 1:N (um usuário pode cadastrar vários lugares)
- **Usuários** e **Hospedagens**: 1:N (um usuário pode realizar várias hospedagens)
- **Lugares** e **Hospedagens**: 1:N (um lugar pode ser hospedado várias vezes)
- **Hospedagens** e **Avaliações**: 1:N (uma hospedagem pode ter várias avaliações)
- **Usuários** e **Avaliações**: 1:N (um usuário pode fazer várias avaliações)

## Explicação

- **Usuários**: Armazena informações básicas e de contato dos usuários.
- **Lugares**: Detalhes dos lugares disponíveis para hospedagem.
- **Hospedagens**: Registra as reservas feitas pelos usuários.
- **Avaliações**: Permite que os usuários avaliem suas hospedagens.

Essa estrutura garante que todas as informações necessárias sejam armazenadas de forma organizada e que os relacionamentos entre as tabelas sejam claros e eficientes.

