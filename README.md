# Gerenciador de Senhas com Criptografia

Este projeto é um simples gerenciador de senhas que permite armazenar credenciais de forma segura em um arquivo Excel (.xlsx). As senhas são criptografadas utilizando a biblioteca `bcrypt` antes de serem armazenadas.

## Requisitos

Antes de executar o código, certifique-se de ter instalado as seguintes bibliotecas:

```sh
pip install bcrypt openpyxl
```

## Como Funciona

1. O script solicita ao usuário as seguintes informações:
   - Nome da conta (ex: Instagram, Facebook, etc.)
   - Nome de usuário
   - Senha

2. A senha fornecida é criptografada usando `bcrypt`.

3. Os dados são armazenados em um arquivo `users.xlsx` contendo as seguintes colunas:
   - **Conta**: Nome da plataforma ou serviço
   - **Usuário**: Nome do usuário
   - **Senha Criptografada**: Senha protegida com `bcrypt`

## Estrutura do Código

- `criar_ou_abrir_workbook(filename)`: Verifica se o arquivo Excel existe, cria um novo se necessário e adiciona um cabeçalho caso esteja vazio.
- `save_user_to_excel(filename, account, username, hashed_password)`: Adiciona os dados do usuário ao arquivo e salva as alterações.
- `main()`: Função principal que coleta as informações do usuário, criptografa a senha e salva os dados.

## Como Executar

Basta rodar o script Python:

```sh
python script.py
```

Substitua `script.py` pelo nome do arquivo caso tenha salvo com outro nome.

## Segurança

- As senhas são armazenadas de forma segura utilizando `bcrypt`, garantindo que não possam ser facilmente recuperadas.
- O arquivo Excel não é protegido por senha ou criptografia adicional, então é recomendável armazená-lo em um local seguro.

## Melhorias Futuras

- Implementação de um sistema de recuperação e verificação de senhas.
- Adição de uma interface gráfica para facilitar o uso.
- Proteção adicional para o arquivo Excel.

---

**Autor:** Seu Nome
