# :test_tube: Script de Teste Manual — E-vini IA (Sommelier Digital Evino)

## :dart: Objetivo

Validar o fluxo conversacional do chat de recomendação de vinhos E-vini IA, incluindo:


Interação pelo menu inicial
Entrada por texto e áudio
Recomendações de produtos
Refinamentos (ex.: Mais opções, Vinhos brancos)
Adição e gerenciamento do carrinho
Continuidade da conversa
Redirecionamento para checkout da Evino


---

## :gear: Pré-condições


Conexão com internet ativa
Permissão de microfone habilitada
Navegador suportado (Safari iOS, Chrome Android ou Desktop)
Carrinho vazio (quando aplicável)


---

## :test_tube: Cenários de Teste

---

### :one: Chat Inicial e Menu

| ID | Caso de Teste | Passos | Resultado Esperado |
|----|--------------|--------|--------------------|
| CT-001 | Carregar chat | Acessar a URL do E-vini IA | Mensagem inicial e opções do menu exibidas |
| CT-002 | Selecionar opção do menu | Clicar em cada opção disponível | Bot retorna recomendações relacionadas |
| CT-003 | Enviar mensagem digitada | Digitar “Quero um vinho branco leve” | Sugestões coerentes exibidas |

---

### :two: Interação por Voz

| ID | Caso | Passos | Resultado Esperado |
|----|------|--------|--------------------|
| CT-004 | Permitir microfone | Clicar no ícone de microfone | Sistema inicia captura de áudio |
| CT-005 | Enviar comando por voz | Falar “Vinho para churrasco” | Recomendações adequadas exibidas |
| CT-006 | Negar permissão | Negar acesso ao microfone | Mensagem orientativa exibida sem quebrar o fluxo |

---

### :three: Recomendações de Produtos

| ID | Caso | Passos | Resultado Esperado |
|----|------|--------|--------------------|
| CT-007 | Exibir cards | Selecionar “Destaques de Portugal” | Cards com nome, preço e botão "+" |
| CT-008 | Validar layout | Analisar 3 produtos | Informações legíveis e alinhadas |
| CT-009 | Rolagem | Rolar lista de produtos | Navegação fluida sem travamentos |

---

### :four: Refinamentos

| ID | Caso | Passos | Resultado Esperado |
|----|------|--------|--------------------|
| CT-010 | Mais opções | Clicar em “Mais opções” | Novos vinhos exibidos |
| CT-011 | Vinhos brancos | Selecionar filtro | Resultados filtrados corretamente |
| CT-012 | Troca de filtros | Alternar filtros | Contexto da conversa mantido |

---

### :five: Carrinho

| ID | Caso | Passos | Resultado Esperado |
|----|------|--------|--------------------|
| CT-013 | Adicionar produto | Clicar no botão "+" | Produto adicionado ao carrinho |
| CT-014 | Abrir carrinho | Abrir modal | Produto listado corretamente |
| CT-015 | Alterar quantidade | Utilizar +/- | Total recalculado |
| CT-016 | Remover item | Clicar no X | Item removido |
| CT-017 | Fechar carrinho | Fechar modal | Retorno ao chat |

---

### :six: Continuar Conversando vs Checkout

| ID | Caso | Passos | Resultado Esperado |
|----|------|--------|--------------------|
| CT-018 | Continuar conversa | Clicar “Continuar conversando” | Chat permanece ativo |
| CT-019 | Finalizar compra | Clicar checkout | Redirecionamento correto para Evino |
| CT-020 | Retornar ao chat | Voltar após checkout | Estado da conversa preservado |

---

### :seven: Cenários de Exceção

| ID | Caso | Passos | Resultado Esperado |
|----|------|--------|--------------------|
| CT-021 | Mensagem vazia | Enviar sem texto | Ação bloqueada |
| CT-022 | Sem internet | Desconectar rede | Mensagem de erro amigável |
| CT-023 | Texto longo | Enviar texto extenso | Interface permanece estável |
| CT-024 | Acessibilidade | Aumentar zoom/fonte | Layout continua utilizável |

---

## :paperclip: Evidências


Screenshots
Gravações de tela
Dispositivo / Navegador
Data e hora
Resultado esperado vs obtido