# Casos de Teste - ProvaCar

Ambiente: provaqa.fandi.com.br
Pré-condição geral: acessar o site e clicar em iniciar

## Cadastro

| ID | Título | Passos | Resultado esperado | Resultado obtido |
|---|---|---|---|---|
| CT001 | Cadastrar veículo com todos os campos válidos | 1. Abrir o cadastro 2. Preencher todos os campos com dados válidos 3. Clicar em salvar | Mensagem de sucesso e veículo na lista | Passou |
| CT002 | Salvar com todos os campos vazios | 1. Abrir o cadastro 2. Clicar em salvar sem preencher nada | Sistema bloqueia e indica os campos obrigatórios | Passou |
| CT003 | Salvar com apenas alguns campos preenchidos | 1. Preencher só parte dos campos 2. Clicar em salvar | Sistema bloqueia e indica o que falta | Passou |
| CT004 | Campos numéricos rejeitam letras | 1. Digitar letras nos campos de ano | Só números são aceitos | Passou |
| CT005 | Cadastrar o mesmo veículo duas vezes | 1. Cadastrar um veículo 2. Cadastrar outro com os mesmos dados | Sistema bloqueia e avisa que já existe | Falhou (BUG003) |
| CT006 | Ano final com valor absurdo | 1. Preencher ano final com 999999999 2. Salvar | Sistema bloqueia e informa ano inválido | Falhou (BUG004) |
| CT007 | Ano inicial com valor absurdo | 1. Preencher ano inicial com 999999999 2. Salvar | Sistema bloqueia e informa ano inválido | falhou  |
| CT008 | Ano final menor que o ano inicial | 1. Ano inicial 2020 e ano final 2010 2. Salvar | Sistema bloqueia | falhou |
| CT009 | Campos de texto com acentos e caracteres especiais | 1. Digitar texto com acentos 2. Salvar | Dados salvos e exibidos corretamente | Passou |
| CT010 | Campos de texto com texto muito longo | 1. Digitar um texto enorme 2. Salvar | Sistema limita o tamanho ou o layout se mantém | falhou |
| CT011 | Clicar duas vezes rápido em salvar | 1. Preencher o cadastro 2. Clicar duas vezes em salvar | Só um registro criado | falhou |

## Filtro e consulta

| ID | Título | Passos | Resultado esperado | Resultado obtido |
|---|---|---|---|---|
| CT012 | Filtrar por tipo Automóvel | 1. Selecionar Automóvel no filtro | Marcas e modelos de automóvel listados | Passou |
| CT013 | Filtrar por Utilitário | 1. Selecionar Utilitário | Marcas e modelos listados | Falhou (BUG005) |
| CT014 | Filtrar por Caminhão | 1. Selecionar Caminhão | Marcas e modelos listados | Falhou (BUG005) |
| CT015 | Filtrar por Ônibus | 1. Selecionar Ônibus | Marcas e modelos listados | Falhou (BUG005) |
| CT016 | Filtrar por Implemento | 1. Selecionar Implemento | Marcas e modelos listados | Falhou (BUG005) |
| CT017 | Filtrar por Motocicleta | 1. Selecionar Motocicleta | Marcas e modelos listados | Falhou (BUG005) |
| CT018 | Filtrar por Máquina | 1. Selecionar Máquina | Marcas e modelos listados | Falhou (BUG005) |
| CT019 | Texto das opções do filtro sem erro de grafia | 1. Abrir a lista de tipos 2. Ler as opções | Todas escritas corretamente | Falhou (BUG006) |
| CT020 | Modelo só lista opções da marca escolhida | 1. Selecionar uma marca 2. Abrir a lista de modelos | Só modelos daquela marca | Passou |
| CT021 | Mensagem quando não há registros | 1. Aplicar filtro sem resultado | Mensagem "Nenhum registro encontrado" | Falhou (MEL002) |

## Edição

| ID | Título | Passos | Resultado esperado | Resultado obtido |
|---|---|---|---|---|
| CT022 | Dados carregam corretos ao abrir a edição | 1. Clicar em editar em um registro 2. Conferir os campos | Cada campo mostra seu valor (ano inicial e final corretos) | Falhou (BUG001) |
| CT023 | Editar e salvar um registro | 1. Editar um campo 2. Salvar 3. Procurar na lista | Mensagem de sucesso e registro atualizado na lista | Falhou (BUG002) |
| CT024 | Cancelar a edição descarta as mudanças | 1. Editar um campo 2. Clicar em cancelar 3. Reabrir o registro | Valores originais mantidos | Passou |
| CT025 | Salvar edição sem alterar nada | 1. Abrir a edição 2. Salvar sem mudar | Aviso de que não houve alteração | Falhou (MEL006) |

## Exclusão

| ID | Título | Passos | Resultado esperado | Resultado obtido |
|---|---|---|---|---|
| CT026 | Excluir um registro | 1. Clicar em excluir | Registro removido da lista | Passou |
| CT027 | Confirmação antes de excluir | 1. Clicar em excluir | Janela pedindo confirmação | Falhou (MEL001) |
| CT028 | Excluir vários registros seguidos | 1. Excluir 3 registros em sequência | Todos removidos sem erro | Passou |

## Geral

| ID | Título | Passos | Resultado esperado | Resultado obtido |
|---|---|---|---|---|
| CT029 | Dados persistem ao recarregar | 1. Cadastrar, editar e excluir 2. Recarregar (F5) | Dados mantidos | Falhou (BUG007) |
| CT030 | Layout com janela reduzida | 1. Reduzir a janela | Layout se adapta sem cortes | Passou |
| CT031 | Navegação por Tab | 1. Navegar pelos campos com Tab | Foco passa por todos os campos na ordem | Passou |
| CT032 | Sem erro técnico ou tela em branco | 1. Usar todas as funções | Nenhum erro técnico | Passou |