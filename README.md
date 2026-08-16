# 🐦 Tucano Store

Bot Discord completo para lojas virtuais com sistema de pagamentos via PIX, tickets, painéis de produtos, cupons de desconto, sistema de convites com recompensa, moderação anti-hack e muito mais.

Multi-servidor: cada servidor configura sua própria loja com produtos, preços, chave PIX, painéis e regras — de forma 100% independente.

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

## ✨ Funcionalidades

### 🛒 Loja e Compras
- **Painéis dinâmicos** com produtos, preços, estoque e emojis personalizados
- **Sistema de carrinho** com edição de quantidades e remoção de itens
- **Pagamento via PIX** com QR Code gerado automaticamente
- **Tickets de compra** privados para cada pedido
- **Submissão de comprovante** dentro do ticket
- **Avaliação por estrelas** após entrega
- **Calculadora integrada** (R$ → Quantidade / Quantidade → R$) na tela de compra
- **Histórico de compras** por usuário
- **Controle de gasto** por usuário
- **Ranking de maiores compradores**

### 🎟️ Cupons de Desconto
- **Cupons públicos** (código digitável) e **cupons de sorteio** (resgatados com mensagens)
- **Vinculação a produto específico** — funciona só para o produto escolhido
- **Quantidade mínima** para ativar o cupom
- **Modo "leva tudo"** — exige comprar todo o estoque atual do produto
- **Exibição no painel** — mostra o cupom disponível abaixo do produto
- **Aplicação automática** — sugere o cupom ao adicionar o produto no carrinho
- **Limite de usos** por cupom (ou ilimitado)
- **Validação em tempo real** — desconto só sobre o produto vinculado

### 🎁 Sistema de Convites com Recompensa
- **1 convite por vez** por usuário (modelo 1-ciclo)
- **Tracking automático** — detecta quem convidou quem (via snapshot de invites)
- **Notificação por DM** ao bater a meta
- **Resgate via ticket** — abre um canal privado com a staff
- **Cargo automático** ao resgatar (opcional)
- **Ranking de convidadores** do servidor
- **Recuperação de convite** — comando pra ver o link se perder

### 🧹 Moderação e Segurança
- **Honeypot anti-hack** — canal armadilha que bane automaticamente quem envia mensagem
- **Ban temporário** com desbanimento automático após X dias
- **Log de membros** — entrada, saída, kick, ban
- **Transcripts HTML** de tickets encerrados
- **Sistema de verificação** com cargo de verificado
- **Modmail** — DM direto com a staff
- **Contador de mensagens** com ranking e canais ignorados
- **Sorteios (Giveaways)** com requisitos de cargo e mensagens

### 🎫 Tickets e Suporte
- **Tickets de compra** — canal privado por pedido, com comprovante e entrega
- **Tickets de suporte** — para dúvidas e problemas
- **Categorias configuráveis** para cada tipo de ticket
- **Transcript automático** ao fechar
- **Sistema de avaliação** pós-atendimento

### 📊 Painel de Controle
- **Dashboard fixo** com botões de gestão rápida
- **Gerenciamento de produtos** (adicionar, editar, excluir, ativar/desativar)
- **Gerenciamento de painéis** (criar, editar, adicionar/remover opções)
- **Estatísticas de vendas** por servidor
- **Relatórios de faturamento**
- **Backup e restauração** de dados por servidor

### 🔔 Automações
- **Presença rotativa** do bot (mostra estatísticas embaixo do nome)
- **Limpeza automática** de lojas inativas (com período de carência)
- **Lembretes de licença** expirando
- **Backup automático** semanal
- **Sincronização de painéis** ao editar produtos

---

## 📋 Comandos Disponíveis

### 🛒 Loja e Compras

| Comando | Descrição | Exemplo |
|---|---|---|
| `/sacola ver` | Mostra seu carrinho de compras com subtotal, desconto e total | `/sacola ver` |
| `/sacola historico` | Lista suas compras anteriores e status | `/sacola historico` |
| `/sacola gasto` | Mostra quanto você já gastou no servidor | `/sacola gasto` |
| `/loja top_gastadores` | Ranking dos maiores compradores do servidor | `/loja top_gastadores` |
| `/loja meu_hub` | Hub pessoal com botões de acesso rápido | `/loja meu_hub` |

