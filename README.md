# 🐦 Tucano Store

Bot Discord completo para lojas virtuais com sistema de pagamentos via PIX, tickets, painéis de produtos, cupons de desconto, sistema de convites com recompensa, moderação anti-hack e muito mais.

Multi-servidor: cada servidor configura sua própria loja com produtos, preços, chave PIX, painéis e regras — de forma 100% independente.

> 💰 **Novo na v5.0: o bot agora é FREMIUM** — gratuito com limites (5 produtos e 2 painéis por servidor, vendas ilimitadas), sem taxa e sem comissão. Quer mais? A licença Premium destrava tudo.

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
- **Planos freemium** — grátis com limites, licença destrava (veja tabela acima)
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
- **Sistema de verificação** com cargo de verificado (captcha por DM)
- **Modmail** — DM direto com a staff
- **Contador de mensagens** com ranking e canais ignorados
- **Sorteios (Giveaways)** com requisitos de cargo e mensagens

### 🎫 Tickets e Suporte
- **Tickets de compra** — canal privado por pedido, com comprovante e entrega
- **Tickets de suporte** — para dúvidas e problemas
- **Tickets de recompensa** — para resgates de convite
- **Categorias configuráveis** para cada tipo de ticket
- **Transcript automático** ao fechar (com histórico completo salvo antes da exclusão)
- **Sistema de avaliação** pós-atendimento

### 📊 Painel de Controle
- **Dashboard fixo** com botões de gestão rápida
- **Gerenciamento de produtos** (adicionar, editar, excluir, ativar/desativar)
- **Gerenciamento de painéis** (criar, editar, adicionar/remover opções)
- **Estatísticas de vendas** por servidor
- **Relatórios de faturamento** (CSV)
- **Backup e restauração** de dados por servidor (restrito a administradores)

### 🔔 Automações
- **Presença rotativa** do bot (mostra estatísticas embaixo do nome)
- **Limpeza automática** de lojas inativas (com período de carência de 30 dias)
- **Lembretes de licença** expirando (1, 3 e 7 dias antes)
- **Backup automático** semanal
- **Sincronização de painéis** ao editar produtos
- **Verificação de integridade** do banco de dados a cada inicialização (com auto-reparo)

---

## 📋 Comandos Disponíveis

### 💰 Planos da Loja

| Comando | Descrição | Exemplo |
|---|---|---|
| `/loja vincular` | Ativa sua loja **de graça** (plano Gratuito, sem taxa) | `/loja vincular` |
| `/loja plano` | Mostra seu plano, uso dos limites (3/5 produtos, 1/2 painéis) e dívidas antigas | `/loja plano` |
| `/loja mudardeplano` | Compra/renova a licença Premium (R$ 0,50/dia, criação ilimitada) | `/loja mudardeplano` |

### 🛒 Loja e Compras

| Comando | Descrição | Exemplo |
|---|---|---|
| `/sacola ver` | Mostra seu carrinho com subtotal, desconto e total | `/sacola ver` |
| `/minhascompras` | Lista suas compras anteriores e status | `/minhascompras` |
| `/loja meugasto` | Mostra quanto você já gastou e o próximo cargo de recompensa | `/loja meugasto` |
| `/loja top` | Ranking dos maiores compradores do servidor | `/loja top` |
| `/minha_loja` | Hub pessoal com botões de acesso rápido (sacola, histórico, cupons, gastos) | `/minha_loja` |
| `/loja robux calcular_robux` | Calculadora de conversão R$ ↔ Robux | `/loja robux calcular_robux` |

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
5. O convite antigo é invalidado → você pode criar outro e continuar ganhando

### 🎉 Sorteios

| Comando | Descrição | Exemplo |
|---|---|---|
| `/sorteio criar` | Cria um novo sorteio (vencedores: mínimo 1) | `/sorteio criar` |
| `/sorteio gerenciar` | Gerencie sorteios ativos (encerrar, reroll, deletar) | `/sorteio gerenciar` |
| `/sorteio minhasmensagens` | Vê seu saldo de mensagens para sorteios com requisito | `/sorteio minhasmensagens` |

**Recursos dos sorteios:**
- Requisito de cargo para participar
- Requisito de mensagens (ex: mínimo de 50 mensagens)
- Múltiplos vencedores
- Encerramento automático no horário
- Reroll de vencedores (substitui a lista anterior)

### 🧹 Moderação (Honeypot)

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
5. Toda a staff é isenta do ban automático (admin, dono, gerentes da loja e bots)
6. Bans expiram automaticamente (desbanimento agendado)

### 💬 Modmail e Sugestões

| Comando | Descrição | Exemplo |
|---|---|---|
| DM direto | Mande mensagem no privado do bot → abre ticket com a staff (dono de servidor/loja) | — |
| `/sugestao` | Envia uma sugestão direto pro dono do bot | `/sugestao` |

> O modmail tem anti-spam: cooldown de 5 minutos entre tickets e fila de mensagens enquanto o canal é criado (nada se perde).

