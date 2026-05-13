# SysColaborador - Avaliação de Segurança

## Descrição

Este repositório contém os resultados da avaliação funcional e de segurança realizada na aplicação **SysColaborador**, disponibilizada como ambiente de teste técnico.

Os testes foram executados manualmente com foco em:

- autenticação;
- validação de entrada;
- integridade de dados;
- comportamento da interface;
- consistência funcional.

---

## Escopo Avaliado

- Fluxo de autenticação
- Cadastro de colaboradores
- Listagem e gerenciamento de registros
- Comportamento da interface administrativa

---

## Relatórios

| ID | Título | Severidade |
|---|---|---|
| 01 | Autenticação permite senha vazia | Alto |
| 02 | Ausência de validação server-side | Baixo |
| 03 | Elementos de interface sem funcionalidade | Baixo |
| 04 | IDs duplicados exibidos na interface | Baixo |

---

## Estrutura

```txt
/relatorios  -> relatórios detalhados
```
