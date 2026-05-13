# Falha - Autenticação permite login com senha vazia

## Descrição  
O sistema permite autenticação utilizando apenas um nome de usuário válido, sem necessidade de informar senha. Durante os testes, foi possível acessar contas deixando o campo de senha vazio.

O comportamento indica ausência ou falha na validação server-side durante o processo de autenticação.

---

## Ambiente de Teste
- **Ambiente:** QA
- **SO:** Windows 11
- **Navegador:** Brave

---

## Passos para reproduzir
1. Acessar a tela de login
2. Informar um usuário válido
3. Deixar o campo de senha vazio
4. Clicar no botão "Entrar"

---

## Resultado Esperado
O sistema deve bloquear autenticações com senha vazia e retornar mensagem de credenciais inválidas.

---

## Resultado Obtido
O sistema autentica o usuário com sucesso mesmo sem senha informada.

---

## Impacto
- Possível acesso não autorizado
- Comprometimento de contas
- Falha no fluxo de autenticação

---

## Severidade
Alta

---

## Evidência
(Autenticação com senha vazia)[https://github.com/user-attachments/assets/a9196a2a-26f3-410b-9b3f-66b159cdb3da]