### ⚙️ Configuração do Servidor (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/configurar pix` | Configura a chave PIX do servidor (criptografada no banco) | `/configurar pix` |
| `/configurar canais` | Define canais de log, provas, carrinho, etc | `/configurar canais` |
| `/configurar verificacao definir` | Define cargo e canal de verificação (captcha) | `/configurar verificacao definir` |
| `/configurar cargo_suporte` | Adiciona cargo de suporte (vê tickets) | `/configurar cargo_suporte` |
| `/configurar recompensa` | Cargos automáticos por valor gasto | `/configurar recompensa` |
| `/configurar campo_entrega` | Personaliza a pergunta de entrega do produto | `/configurar campo_entrega` |
| `/configurar canal_ignorado` | Ignora canal no contador de mensagens | `/configurar canal_ignorar` |

### 🛍️ Gerenciamento de Produtos (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/produto adicionar` | Adiciona um produto ⚠️ *respeita o limite do plano* | `/produto adicionar` |
| `/produto editar` | Edita um produto existente | `/produto editar` |
| `/produto info` | Mostra info de um produto | `/produto info` |
| `/produto listar` | Lista todos os produtos (com menu de ações) | `/produto listar` |
| `/produto status` | Ativa/desativa um produto *(inativos não contam no limite!)* | `/produto status` |
| `/produto excluir` | Exclui um produto | `/produto excluir` |
| `/produto limiar_estoque` | Define estoque mínimo (avisa quando baixar) | `/produto limiar_estoque` |

### 🖼️ Gerenciamento de Painéis (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/painel criar` | Cria um novo painel ⚠️ *respeita o limite do plano* | `/painel criar` |
| `/painel postar` | Posta o painel em um canal | `/painel postar` |
| `/painel add_opcao` | Adiciona produto ao painel | `/painel add_opcao` |
| `/painel remover_opcao` | Remove produto do painel | `/painel remover_opcao` |
| `/painel editar` | Edita o painel (banner, cor, etc) | `/painel editar` |
| `/painel editar_opcao` | Edita uma opção do painel | `/painel editar_opcao` |
| `/painel sync` | Sincroniza o painel (atualiza preços/estoque) | `/painel sync` |
| `/painel excluir` | Exclui o painel | `/painel excluir` |

### 🎟️ Cupons (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/cupom admin_criar_publico` | Cria cupom público (código) | `/cupom admin_criar_publico` |
| `/cupom admin_criar_tipo` | Cria cupom de sorteio | `/cupom admin_criar_tipo` |
| `/cupom admin_listar` | Lista todos os cupons | `/cupom admin_listar` |
| `/cupom admin_excluir` | Exclui um cupom | `/cupom admin_excluir` |
| `/cupom admin_remover_tipo` | Desativa um cupom de sorteio | `/cupom admin_remover_tipo` |

**Parâmetros especiais ao criar cupom:**
- `produto` (opcional) — vincula o cupom a um produto específico
- `mostrar_painel` (opcional) — exibe o cupom no painel do produto
- `auto_aplicar` (opcional) — sugere o cupom ao adicionar o produto no carrinho
- `quantidade_minima` (opcional) — exige mínimo de unidades (use `-1` para "leva tudo")

### 🎁 Convites (Admin)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/convite admin_configurar` | Configura o sistema de convites | `/convite admin_configurar` |
| `/convite admin_desativar` | Desativa o sistema de convites | `/convite admin_desativar` |

### 🧹 Ações em Massa (apenas dono do bot)

| Comando | Descrição | Exemplo |
|---|---|---|
| `/revalidar notificar_todos` | Envia DM para todos os membros (com confirmação) | `/revalidar notificar_todos` |
| `/revalidar remover_cargo` | Remove um cargo de todos os membros (com confirmação) | `/revalidar remover_cargo` |

---

## ⚙️ Configuração Inicial (Após adicionar o bot)

1. **Ative sua loja grátis**: `/loja vincular` — sem custo, sem comissão
2. **Configure o PIX**: `/configurar pix` — defina a chave PIX do seu servidor
3. **Configure os canais**: `/configurar canais` — log, provas, carrinho, etc
4. **Adicione produtos**: `/produto adicionar` — até 5 no plano grátis
5. **Crie um painel**: `/painel criar` → `/painel add_opcao` → `/painel postar`
6. **Configure a categoria de tickets**: `/configurar canais`
7. **(Opcional) Ative o honeypot**: crie um canal privado → `/honeypot ativar`
8. **(Opcional) Configure convites**: `/convite admin_configurar`
9. **Precisa de mais espaço?** `/loja mudardeplano` — licença Premium

---

## 🔒 Recursos de Segurança