**Fluxo de compra:**
1. Abra o painel da loja no canal de compras
2. Selecione um produto no menu suspenso
3. Veja as opções: **Comprar**, **Calcular R$→Qtd**, **Calcular Qtd→R$**
4. Use a calculadora pra saber o valor antes de comprar
5. Confirme a quantidade → item vai pro carrinho
6. Use `/sacola ver` → aplique cupons → clique em **Finalizar Compra**
7. Um ticket privado é aberto com o QR Code PIX
8. Envie o comprovante no ticket → staff confirma → entrega

### 🎟️ Cupons

| Comando | Descrição | Exemplo |
|---|---|---|
| `/cupom resgatar` | Gastar mensagens para tentar a sorte e ganhar um cupom | `/cupom resgatar` |
| `/cupom meuscupons` | Lista seus cupons disponíveis | `/cupom meuscupons` |

**Como aplicar cupom na sacola:**
- **Cupom de inventário**: selecione no menu suspenso da sacola
- **Cupom público (código)**: clique em "🏷️ Aplicar Código" e digite o código

**Exemplos de cupons que admins podem criar:**
- `NATAL10` — 10% OFF em qualquer produto (global)
- `MUSH10` — 10% OFF só no produto "Mush" (vinculado)
- `BULK10` — 10% OFF exigindo mínimo de 5000 unidades de Mush
- `LEVATUDO` — 20% OFF exigindo comprar TODO o estoque atual de Mush

### 🎁 Convites com Recompensa

| Comando | Descrição | Exemplo |
|---|---|---|
| `/convite criar` | Gera um link de convite personalizado | `/convite criar` |
| `/convite meu_convite` | Mostra o link do seu convite ativo (se perdeu) | `/convite meu_convite` |
| `/convite status` | Mostra seu progresso de convites no ciclo atual | `/convite status` |
| `/convite resgatar` | Abre um ticket para receber sua recompensa | `/convite resgatar` |
| `/convite ranking` | Top 10 convidadores do servidor | `/convite ranking` |

**Fluxo do sistema de convites:**
1. Use `/convite criar` → recebe um link personalizado
2. Compartilhe com amigos → quando alguém entra pelo link, +1 no seu contador
3. Ao bater a meta (ex: 5 convites), recebe uma DM avisando
4. Use `/convite resgatar` → abre ticket com a staff + recebe o prêmio
5. O convite antigo é deletado → você pode criar outro e continuar ganhando

### 🎫 Tickets

| Comando | Descrição | Exemplo |
|---|---|---|
| `/ticket fechar` | Fecha o ticket atual (gera transcript) | `/ticket fechar` |

**Tickets são abertos automaticamente:**
- Ao finalizar uma compra (ticket de compra)
- Ao clicar em "Suporte" no painel (ticket de suporte)
- Ao resgatar recompensa de convites (ticket de recompensa)

### 🧹 Moderação

| Comando | Descrição | Exemplo |
|---|---|---|
| `/honeypot ativar` | Ativa o honeypot no canal atual (qualquer msg = ban) | `/honeypot ativar` |
| `/honeypot desativar` | Desativa o honeypot do servidor | `/honeypot desativar` |
| `/honeypot status` | Mostra estado do honeypot e bans ativos | `/honeypot status` |
| `/honeypot desbanir` | Remove o ban honeypot de um usuário manualmente | `/honeypot desbanir @user` |

**Como funciona o honeypot:**
1. Crie um canal privado (ex: `#🪤-armadilha`)
2. Use `/honeypot ativar` nele
3. O bot posta uma mensagem fixada avisando que é proibido enviar mensagens
4. Se alguém enviar → mensagem é deletada + usuário banido por X dias
5. Staff (admin+) é isento do ban automático
6. Bans expiram automaticamente

### 🎉 Sorteios (Giveaways)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/sorteio criar` | Cria um novo sorteio | `/sorteio criar prêmio:"100 Robux" dias:7 vencedores:1` |
| `/sorteio gerenciar` | Gerencie sorteios ativos (encerrar, reroll, deletar) | `/sorteio gerenciar` |

**Recursos dos sorteios:**
- Requisito de cargo para participar
- Requisito de mensagens (ex: mínimo de 50 mensagens)
- Múltiplos vencedores
- Encerramento automático no horário
- Reroll de vencedores

### 💬 Modmail

| Comando | Descrição | Exemplo |
|---|---|---|
| `/modmail` | Abre uma conversa privada com a staff via DM | `/modmail` |

### 💡 Sugestões

