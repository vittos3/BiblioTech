
# **Sistema de Gerenciamento de Biblioteca Online**

Este é um projeto de um sistema de gerenciamento de biblioteca virtual, desenvolvido em Python, com o objetivo de consolidar conhecimentos em programação e explorar conceitos práticos em um contexto realista.

---

## **Descrição do Projeto**

O sistema permite gerenciar livros, usuários e empréstimos de forma eficiente. A aplicação utiliza conceitos de orientação a objetos, manipulação de arquivos, APIs externas e oferece uma interface baseada em FastAPI para facilitar as operações.

---

## **Funcionalidades**

### **1. Gerenciamento de Livros**
- Adicionar, editar, remover e listar livros.
- Atributos dos livros: título, autor, gênero, número de páginas e disponibilidade.

### **2. Gerenciamento de Usuários**
- Cadastro, remoção e listagem de usuários.
- Atributos dos usuários: nome, email e lista de livros emprestados.

### **3. Empréstimos**
- Registro de empréstimos e devoluções.
- Limite de até 3 livros por usuário.
- Cálculo automático da data de devolução (7 dias).

### **4. Persistência de Dados**
- Dados de livros e usuários são armazenados em arquivos `.json` para garantir persistência entre execuções.

### **5. API Pública**
- Integração com a [Open Library API](https://openlibrary.org/dev/docs/api/books) para busca e cadastro de livros via ISBN.

### **6. Interface FastAPI**
- Endpoints para:
  - Cadastro e consulta de livros e usuários.
  - Registro de empréstimos e devoluções.

### **7. Tratamento de Erros**
- Implementação de `try-except` para lidar com situações como:
  - Dados inválidos.
  - Arquivos ausentes ou corrompidos.
  - Falhas na conexão com a API.

---

## **Estrutura do Código**

### **1. Classes**
- **Classe `Book`**: Representa os livros com atributos como título, autor, gênero e disponibilidade.  
- **Classe `User`**: Representa os usuários com atributos como nome, email e lista de livros emprestados.  
- **Classe `Library`**: Gerencia as listas de livros e usuários, além da lógica de empréstimos e persistência.  

### **2. Persistência de Dados**
- Os dados são armazenados em arquivos `.json` e carregados automaticamente ao iniciar o sistema.  

### **3. Endpoints FastAPI**
- **GET `/books`**: Lista todos os livros.  
- **POST `/books`**: Cadastra um novo livro.  
- **POST `/users`**: Cadastra um novo usuário.  
- **POST `/borrow`**: Registra um empréstimo.  
- **POST `/return`**: Registra a devolução de um livro.  

### **4. API Externa**
- Integração com a Open Library API para buscar informações detalhadas de livros e facilitar o cadastro.

---

## **Como Executar o Projeto**

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```
2. Instale as dependências:
   ```bash
   pip install fastapi uvicorn requests
   ```
3. Execute o servidor FastAPI:
   ```bash
   uvicorn main:app --reload
   ```
4. Acesse a interface interativa da API no navegador:
   ```
   http://127.0.0.1:8000/docs
   ```

---

## **Tecnologias Utilizadas**
- **Python**: Linguagem principal do projeto.  
- **FastAPI**: Para criação dos endpoints RESTful.  
- **JSON**: Para persistência de dados.  
- **Open Library API**: Para busca de informações de livros.  

---

## **Contribuição**

Sinta-se à vontade para contribuir com o projeto! Basta seguir os passos:  
1. Faça um fork do repositório.  
2. Crie uma nova branch:  
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
3. Faça suas alterações e envie um pull request.  

---

## **Licença**

Este projeto é distribuído sob a licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.
