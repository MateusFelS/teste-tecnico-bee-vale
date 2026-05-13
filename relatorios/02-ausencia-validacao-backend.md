# Falha - Ausência de validação server-side em campos críticos de cadastro

## Descrição
Diversos campos do sistema aceitam valores semanticamente inválidos sem qualquer validação aparente no backend.

Durante os testes, foi possível cadastrar:
- Nome completo contendo apenas números
- Cargo contendo valores arbitrários
- CPF inválido
- Telefone inválido
- Salário com valores alfabéticos

O comportamento indica ausência de validação server-side e possível confiança excessiva nas validações do frontend.

---

## Ambiente de Teste
- **Ambiente:** QA
- **SO:** Windows 11
- **Navegador:** Brave

---

## Passos para reproduzir
1. Acessar o formulário de cadastro de colaborador
2. Preencher os campos com valores inválidos:
   - Nome: `11111`
   - Cargo: `11111`
   - CPF: `123`
   - Telefone: `abc`
   - Salário: `teste`
3. Clicar no botão "Salvar Colaborador"

---

## Resultado Esperado
O sistema deve validar tipos, formato e consistência dos dados antes da persistência.

---

## Resultado Obtido
Os dados inválidos são aceitos e persistidos normalmente.

---

## Impacto
- Corrupção de integridade de dados
- Possíveis falhas em relatórios e integrações
- Inconsistência operacional
- Indício de ausência de validação backend

---

## Severidade
Baixa

---

## Evidência
- [Validação ausente ](https://github.com/user-attachments/assets/c0d8beae-ad54-4cd6-8128-2bcdc0507f41)
