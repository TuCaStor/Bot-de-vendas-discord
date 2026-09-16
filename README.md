# ⚙️ Moshiini_ Automações

Bot Discord completo para lojas virtuais com sistema de pagamentos via PIX, tickets, painéis de produtos, cupons de desconto, sistema de convites com recompensa, moderação anti-hack e muito mais.

Multi-servidor: cada servidor configura sua própria loja com produtos, preços, chave PIX, painéis e regras — de forma 100% independente.

> 💰 **Novo na v5.0: o bot agora é FREMIUM** — gratuito com limites (5 produtos e 2 painéis por servidor, vendas ilimitadas), sem taxa e sem comissão. Quer mais? A licença Premium destrava tudo.

---

## 🧭 Comece por aqui — escolha seu caminho

| Você é... | Caminho |
|---|---|
| 📱 **Usuário de celular** | Seção **"Guia do Usuário de Celular"** — tudo pelo Dashboard, sem digitar nada |
| 💻 **Usuário de PC** | Seção **"Guia do Usuário de PC"** — todos os comandos com exemplos |
| 🛍️ **Só quero comprar** | Seção **"Comprando pelo painel da loja"** — funciona igual no celular e no PC |
| 👑 **Dono de servidor, 1ª vez** | Seção **"Passo a Passo"** — configure sua loja em 10 minutos |

> 💡 **Dica**: todos os comandos exibem uma **tag de permissão** na descrição (ex.: `[ADMINS]`, `[TODOS]`) — ao digitar o comando no Discord você já vê quem pode usá-lo.

---

## 🚀 Adicione o Bot ao seu Servidor

```
https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot
```

> ⚠️ O bot precisa da permissão **Administrador** para funcionar corretamente (criar canais, cargos, gerenciar mensagens, bans, etc).

**Permissões essenciais:**
- ✅ Criar Convite (sistema de convites)
- ✅ Gerenciar Servidor (tracking de invites)
- ✅ Banir Membros (honeypot)
- ✅ Gerenciar Canais (tickets)
- ✅ Gerenciar Cargos (verificação, recompensas)
- ✅ Ler Histórico de Mensagens (transcripts)
- ✅ Gerenciar Mensagens (moderação)

---

## 💰 Planos

| | **Gratuito** 🆓 | **Premium** 💎 |
|---|---|---|
| Custo | R$ 0 — sem taxa, sem comissão | R$ 0,50/dia |
| Produtos | criar até **5** | **ilimitado** |
| Painéis | criar até **2** | **ilimitado** |
| Vendas, tickets, cupons, entrega | ✅ ilimitado | ✅ ilimitado |

- **Ativação instantânea**: `/loja vincular` — a loja já nasce no plano Gratuito, sem burocracia
- **Downgrade gracioso**: sua loja passou do limite quando a licença expirou? **Nada é removido nem bloqueado** — tudo continua vendendo; você só não cria itens novos até renovar ou excluir algo
- Produtos **inativos/desativados não contam** no limite
- Veja seu uso a qualquer momento: `/loja plano` (ex: "3/5 produtos, 1/2 painéis")
- Aumente o limite: `/loja mudardeplano`

---

## ⚡ Passo a Passo — Configure sua Loja em 10 Minutos

> Configuração feita **uma única vez** pelo dono do servidor (ou admins). Funciona no celular e no PC — cada passo usa 1 comando e o Discord te mostra os campos na tela.

