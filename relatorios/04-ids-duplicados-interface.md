# Falha - IDs duplicados exibidos para colaboradores distintos

## Descrição
Foi identificada inconsistência na exibição dos identificadores de colaboradores na interface do sistema.

Durante os testes, múltiplos colaboradores distintos foram apresentados utilizando o mesmo ID visual (`#7`), apesar de possuírem dados diferentes.

Os registros permaneceram independentes durante operações de edição e exclusão, indicando possível inconsistência de renderização ou mapeamento incorreto dos identificadores no frontend.

---

## Ambiente de Teste
- **Ambiente:** QA
- **SO:** Windows 11
- **Navegador:** Brave

---

## Passos para reproduzir
1. Criar múltiplos colaboradores
2. Acessar a listagem de colaboradores
3. Observar os identificadores exibidos na tabela

---

## Resultado Esperado
Cada colaborador deve possuir um identificador visual único e consistente.

---

## Resultado Obtido
Múltiplos colaboradores distintos são exibidos utilizando o mesmo identificador visual.

---

## Impacto
- Ambiguidade operacional
- Possível confusão durante gerenciamento de registros
- Redução da confiabilidade da interface

---

## Severidade
Baixa

---

## Evidência
- [IDs duplicados]("https://github.com/user-attachments/assets/4a388cd0-87bb-46f0-9aa3-c96cfb53b512")
