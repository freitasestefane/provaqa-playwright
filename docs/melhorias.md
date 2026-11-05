# Melhorias - ProvaCar

Ambiente: provaqa.fandi.com.br

---

## MEL001 - Pedir confirmação antes de excluir um veículo
**Onde:** botão de excluir na lista de veículos
**Situação atual:** o registro é excluído imediatamente, sem nenhum aviso
**Sugestão:** exibir uma janela perguntando "Deseja realmente excluir este veículo?" com as opções Confirmar e Cancelar
**Benefício:** evita exclusões acidentais e perda de dados por um clique errado

---

## MEL002 - Exibir mensagem quando não houver registros
**Onde:** lista de veículos e resultado do filtro
**Situação atual:** quando não há registros (ou o filtro não retorna nada), a área fica vazia, sem nenhuma informação
**Sugestão:** mostrar a mensagem "Nenhum registro encontrado"
**Benefício:** o usuário entende que a busca não trouxe resultado e que não se trata de uma falha do sistema

---

## MEL003 - Validar a faixa dos anos e a relação entre eles
**Onde:** campos ano inicial e ano final (cadastro e edição)
**Situação atual:** não há limite de caracteres nem de valor (aceita, por exemplo, 999999999)
**Sugestão:** limitar a 4 dígitos, definir uma faixa de anos válida e bloquear ano final menor que o ano inicial
**Benefício:** dados consistentes e confiáveis na base de veículos

---

## MEL004 - Limitar o tamanho dos campos de texto
**Onde:** campos de texto do cadastro e da edição
**Situação atual:** aceita textos muito longos
**Sugestão:** definir um limite máximo de caracteres por campo, com contador ou mensagem
**Benefício:** evita quebra de layout e dados fora do padrão

---

## MEL005 - Avisar quando o usuário salva sem alterar nada
**Onde:** tela de edição
**Situação atual:** ao salvar sem mudar nenhum dado, aparece "Veículo atualizado com sucesso"
**Sugestão:** exibir "Nenhuma alteração foi realizada" ou desabilitar o botão salvar até haver mudança
**Benefício:** mensagens fiéis à realidade e menos confusão para o usuário

---

## MEL006 - Revisar a ortografia e os textos da tela
**Onde:** toda a interface
**Situação atual:** existe pelo menos um erro de grafia ("mýquina")
**Sugestão:** revisar todos os textos, rótulos e mensagens
**Benefício:** passa mais profissionalismo e evita dúvida de leitura