| # | O que fazer | Como fazer | Tag |
|---|---|---|---|
| 1️⃣ | **Adicionar o bot** | Use o link de convite acima (permissão Administrador) | — |
| 2️⃣ | **Ativar a loja grátis** | Digite `/loja vincular` → a loja nasce no plano Gratuito na hora | `[DONO DO SERV]` |
| 3️⃣ | **Configurar o PIX** | `/configurar pix` → escolha o tipo e cole a chave (o bot criptografa antes de salvar) | `[ADMINS]` |
| 4️⃣ | **Definir os canais** | `/configurar canais` → canais de log, provas, carrinho e categoria de tickets | `[ADMINS]` |
| 5️⃣ | **Cadastrar produtos** | `/produto adicionar` → nome, preço (R$), estoque e descrição (até 5 no grátis) | `[GERENTE+]` |
| 6️⃣ | **Montar o painel da loja** | `/painel criar` → `/painel add_opcao` (liga o produto ao painel) → `/painel postar` (publica no canal) | `[GERENTE+]` |
| 7️⃣ | **Abrir o Dashboard** (essencial p/ celular) | `/gerenciar_loja dashboard_fixo` → painel fixo com botões de gestão | `[GERENTE+]` |
| 8️⃣ | **Extras (opcional)** | Honeypot: `/honeypot ativar` · Verificação: `/configurar verificacao definir` · Convites: `/convite admin_configurar` · Cupons: `/cupom admin_criar_publico` | `[GERENTE+]`/`[ADMINS]` |
| 9️⃣ | **Precisa de mais espaço?** | `/loja mudardeplano` → licença Premium (R$ 0,50/dia, criação ilimitada) | `[DONO DO SERV]` |

**Pronto!** Com o painel postado (passo 6) o servidor já pode vender. O Dashboard (passo 7) é o que deixa a gestão 100% por botões — perfeito para quem administra pelo celular.

---

## 📱 Guia do Usuário de Celular — Tudo pelo Dashboard

> No celular, digitar comando é trabalho braçal. Por isso o bot trabalha com **painéis fixos e botões**: você configura uma vez e depois é só tocar na tela.

### 🏪 O Dashboard da loja (para quem gerencia)

1. Alguém da equipe (gerente, admin ou o dono do servidor) digita `/gerenciar_loja dashboard_fixo` **uma única vez**, no canal de gestão da loja
2. O bot posta o **Dashboard fixo com botões de gestão rápida** — ele continua lá mesmo depois do bot reiniciar
3. A partir daí, a gestão inteira é no toque:
   - 🛍️ **Produtos**: adicionar, editar, ativar/desativar e excluir pelos botões
   - 🖼️ **Painéis**: criar e postar sem digitar comandos
   - 📊 **Estatísticas de vendas** e exportação de relatório
   - 💾 **Backup e restauração** da loja (com validação — só admins)
4. Comandos úteis para a equipe no celular (quando quiser):
   - `/gerenciar_loja estatisticas` — resumo de vendas do servidor
   - `/gerenciar_loja relatorio` — exporta as vendas em CSV
   - `/gerenciar_loja diagnostico` — checa a saúde das configurações
   - `/gerenciar_loja painel_controle` — painel de controle interativo

### 🛍️ Comprando pelo celular (clientes)

1. Abra o canal com o **painel da loja** (postado na configuração)
2. Toque no **menu suspenso** e escolha o produto
3. Use os botões da tela: **Comprar**, **Calcular R$→Qtd** ou **Calcular Qtd→R$**
4. No carrinho: ajuste quantidades, remova itens e aplique cupom (menu ou botão **"Aplicar Código"**)
5. Toque em **Finalizar Compra** → abre um ticket privado com o **QR Code PIX**
6. Anexe o **comprovante** no ticket → a staff confirma → entrega do produto
7. Avalie o atendimento com **estrelas** ⭐

### 👤 Sua área pessoal (botões, sem digitar)

- `/loja minha_loja` → hub pessoal com botões: **Ver Sacola**, **Histórico**, **Gasto Total** e **Cupons**
- **Suporte**: mande uma DM no bot — o modmail abre um ticket privado com a staff (dono de servidor/loja)
- **Trocas com segurança**: `/trocar enviar` convida alguém para uma troca com middleman e recibo anti-fraude — o convite chega na DM da pessoa

> ✅ **Resumo do celular**: 1 comando para o Dashboard (uma vez) + `/loja minha_loja` quando quiser. Todo o resto é botão.