- **Criptografia** de dados sensíveis (chaves PIX) com Fernet (AES-128-CBC + HMAC-SHA256)
- **Whitelists de colunas** contra SQL Injection nos UPDATEs dinâmicos
- **Sistema anti-bypass**: lojas inativas têm dados preservados por 30 dias (evita kick+re-convite pra burlar carência)
- **Validação atômica** de estoque (sem oversell, mesmo com cliques simultâneos)
- **Proteção anti-corrida** em ações financeiras: confirmar pagamento, cancelar, aprovar licença e resgatar recompensas não sofrem duplicação com cliques duplos
- **Notificação automática de erros** pro dono do bot via DM (com cooldown anti-spam, rate limit e **ocultação automática de tokens e chaves**)
- **Backup/restauração restritos a administradores** — com validação de conteúdo (rejeita backups adulterados)
- **Honeypot** com isenção completa da staff (não bane admin, dono nem gerentes)
- **Bans temporários** com desbanimento automático
- **Auto-reparo do banco**: integridade verificada a cada inicialização, com correção automática de referências quebradas e limpeza de registros órfãos

---

## 🛠️ Stack Técnico

- **Linguagem**: Python 3.10+
- **Framework**: discord.py 2.x
- **Banco de dados**: SQLite (migrações versionadas v1→v27, idempotentes, com auto-reparo)
- **Criptografia**: cryptography (Fernet)
- **QR Code PIX**: pixqrcodegen + qrcode
- **Timezone**: pytz (America/Sao_Paulo)
- **Qualidade**: 168 testes automatizados (8 suítes) rodando em ambiente isolado

---

## 📊 Arquitetura

```
botvenda/
├── bot.py                  # Entry point, carrega cogs, handlers globais
├── config.py               # Configurações (IDs, cores, limites do plano grátis)
├── crypto.py               # Criptografia Fernet (chaves PIX)
├── database.py             # SQLite + migrações v1-v27 (auto-reparo) + CRUD
├── ui_components.py        # Views, Modals, Selects (Discord UI)
├── CHANGELOG.md            # Histórico completo de versões
├── DESENVOLVIMENTO.md      # Guia técnico (deploy, env, testes)
├── cogs/
│   ├── events.py           # on_member_join/leave/guild_remove/join
│   ├── store.py            # Loja, carrinho, tickets de compra, checkout PIX
│   ├── admin.py            # Dashboard, produtos, painéis, backup
│   ├── billing_cog.py      # Planos (freemium), licenças, faturamento legado
│   ├── coupon_cog.py       # Cupons (públicos + sorteio + vinculados a produto)
│   ├── invite_cog.py       # Sistema de convites com recompensa (1-ciclo)
│   ├── honeypot_cog.py     # Armadilha anti-hack com ban temporário
│   ├── giveaway_cog.py     # Sorteios com requisitos
│   ├── verification_cog.py # Verificação de membros (captcha por DM)
│   ├── modmail_cog.py      # Modmail (DM com staff)
│   ├── logger_cog.py       # Log de mensagens deletadas
│   ├── mass_actions.py     # Ações em massa (DM, cargos)
│   ├── message_counter_cog.py # Contador de mensagens
│   ├── permissions_cog.py  # /botadmin: licenças, gerentes, bloqueios
│   ├── status_cog.py       # Presença rotativa + status global + limpeza
│   ├── tasks.py            # Tasks agendadas (lembretes, backup)
│   ├── utility_cog.py      # Sugestões
│   ├── config_cog.py       # /configurar (canais, pix, cargos)
│   └── test_bot_cog.py     # Autoteste (apenas ambiente de testes)
├── utils/
│   ├── bot_utils.py        # Permissões UNIFICADAS + CogBase + helpers
│   ├── error_notifier.py   # Notificação de erros (cooldown + rate limit + redação)
│   └── transcript.py       # Geração de transcripts HTML
└── tests/                  # 8 suítes de testes automatizados (168 verificações)
```

---

## 📈 Recursos Avançados

- **Multi-servidor**: cada servidor tem configuração isolada
- **Modelo freemium**: plano grátis com limites de criação; licença Premium ilimitada — sem comissão sobre vendas
- **Presença rotativa**: mostra servidores, membros, vendas totais, receita (com cache de performance)
- **Backup automático** semanal (domingo às 03:00 UTC)
- **Sincronização de painéis**: ao editar produto, painéis atualizam automaticamente
- **Calculadora de compra**: R$ → Qtd / Qtd → R$ integrada ao fluxo
- **Anti-bypass de taxa**: dados financeiros preservados ao kick+re-convite (carência de 30 dias)
- **Integridade do banco**: verificação + auto-reparo na inicialização (FKs, órfãos, índices)
- **Performance**: índices de consulta, cache de estatísticas, operações de banco fora da thread principal

---

## 🆘 Suporte

- Use `/sugestao` pra enviar sugestões direto pro dono
- Mande DM pro bot pra abrir um modmail com a staff (dono de servidor/loja)
- Abra um ticket de suporte pelo painel

---

## 📝 Licença

Uso pessoal. Entre em contato com o dono do bot para uso comercial.

---

## 📜 Changelog

Histórico completo de versões (v1.1 até a v5.0): veja [CHANGELOG.md](CHANGELOG.md).
