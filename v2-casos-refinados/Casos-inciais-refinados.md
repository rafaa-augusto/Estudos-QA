# Casos de Teste - Login SauceDemo (v2) - Refinado

Nesta versão, apliquei boas práticas de documentação de testes, utilizando tabelas e detalhando os dados de entrada e resultados esperados conforme os padrões da área de QA.

| ID        | Título do Caso de Teste         | Pré-condição                            | Passo a Passo                                                                                                                                                                          | Resultado Esperado                                                                                                                  |
| :-------- | :------------------------------ | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| **CT001** | Validar login com sucesso       | Usuário cadastrado no sistema.          | 1. Acessar o site [Saucedemo](https://www.saucedemo.com/)<br>2. Digitar `standard_user` no campo Username<br>3. Digitar `secret_sauce` no campo Password<br>4. Clicar no botão "Login" | O login deve ser realizado com sucesso e o usuário redirecionado para a página de produtos (`/inventory.html`).                     |
| **CT002** | Login com senha incorreta       | Usuário cadastrado, mas senha inválida. | 1. Acessar o site<br>2. Digitar `standard_user`<br>3. Digitar uma senha incorreta (ex: `12345`) <br>4. Clicar em "Login"                                                               | O sistema deve impedir o acesso e exibir a mensagem: _"Epic sadface: Username and password do not match any user in this service"_. |
| **CT003** | Login com usuário incorreto     | Usuário não cadastrado.                 | 1. Acessar o site<br>2. Digitar um usuário inexistente (ex: `user_errado`) <br>3. Digitar `secret_sauce`<br>4. Clicar em "Login"                                                       | O sistema deve exibir mensagem de erro informando credenciais inválidas.                                                            |
| **CT004** | Usuário em letras maiúsculas    | Usuário cadastrado em minúsculas.       | 1. Acessar o site<br>2. Digitar o usuário em CAIXA ALTA (ex: `STANDARD_USER`) <br>3. Digitar senha correta<br>4. Clicar em "Login"                                                     | O sistema deve tratar como erro de login (Case Sensitive).                                                                          |
| **CT005** | Validar login com campos vazios | Acesso à tela de login.                 | 1. Acessar o site<br>2. Deixar os campos Username e Password em branco<br>3. Clicar em "Login"                                                                                         | O sistema deve exibir a mensagem: _"Epic sadface: Username is required"_.                                                           |

---

## 📹 Evidências de Execução

Abaixo estão os vídeos demonstrando a execução manual destes testes:

- **Execução CT001 e CT002:** [Link para o vídeo ou arquivo]
- **Execução CT003 ao CT005:** [Link para o vídeo ou arquivo]