---

## 🛍️ Comprando pelo painel da loja (celular e PC)

O fluxo de compra é o mesmo nas duas plataformas — tudo por menu e botões:

1. **Abra o painel da loja** no canal de compras
2. **Selecione o produto** no menu suspenso
3. Escolha na tela: **Comprar** · **Calcular R$→Qtd** · **Calcular Qtd→R$** (a calculadora mostra o valor antes de você se comprometer)
4. Confirme a quantidade → o item vai para a **sacola**
5. Aplique um **cupom** (se tiver) e clique em **Finalizar Compra**
6. Um **ticket privado** é aberto com o QR Code PIX
7. Envie o **comprovante** → a staff confirma → **entrega** do produto
8. Avalie com **estrelas** — e consulte tudo depois em `/minhascompras`

---

## 💻 Guia do Usuário de PC — Comandos com Exemplos

No PC digitar é rápido — então aqui vai o **guia completo dos 94 comandos**, organizados por quem pode usar. Cada comando também mostra a tag na descrição, dentro do Discord.

**Legenda das tags:**

| Tag | Quem pode usar |
|---|---|
| `[TODOS]` | Qualquer membro |
| `[GER. SERVIDOR]` | Quem tem a permissão "Gerenciar Servidor" |
| `[GERENTE+]` | Dono do servidor, admins **ou gerentes da loja** (nível ≥ 1) |
| `[ADMINS]` | Dono do servidor ou administradores (gerentes **não** entram) |
| `[DONO DO SERV]` | Somente o dono do servidor |
| `[DONO DO BOT]` | Somente o dono do bot |

### 👥 Comandos de cliente `[TODOS]`

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/loja minha_loja` | Hub pessoal com botões: sacola, histórico, gasto e cupons | `/loja minha_loja` → toca em "Ver Sacola" |
| `/sacola ver` | Mostra seu carrinho com subtotal, desconto e total | `/sacola ver` → ajusta quantidade e finaliza |
| `/minhascompras` | Lista suas últimas 10 compras nesta loja com status | `/minhascompras` |
| `/loja meugasto` | Quanto você já gastou e o próximo cargo de recompensa | `/loja meugasto` → "faltam R$ 50 pro cargo Comprador" |
| `/loja top` | Ranking dos maiores compradores do servidor | `/loja top` |
| `/loja robux calcular_robux` | Conversão R$ ↔ Robux (com ou sem a taxa de 30%) | informe `100` R$ e escolha "com taxa" |
| `/cupom resgatar` | Roleta de cupons: gasta mensagens acumuladas para tentar a sorte | `/cupom resgatar` → gira com o saldo de mensagens |
| `/cupom meuscupons` | Lista seus cupons disponíveis | `/cupom meuscupons` |
| `/convite criar` | Gera seu link de convite rastreado (1 ciclo por vez) | `/convite criar` → compartilha o link |
| `/convite meu_convite` | Recupera o link do seu convite ativo | `/convite meu_convite` |
| `/convite status` | Seu progresso no ciclo atual | `/convite status` → "3/5 convites" |
| `/convite resgatar` | Abre ticket para receber a recompensa ao bater a meta | `/convite resgatar` |
| `/convite ranking` | Top 10 convidadores do servidor | `/convite ranking` |
| `/sorteio minhasmensagens` | Seu saldo de mensagens para sorteios com requisito | `/sorteio minhasmensagens` |
| `/trocar enviar` | Convida alguém para uma troca com middleman (MM) | `/trocar enviar` → escolhe a pessoa → convite na DM dela (expira em 15 min) |
| `/trocar aceitar` | Aceita a troca — abre o ticket privado dos dois lados | `/trocar aceitar` após receber o convite |
| `/trocar verificar` | Valida a assinatura digital de um recibo | anexe o recibo no comando → bot confirma autenticidade |
| `/status_publico` | Resumo público do bot (servidores, membros, vendas) | `/status_publico` |
| `/sugestao` | Envia sugestão direto pro dono do bot (1 a cada 24h) | `/sugestao` → "adiciona pagamento via card" |

**Fluxo do sistema de convites:**
1. `/convite criar` → recebe um link personalizado
2. Compartilhe → cada entrada pelo link soma +1 no seu contador
3. Bateu a meta (ex: 5)? Chega uma **DM avisando**
4. `/convite resgatar` → ticket com a staff + prêmio (+ cargo automático, se configurado)
5. O ciclo encerra → pode criar outro convite e continuar ganhando

### 🛠️ Comandos da equipe `[GERENTE+]` (dono, admins e gerentes da loja)

**Produtos:**

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/produto adicionar` | Novo produto (respeita o limite do plano) | nome: `Mush` · preço: `2.50` · estoque: `10000` |
| `/produto editar` | Edita um produto existente | muda só o preço, o resto fica |
| `/produto info` | Detalhes de um produto | preço, estoque, vendas |
| `/produto listar` | Lista todos com menu de ações (editar/excluir) | `/produto listar` → seleciona na lista |
| `/produto status` | Ativa/desativa *(inativos não contam no limite!)* | desativa produto fora de época |
| `/produto excluir` | Exclui um produto | `/produto excluir` |
| `/produto limiar_estoque` | Aviso automático de estoque baixo | define mínimo `50` → bot avisa ao atingir |