| Comando | Descrição | Exemplo |
|---|---|---|
| `/sugestao` | Envia uma sugestão direto pro dono do bot | `/sugestao mensagem:"Adicionar PayPal"` |

### ⚙️ Configuração do Servidor (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/configurar pix` | Configura a chave PIX do servidor | `/configurar pix chave:"email@x.com" nome:"Loja" cidade:"SAO PAULO"` |
| `/configurar canais` | Define canais de log, provas, carrinho, etc | `/configurar canais log:#logs prova:#provas` |
| `/configurar cargo_verificado` | Define cargo de verificação | `/configurar cargo_verificado @Verificado` |
| `/configurar cargo_suporte` | Adiciona cargo de suporte (vê tickets) | `/configurar cargo_suporte @Staff` |
| `/configurar ignorar_canal` | Ignora canal no contador de mensagens | `/configurar ignorar_canal #bot-spam` |

### 🛍️ Gerenciamento de Produtos (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/produto add` | Adiciona um produto | `/produto add nome:"Mush" tipo:MOEDA modelo:MILHAR preco:0.18 estoque:100000 emoji:🍄` |
| `/produto editar` | Edita um produto existente | `/produto editar produto:"Mush" novo_preco:0.15` |
| `/produto info` | Mostra info de um produto | `/produto info produto:"Mush"` |
| `/produto listar` | Lista todos os produtos | `/produto listar` |
| `/produto status` | Ativa/desativa um produto | `/produto status produto:"Mush"` |
| `/produto excluir` | Exclui um produto | `/produto excluir produto:"Mush"` |
| `/produto limiar` | Define estoque mínimo (avisa quando baixar) | `/produto limiar produto:"Mush" limiar:1000` |

### 🖼️ Gerenciamento de Painéis (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/painel criar` | Cria um novo painel | `/painel criar titulo:"🛒 Loja" descricao:"Compre aqui!"` |
| `/painel postar` | Posta o painel em um canal | `/painel postar painel:"loja" canal:#loja` |
| `/painel add_opcao` | Adiciona produto ao painel | `/painel add_opcao painel:"loja" produto:"Mush" emoji:🍄` |
| `/painel remover_opcao` | Remove produto do painel | `/painel remover_opcao painel:"loja" opcao:"..."` |
| `/painel editar` | Edita o painel (banner, cor, etc) | `/painel editar painel:"loja" banner:"https://..."` |
| `/painel sync` | Sincroniza o painel (atualiza preços) | `/painel sync painel:"loja"` |
| `/painel excluir` | Exclui o painel | `/painel excluir painel:"loja"` |

### 🎟️ Cupons (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/cupom admin_criar_publico` | Cria cupom público (código) | `/cupom admin_criar_publico codigo:"NATAL10" valor:10 usos:100 produto:"Mush" mostrar_painel:True` |
| `/cupom admin_criar_tipo` | Cria cupom de sorteio | `/cupom admin_criar_tipo nome:"Cupom 5%" valor:5 peso:10` |
| `/cupom admin_listar` | Lista todos os cupons | `/cupom admin_listar` |
| `/cupom admin_excluir` | Exclui um cupom | `/cupom admin_excluir cupom:"NATAL10"` |
| `/cupom admin_remover_tipo` | Desativa um cupom de sorteio | `/cupom admin_remover_tipo cupom:"..."` |

**Parâmetros especiais ao criar cupom:**
- `produto` (opcional) — vincula o cupom a um produto específico
- `mostrar_painel` (opcional) — exibe o cupom no painel do produto
- `auto_aplicar` (opcional) — sugere o cupom ao adicionar o produto no carrinho
- `quantidade_minima` (opcional) — exige mínimo de unidades (use `-1` para "leva tudo")

### 🎁 Convites (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/convite admin_configurar` | Configura o sistema de convites | `/convite admin_configurar threshold:5 recompensa:"50 Robux + VIP" cargo:@VIP categoria:#tickets` |
| `/convite admin_desativar` | Desativa o sistema de convites | `/convite admin_desativar` |

### 🧹 Moderação em Massa (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/moderacao notificar_todos` | Envia DM para todos os membros | `/moderacao notificar_todos mensagem:"..."` |
| `/moderacao adicionar_cargo` | Adiciona cargo a todos | `/moderacao adicionar_cargo cargo:@Membro` |
| `/moderacao remover_cargo` | Remove cargo de todos | `/moderacao remover_cargo cargo:@Antigo` |

---

