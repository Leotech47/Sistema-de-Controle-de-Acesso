Esse código Python cria um **sistema de login simples** usando um dicionário para armazenar nomes de usuários e suas senhas correspondentes. Ele simula um cenário onde uma empresa precisa verificar as credenciais dos funcionários para conceder acesso.

---
## Explicação do Código

O código funciona da seguinte maneira:

1.  **Dicionário de Usuários (`usuarios`):** No início do programa, um dicionário chamado `usuarios` é definido. Cada **chave** neste dicionário é um **nome de usuário** (por exemplo, "joao", "ana") e o **valor** associado a essa chave é a **senha** correspondente (por exemplo, "1234", "abcd"). Este dicionário atua como nosso banco de dados de credenciais.

2.  **Entrada do Usuário:**
    * `usuario = input().strip()`: Esta linha lê a primeira entrada fornecida pelo usuário, que é o nome de usuário. O método `.strip()` é usado para remover quaisquer espaços em branco extras no início ou no final da string.
    * `senha = input().strip()`: Similarmente, esta linha lê a segunda entrada, que é a senha, e também remove espaços em branco.

3.  **Verificação de Credenciais (`if` e `else`):**
    * `if usuario in usuarios and usuarios[usuario] == senha:`: Esta é a parte central da lógica de verificação.
        * `usuario in usuarios`: Primeiro, ela verifica se o nome de usuário digitado existe como uma chave no dicionário `usuarios`. Se o usuário não for encontrado no dicionário, a condição já é falsa, e o bloco `else` será executado.
        * `usuarios[usuario] == senha`: Se o usuário for encontrado, esta parte da condição verifica se a senha fornecida pelo usuário (`senha`) corresponde ao valor (a senha correta) associado àquele usuário no dicionário (`usuarios[usuario]`).
    * Se ambas as condições forem verdadeiras (o usuário existe e a senha está correta), a mensagem "Acesso permitido" é impressa.
    * `else:`: Se qualquer uma das condições no `if` for falsa (usuário não existe ou a senha está incorreta), o programa executa o bloco `else` e imprime "Usuário ou senha incorretos".

---
## Exemplos de Aplicação

Aqui estão três exemplos de como esse tipo de sistema de login pode ser aplicado em cenários reais:

1.  **Login em um Sistema Interno da Empresa:**
    * **Cenário:** Uma empresa tem um portal interno para que os funcionários acessem holerites, solicitem férias ou consultem políticas internas.
    * **Aplicação:** O sistema de login verifica as credenciais do funcionário antes de conceder acesso a essas informações confidenciais. A `usuarios` pode ser um banco de dados de funcionários.

2.  **Acesso a um Painel de Controle de Website:**
    * **Cenário:** Um administrador de website precisa fazer login em um painel para gerenciar conteúdo, usuários ou configurações do site.
    * **Aplicação:** O sistema de login garante que apenas usuários autorizados (administradores) possam acessar o painel de controle, protegendo a integridade do site.

3.  **Verificação de Credenciais para um Aplicativo Desktop Simples:**
    * **Cenário:** Um pequeno aplicativo desktop é usado para gerenciar o estoque de uma loja local. Apenas o gerente e alguns funcionários específicos devem ter acesso para modificar os dados.
    * **Aplicação:** O aplicativo solicita nome de usuário e senha na inicialização, usando um mecanismo de login similar para permitir o acesso apenas aos usuários com as credenciais corretas.