**Painéis:**

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/painel criar` | Novo painel (respeita o limite do plano) | título: `Loja de Mush` + banner e cor |
| `/painel add_opcao` | Liga um produto ao painel | adiciona `Mush` ao painel criado |
| `/painel remover_opcao` | Remove produto do painel | `/painel remover_opcao` |
| `/painel editar` | Edita texto, imagens e cor do painel | troca o banner de temporada |
| `/painel editar_opcao` | Edita um item do painel | `/painel editar_opcao` |
| `/painel postar` | Publica (ou move) o painel num canal — já com produtos e estoque | posta no `#loja` |
| `/painel sync` | Re-sincroniza o painel com o banco | após edição em massa de preços |
| `/painel excluir` | Exclui o painel | `/painel excluir` |

**Gestão da loja e honeypot:**

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/gerenciar_loja painel_controle` | Painel de controle interativo | `/gerenciar_loja painel_controle` |
| `/gerenciar_loja dashboard_fixo` | Dashboard fixa com botões (ideal p/ celular) | posta no canal de gestão |
| `/gerenciar_loja estatisticas` | Resumo de vendas do servidor | `/gerenciar_loja estatisticas` |
| `/gerenciar_loja relatorio` | Exporta CSV de vendas | `/gerenciar_loja relatorio` |
| `/gerenciar_loja diagnostico` | Saúde das configurações (pix, canais…) | `/gerenciar_loja diagnostico` |
| `/honeypot ativar` | Canal vira armadilha: quem envia mensagem = ban | cria `#🪤-armadilha` → ativa nele |
| `/honeypot desativar` | Desativa a armadilha | `/honeypot desativar` |
| `/honeypot status` | Estado do honeypot + bans ativos | `/honeypot status` |
| `/honeypot desbanir` | Remove o ban honeypot manualmente | `/honeypot desbanir` → escolhe o usuário |

**Como funciona o honeypot:** crie um canal privado → `/honeypot ativar` nele → o bot fixa um aviso → quem mandar mensagem leva ban temporário (mensagem deletada) e é desbanido sozinho após X dias (padrão 7). Toda a staff é isenta.

### 🔐 Comandos de administrador `[ADMINS]`