## ⚙️ Configuração Inicial (Após adicionar o bot)

1. **Configure o PIX**: `/configurar pix` — defina a chave PIX do seu servidor
2. **Configure os canais**: `/configurar canais` — log, provas, carrinho, etc
3. **Adicione produtos**: `/produto add` — crie seus produtos
4. **Crie um painel**: `/painel criar` → `/painel add_opcao` → `/painel postar`
5. **Configure a categoria de tickets**: `/configurar canais`
6. **(Opcional) Ative o honeypot**: crie um canal privado → `/honeypot ativar`
7. **(Opcional) Configure convites**: `/convite admin_configurar`

---

## 🔒 Recursos de Segurança

- **Criptografia** de dados sensíveis (chaves PIX) com Fernet (AES-128-CBC + HMAC-SHA256)
- **Whitelists de colunas** contra SQL Injection nos UPDATEs dinâmicos
- **Sistema anti-bypass**: lojas inativas têm dados preservados por 30 dias (evita kick+re-convite pra resetar período de teste)
- **Validação atômica** de estoque (sem oversell)
- **Notificação automática de erros** pro dono do bot via DM (com cooldown anti-spam)
- **Honeypot** com isenção de staff (não bane admin/owner)
- **Bans temporários** com desbanimento automático

---

## 🛠️ Stack Técnico

- **Linguagem**: Python 3.10+
- **Framework**: discord.py
- **Banco de dados**: SQLite (com migrações versionadas)
- **Criptografia**: cryptography (Fernet)
- **QR Code PIX**: pixqrcodegen + qrcode
- **Timezone**: pytz (America/Sao_Paulo)

---

## 📊 Arquitetura

```
botvenda/
├── bot.py                  # Entry point, carrega cogs, handlers globais
├── config.py               # Configurações (IDs, cores, taxas)
├── crypto.py              # Criptografia Fernet
├── database.py            # SQLite + migrações v1-v24 + CRUD
├── ui_components.py       # Views, Modals, Selects (Discord UI)
├── cogs/
│   ├── events.py          # on_member_join/leave/guild_remove/join
│   ├── store.py           # Loja, carrinho, tickets de compra, checkout PIX
│   ├── admin.py           # Dashboard, produtos, painéis, backup
│   ├── billing_cog.py    # Comissão, licenças, faturamento
│   ├── coupon_cog.py     # Cupons (públicos + sorteio + vinculados a produto)
│   ├── invite_cog.py     # Sistema de convites com recompensa (1-ciclo)
│   ├── honeypot_cog.py   # Armadilha anti-hack com ban temporário
│   ├── giveaway_cog.py    # Sorteios com requisitos
│   ├── verification_cog.py # Verificação de membros
│   ├── modmail_cog.py     # Modmail (DM com staff)
│   ├── logger_cog.py      # Log de mensagens deletadas
│   ├── mass_actions.py    # Ações em massa (DM, cargos)
│   ├── message_counter_cog.py # Contador de mensagens
│   ├── permissions_cog.py  # Permissões e licenças
│   ├── status_cog.py     # Presença rotativa + status global + limpeza
│   ├── tasks.py           # Tasks agendadas (lembretes, backup)
│   ├── utility_cog.py    # Sugestões
│   └── test_bot_cog.py   # Autoteste
└── utils/
    ├── bot_utils.py        # CogBase com error handler + notificação DM
    ├── error_notifier.py   # Notificação de erros pro dono (cooldown + rate limit)
    └── transcript.py      # Geração de transcripts HTML
```

---

## 📈 Recursos Avançados

- **Multi-servidor**: cada servidor tem configuração isolada
- **Presença rotativa**: mostra servidores, membros, vendas totais, receita
- **Backup automático** semanal (domingo às 03:00 UTC)
- **Sincronização de painéis**: ao editar produto, painéis atualizam automaticamente
- **Calculadora de compra**: R$ → Qtd / Qtd → R$ integrada ao fluxo
- **Período de teste** de 24h pra novas lojas (comissão isenta)
- **Sistema de comissão** automático com faturamento cíclico
- **Anti-bypass de taxa**: dados financeiros preservados ao kick+re-convite

---

## 🆘 Suporte

- Use `/sugestao` pra enviar sugestões direto pro dono
- Use `/modmail` pra falar com a staff do servidor
- Abra um ticket de suporte pelo painel

---

## 📝 Licença

Uso pessoal. Entre em contato com o dono do bot para uso comercial.
