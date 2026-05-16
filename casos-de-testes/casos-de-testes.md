# Casos de Teste — SysColaborator

| ID | Cenário | Pré-condição | Dados de Teste | Passo a Passo | Resultado Esperado |
|---|---|---|---|---|---|
| CT-001 | Login com credenciais válidas | Sistema disponível | Usuário: `admin`<br>Senha: `admin123` | 1. Acessar sistema<br>2. Informar credenciais válidas<br>3. Clicar em login | Sistema deve autenticar e acessar dashboard |
| CT-002 | Login com usuário inválido | Sistema disponível | Usuário: `admin123`<br>Senha: `admin123` | 1. Informar usuário inválido<br>2. Informar senha válida<br>3. Clicar em login | Sistema deve impedir acesso e exibir mensagem de erro |
| CT-003 | Login com senha inválida | Sistema disponível | Usuário: `admin`<br>Senha: `123admin` | 1. Informar usuário válido<br>2. Informar senha inválida<br>3. Clicar em login | Sistema deve impedir acesso e exibir mensagem de erro |
| CT-004 | Login com campos vazios | Sistema disponível | Usuário: vazio<br>Senha: vazia | 1. Não preencher campos<br>2. Clicar em login | Sistema deve validar obrigatoriedade dos campos |
| CT-005 | Dashboard após login | Usuário autenticado | Não aplicável | 1. Realizar login | Dashboard deve exibir indicadores e atividades recentes |
| CT-006 | Pesquisa de colaborador existente | Usuário autenticado | Nome: `João` | 1. Acessar colaboradores<br>2. Pesquisar nome | Sistema deve localizar colaborador correspondente |
| CT-007 | Pesquisa de colaborador inexistente | Usuário autenticado | Nome: `XYZTeste` | 1. Pesquisar colaborador inexistente | Sistema deve informar ausência de resultados |
| CT-008 | Filtro por departamento | Usuário autenticado | Departamento: `TI` | 1. Selecionar departamento | Sistema deve listar apenas colaboradores do setor |
| CT-009 | Ordenação por nome | Usuário autenticado | Não aplicável | 1. Aplicar ordenação | Sistema deve ordenar alfabeticamente |
| CT-010 | Cadastro com dados válidos | Usuário autenticado | Nome: João da Silva<br>Email: joao@email.com<br>CPF: 12345678900<br>Salário: 5000 | 1. Preencher formulário<br>2. Salvar | Sistema deve cadastrar colaborador |
| CT-011 | Cadastro sem nome | Usuário autenticado | Nome vazio | 1. Deixar nome vazio<br>2. Salvar | Sistema deve validar campo obrigatório |
| CT-012 | Cadastro sem e-mail | Usuário autenticado | E-mail vazio | 1. Deixar e-mail vazio<br>2. Salvar | Sistema deve validar campo obrigatório |
| CT-013 | Cadastro sem departamento | Usuário autenticado | Departamento vazio | 1. Não selecionar departamento<br>2. Salvar | Sistema deve validar campo obrigatório |
| CT-014 | Cadastro sem cargo | Usuário autenticado | Cargo vazio | 1. Não preencher cargo<br>2. Salvar | Sistema deve validar campo obrigatório |
| CT-015 | Cadastro sem data de admissão | Usuário autenticado | Data vazia | 1. Não preencher data<br>2. Salvar | Sistema deve validar campo obrigatório |
| CT-016 | Nome com números | Usuário autenticado | Nome: `João123` | 1. Informar nome com números<br>2. Salvar | Sistema deve impedir cadastro ou validar formato inválido |
| CT-017 | Nome com caracteres especiais inválidos | Usuário autenticado | Nome: `@@@###` | 1. Informar caracteres inválidos<br>2. Salvar | Sistema deve validar formato do nome |
| CT-018 | CPF com letras | Usuário autenticado | CPF: `abc123xyz` | 1. Informar CPF inválido<br>2. Salvar | Sistema deve validar CPF numérico |
| CT-019 | CPF incompleto | Usuário autenticado | CPF: `12345` | 1. Informar CPF incompleto<br>2. Salvar | Sistema deve validar quantidade de dígitos |
| CT-020 | E-mail inválido sem @ | Usuário autenticado | E-mail: `joaoemail.com` | 1. Informar e-mail inválido<br>2. Salvar | Sistema deve validar formato do e-mail |
| CT-021 | E-mail inválido sem domínio | Usuário autenticado | E-mail: `joao@` | 1. Informar e-mail inválido<br>2. Salvar | Sistema deve validar formato do e-mail |
| CT-022 | Telefone com letras | Usuário autenticado | Telefone: `abc999` | 1. Informar telefone inválido<br>2. Salvar | Sistema deve validar telefone numérico |
| CT-023 | Salário com letras | Usuário autenticado | Salário: `cinco mil` | 1. Informar salário inválido<br>2. Salvar | Sistema deve validar valor numérico |
| CT-024 | Salário negativo | Usuário autenticado | Salário: `-5000` | 1. Informar salário negativo<br>2. Salvar | Sistema deve impedir valor negativo |
| CT-025 | Data de admissão futura | Usuário autenticado | Data: `01/01/2035` | 1. Informar data futura<br>2. Salvar | Sistema deve validar data inválida |
| CT-026 | Seleção de status | Usuário autenticado | Status: Ativo/Inativo/Férias/Afastado | 1. Abrir campo status | Sistema deve listar todos os status disponíveis |
| CT-027 | Edição de colaborador | Colaborador existente | Alterar cargo | 1. Editar colaborador<br>2. Salvar alterações | Sistema deve atualizar informações |
| CT-028 | Exclusão de colaborador | Colaborador existente | Não aplicável | 1. Excluir colaborador<br>2. Confirmar ação | Sistema deve remover colaborador da lista |
| CT-029 | Cancelar exclusão de colaborador | Colaborador existente | Não aplicável | 1. Clicar excluir<br>2. Cancelar confirmação | Sistema não deve excluir colaborador |
| CT-030 | Cadastro com campos máximos | Usuário autenticado | Observação com texto longo | 1. Preencher campos extensos<br>2. Salvar | Sistema deve salvar sem quebrar layout |
| CT-031 | Cadastro duplicado de e-mail | Usuário autenticado | E-mail já existente | 1. Cadastrar colaborador com e-mail repetido | Sistema deve impedir duplicidade |
| CT-032 | Cadastro duplicado de CPF | Usuário autenticado | CPF já existente | 1. Cadastrar colaborador com CPF repetido | Sistema deve impedir duplicidade |
| CT-033 | Logout do sistema | Usuário autenticado | Não aplicável | 1. Clicar em sair/logout | Sistema deve encerrar sessão e voltar para login |