**Configuração do servidor:**

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/configurar pix` | Define a chave PIX (criptografada no banco) | cola a chave aleatória/e-mail/telefone |
| `/configurar canais` | Canais de log, provas, carrinho, categoria de tickets | `/configurar canais` → preenche os campos |
| `/configurar campo_entrega` | Texto do campo Nick/ID na compra | "Informe seu usuário do jogo" |
| `/configurar cargo_suporte adicionar` | Cargo passa a ver os tickets | adiciona `Staff` |
| `/configurar cargo_suporte remover` | Remove cargo dos tickets | `/configurar cargo_suporte remover` |
| `/configurar cargo_suporte listar` | Lista cargos de suporte | `/configurar cargo_suporte listar` |
| `/configurar canal_ignorado adicionar` | Canal sai da contagem de mensagens | ignora `#comandos-bot` |
| `/configurar canal_ignorado remover` | Canal volta à contagem | `/configurar canal_ignorado remover` |
| `/configurar canal_ignorado listar` | Lista canais ignorados | `/configurar canal_ignorado listar` |
| `/configurar verificacao definir` | Canal + cargo da verificação (captcha por DM) | define `#verificar` + cargo `Membro` |
| `/verificacao postar_painel` | Posta o painel de verificação | posta no canal de entrada |
| `/recompensa adicionar` | Cargo automático por valor gasto | gasto `R$ 100` → cargo `Comprador` |
| `/recompensa remover` | Remove uma recompensa | `/recompensa remover` |
| `/recompensa listar` | Lista as recompensas ativas | `/recompensa listar` |

**Cupons e convites (admin):**

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/cupom admin_criar_publico` | Cupom público com código digitável | código: `NATAL10` · desconto: `10%` · usos: `100` |
| `/cupom admin_criar_tipo` | Cupom de sorteio (resgate com mensagens) | `/cupom admin_criar_tipo` |
| `/cupom admin_listar` | Lista todos os cupons e códigos | `/cupom admin_listar` |
| `/cupom admin_excluir` | Exclui tipo ou código | `/cupom admin_excluir` |
| `/cupom admin_remover_tipo` | Impede um tipo de ser sorteado | `/cupom admin_remover_tipo` |
| `/convite admin_configurar` | Configura o sistema de convites | meta: `5` · recompensa: cargo/prêmio · categoria do ticket |
| `/convite admin_desativar` | Desativa o sistema | `/convite admin_desativar` |

**Parâmetros especiais de cupom** (no criar): `produto` (vincula o desconto a um produto só) · `quantidade_minima` (ex.: `5000`; use `-1` para "leva tudo") · `mostrar_painel` (exibe o cupom no painel) · `auto_aplicar` (sugere ao adicionar no carrinho).

**Exemplos de cupons prontos:**
- `NATAL10` — 10% OFF global
- `MUSH10` — 10% OFF só no produto "Mush" (vinculado)
- `BULK10` — 10% OFF exigindo 5000 unidades de Mush
- `LEVATUDO` — 20% OFF exigindo TODO o estoque atual de Mush

**Backup da loja** (contém dados financeiros — checagem extra):

| Comando | O que faz |
|---|---|
| `/gerenciar_loja backup` | Exporta JSON da loja |
| `/gerenciar_loja restaurar` | Restaura o backup (valida o conteúdo contra adulteração) |

### 🎉 Sorteios `[GER. SERVIDOR]`

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/sorteio criar` | Cria sorteio no canal atual | duração: `2d` · vencedores: `1` · prêmio + opcionais (cargo e mensagens mínimas) |
| `/sorteio gerenciar` | Painel de gerência dos sorteios | encerrar, reroll ou deletar |

- Encerramento automático no horário · múltiplos vencedores · reroll substitui a lista anterior

### 👑 Comandos do dono do servidor `[DONO DO SERV]`

| Comando | O que faz | Exemplo de uso |
|---|---|---|
| `/loja vincular` | Ativa a loja grátis (plano Gratuito, sem taxa) | `/loja vincular` — só o dono do servidor consegue |
| `/loja plano` | Plano atual, uso dos limites e dívidas antigas | `/loja plano` → "3/5 produtos, 1/2 painéis" |
| `/loja mudardeplano` | Compra/renova a licença Premium (R$ 0,50/dia) | `/loja mudardeplano` → paga o PIX → destrava |

