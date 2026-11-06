# Checklist — Cadastro

Data: 06/11/2026. Resultado: 18 verificações aprovadas e 5 falhas, cobrindo os 10 requisitos da atividade.

[Planilha da atividade](https://docs.google.com/spreadsheets/d/1LxCWMtFeZuUBgDT7C5OQpaZETEot1Ny1z9kFQNl4AR4/edit)

Foram usadas classes de equivalência (dados válidos e inválidos) e valores de limite (senhas de 7, 8 e 9 caracteres). A senha deve ter pelo menos 8 caracteres e incluir minúscula, maiúscula, número e símbolo, conforme os requisitos do exercício.

| Nº | Requisito | Verificação | Prioridade | Resultado | Comentário |
|---|---|---|---|---|---|
| 1 | JS-REQ-001 | Cadastro com todos os dados válidos | Critical | Passed | Cadastro concluído e mensagem de sucesso exibida. |
| 2 | JS-REQ-001 | Aceitar e-mail em formato válido | High | Passed | E-mail válido aceito no cadastro. |
| 3 | JS-REQ-001 | Recusar e-mail sem @ | High | Passed | Apareceu Email address is not valid. |
| 4 | JS-REQ-001 | Recusar e-mail sem domínio | High | Passed | Apareceu Email address is not valid. |
| 5 | JS-REQ-002 | Impedir cadastro com e-mail já usado | Critical | Passed | Apareceu Email must be unique; a tela de cadastro permaneceu aberta. |
| 6 | JS-REQ-003 | Recusar senha com 7 caracteres | Critical | Failed | O cadastro foi concluído com 7 caracteres, embora o requisito peça pelo menos 8. |
| 7 | JS-REQ-003 | Aceitar senha válida com 8 caracteres | High | Passed | O cadastro foi concluído com senha válida de 8 caracteres. |
| 8 | JS-REQ-003 | Aceitar senha válida com 9 caracteres no formulário | High | Passed | O botão Register ficou habilitado. Não houve envio neste caso. |
| 9 | JS-REQ-004 | Recusar senha sem letra minúscula no formulário | High | Failed | O botão Register ficou habilitado mesmo sem minúscula. Não houve envio neste caso. |
| 10 | JS-REQ-004 | Recusar senha sem letra maiúscula no formulário | High | Failed | O botão Register ficou habilitado mesmo sem maiúscula. Não houve envio neste caso. |
| 11 | JS-REQ-004 | Recusar senha sem número no formulário | High | Failed | O botão Register ficou habilitado mesmo sem número. Não houve envio neste caso. |
| 12 | JS-REQ-004 | Recusar senha sem símbolo especial | High | Failed | O cadastro foi concluído com uma senha sem símbolo. |
| 13 | JS-REQ-005 | Aceitar confirmação igual à senha | High | Passed | Senhas iguais foram aceitas no cadastro concluído. |
| 14 | JS-REQ-005 | Recusar confirmação diferente da senha | High | Passed | Apareceu Passwords do not match e o botão ficou desativado. |
| 15 | JS-REQ-006 | Dicas de senha desativadas ao abrir o cadastro | High | Passed | A opção Show password advice estava desligada. |
| 16 | JS-REQ-007 | Exibir todas as dicas de senha ao ativar a opção | High | Passed | Apareceram as cinco regras de senha. |
| 17 | JS-REQ-008 | Exibir e selecionar perguntas de segurança | High | Passed | As perguntas apareceram e foi possível escolher uma. |
| 18 | JS-REQ-009 | Impedir cadastro sem e-mail | Critical | Passed | Apareceu aviso de e-mail obrigatório e o botão ficou desativado. |
| 19 | JS-REQ-009 | Impedir cadastro sem senha | Critical | Passed | Apareceu aviso de senha obrigatória e o botão ficou desativado. |
| 20 | JS-REQ-009 | Impedir cadastro sem repetir a senha | Critical | Passed | Apareceu aviso para repetir a senha e o botão ficou desativado. |
| 21 | JS-REQ-009 | Impedir cadastro sem pergunta de segurança | Critical | Passed | O botão ficou desativado até selecionar uma pergunta. |
| 22 | JS-REQ-009 | Impedir cadastro sem resposta de segurança | Critical | Passed | Apareceu aviso de resposta obrigatória e o botão ficou desativado. |
| 23 | JS-REQ-010 | Abrir login pelo link Already a customer? | High | Passed | O link abriu o formulário de login. |

## Falhas encontradas

- O sistema concluiu cadastro com senha de 7 caracteres.
- O sistema manteve o botão de cadastro habilitado sem minúscula, maiúscula ou número. Nesses três casos, a verificação foi feita no formulário, sem enviar o cadastro.
- O sistema concluiu cadastro com senha sem símbolo especial.

Não foram testadas outras combinações além das registradas acima.