### 🤖 Comandos do dono do bot `[DONO DO BOT]`

| Comando | O que faz |
|---|---|
| `/status` | Estatísticas globais do bot |
| `/limpar_lojas_inativas` | Sincroniza e purga lojas inativas há 30+ dias |
| `/testar_bot` | Autoteste completo em ambiente isolado |
| `/botadmin gerar_cobranca_licenca` | Gera e envia cobrança de licença |
| `/botadmin addgerente` / `removegerente` | Concede/remove gerente da loja |
| `/botadmin licenca definir` / `verificar` | Define ou confere licença de um servidor |
| `/botadmin bloquear_loja` / `desbloquear_loja` | Bloqueia/desbloqueia loja manualmente |
| `/botadmin avisar_geral` | Aviso na DM dos donos de servidores/lojas (com escopo: todos/donos/logistas) |
| `/sugestao_admin bloquear` / `desbloquear` | Controla quem pode enviar sugestões |
| `/modmail_admin configurar` | Categoria dos tickets de suporte |
| `/modmail_admin bloquear` / `desbloquear` | Controla quem pode abrir tickets |
| `/revalidar notificar_todos` | DM para TODOS os membros (com confirmação e contador) |
| `/revalidar remover_cargo` | Remove um cargo de todos (com confirmação) |
| `/backup destino` / `canal` / `status` / `teste` / `resetar` | Destino do arquivamento de imagens (Site/Discord/Ambos) |

---

## ✨ Funcionalidades

### 🛒 Loja e Compras
- **Planos freemium** — grátis com limites, licença destrava (veja tabela de planos)
- **Painéis dinâmicos** com produtos, preços, estoque e emojis personalizados
- **Carrinho** com edição de quantidades, remoção e cupons
- **Pagamento via PIX** com QR Code gerado automaticamente
- **Tickets de compra** privados, com comprovante e entrega dentro do canal
- **Calculadora integrada** (R$ → Quantidade / Quantidade → R$) na tela de compra
- **Avaliação por estrelas** após entrega · **histórico** e **ranking de compradores**
- **Trocas com middleman (MM)** — convite por DM, ticket dos dois lados e **recibo anti-fraude assinado digitalmente** (`/trocar`)

### 🎟️ Cupons de Desconto
- Cupons **públicos** (código) e **de sorteio** (resgatados com mensagens)
- **Vinculação a produto**, quantidade mínima, modo "leva tudo", exibição no painel e aplicação automática
- Limite de usos e validação em tempo real (desconto só no produto vinculado)

### 🎁 Convites com Recompensa
- Modelo **1 convite = 1 ciclo**, tracking automático de quem convidou quem
- Notificação por DM ao bater a meta · resgate via ticket · cargo automático opcional
- Ranking de convidadores e recuperação do link do convite

### 🧹 Moderação e Segurança
- **Honeypot anti-hack** com ban temporário e desbanimento automático
- Log de membros (entrada, saída, kick, ban) e **transcripts HTML** dos tickets
- Verificação com **captcha por DM** · modmail · contador de mensagens
- **Sorteios** com requisito de cargo e de mensagens

### 📊 Painel de Controle
- **Dashboard fixa** persistente com botões de gestão rápida
- Gerenciamento de produtos e painéis com menus e botões
- Estatísticas de vendas, relatórios (CSV) e backup/restauração por servidor

### 🔔 Automações
- **Presença rotativa** mostrando estatísticas do bot
- Limpeza automática de lojas inativas (carência de 30 dias)
- Lembretes de licença (1, 3 e 7 dias antes) e backup automático semanal
- Sincronização de painéis ao editar produtos · verificação de integridade do banco a cada inicialização

---

## 🆘 Suporte

- **Celular ou PC**: mande uma **DM no bot** para abrir um modmail com a staff (dono de servidor/loja)
- Abra um **ticket de suporte** pelo painel
- Use `/sugestao` para enviar sugestões direto pro dono do bot

---
