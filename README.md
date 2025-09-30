# 🤖 Guia de Comandos - TuCaNo Store Bot

# Para suporte contate: tucaca_1_40280 no Discord

Bem-vindo ao guia completo de comandos para o seu bot de loja!  
Este documento foi feito para ajudar os donos de servidor a configurar e gerenciar suas lojas de forma rápida e fácil.

---

## ➕ Adicione o Bot ao seu Servidor
Para começar, adicione o TuCaNo Store Bot ao seu servidor clicando no link abaixo:

[**Clique aqui para convidar o Bot**](https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot)

---

## 🚀 Primeiros Passos e Configuração Essencial

### 1. Ative a Loja no seu Servidor
Este é o primeiro e mais importante comando! Ele ativa o bot no seu servidor, vinculando a sua conta de dono para o faturamento.

- **`/loja vincular`**

### 2. Configure os Canais
Defina onde cada ação do bot irá acontecer.

- **`/configurar canais`**
  - > **`categoria_tickets`**: Onde os carrinhos de compra serão criados.  
  - > **`categoria_suporte`**: Para tickets de suporte geral.  
  - > **`canal_provas`**: Canal onde as provas de entrega são postadas.  
  - > **`canal_avaliacoes`**: Onde as avaliações dos clientes aparecem.  
  - > **`canal_logs`**: **(MUITO IMPORTANTE)** Canal privado com históricos e backups.  
  - > **`canal_comandos_sacola`**: *[Opcional]* Canal dedicado para `/sacola`.  

### 3. Configure o PIX
Para receber pagamentos:

- **`/configurar pix`**
  - > **Chave PIX**: e-mail, telefone, CPF/CNPJ ou chave aleatória.  
  - > **Nome do Beneficiário**: Como aparece no PIX.  
  - > **Cidade**: Cidade vinculada à chave PIX.  

### 4. Personalize o Campo de Entrega
Por padrão, o bot pede "Nick do Roblox".  
Personalize para qualquer jogo/serviço!

- **`/configurar campo_entrega`**
  - > **Exemplo:** "Qual seu Riot ID?", "Qual seu nick no Minecraft?", "Qual seu @ no Instagram?".  
  - > Use `PADRAO` para voltar ao padrão.  

---

## 🕹️ Comandos de Hub e Painéis Interativos

### 🎛️ Dashboard de Administração
Painel fixo e persistente para gerenciar a loja.

- **`/gerenciar_loja dashboard_fixo`**
  - Posta um painel permanente em um canal privado.  
  - Sobrevive a reinicializações do bot.  
  - Botões levam a menus efêmeros (mantém o canal limpo).  

### 🧾 Hub do Cliente
Um único comando para tudo que o cliente precisa.

- **`/minha_loja`**
  - 🛒 Ver Sacola  
  - 📜 Histórico de compras  
  - 💸 Gasto total + progresso para próxima recompensa  
  - 🎟️ Cupons disponíveis  

---

## 🛠️ Gerenciamento da Loja (Admins e Gerentes)

### 📦 Produtos (`/produto`)
- **`/produto adicionar`** → adiciona novo produto.  
- **`/produto listar`** → exibe todos os produtos em menu suspenso com botões [✏️ Editar] e [🗑️ Excluir].  
- **`/produto editar`** → edita produto existente.  
- **`/produto excluir`** → remove produto.  
- **`/produto status`** → ativa/desativa produto.  
- **`/produto info`** → detalhes completos.  
- **`/produto limiar_estoque`** → alerta de estoque baixo.  

### 🖼️ Painéis (`/painel`)
- **`/painel criar`** → cria novo painel de vendas.  
- **`/painel editar`** → edita título, descrição, imagens ou cor.  
- **`/painel excluir`** → apaga painel.  
- **`/painel add_opcao`** → adiciona produto ao painel.  
- **`/painel remover_opcao`** → remove produto do painel.  
- **`/painel sync`** → atualiza o painel.  

### 🕹️ Administração Geral (`/gerenciar_loja`)
- **`/gerenciar_loja painel_controle`** → painel interativo para produtos e painéis.  
- **`/gerenciar_loja estatisticas`** → resumo de vendas e top clientes.  
- **`/gerenciar_loja relatorio`** → exporta relatório `.csv`.  
- **`/gerenciar_loja diagnostico`** → checa se a configuração está correta.  
- **`/gerenciar_loja backup`** → gera backup da loja.  
- **`/gerenciar_loja restaurar`** → restaura a loja de um backup.  

### ⚙️ Configurações Avançadas (`/configurar`)
- **`/configurar recompensa adicionar`** → define cargo automático por gasto total.  
- **`/configurar recompensa listar`** → lista recompensas.  
- **`/configurar cargo_suporte adicionar`** → dá acesso a tickets.  
- **`/configurar canal_ignorado adicionar`** → ignora mensagens de um canal para sorteios.  

### 🎉 Sorteios (`/sorteio`)
- **`/sorteio criar`** → inicia sorteio.  
- **`/sorteio gerenciar`** → painel para rerolar, cancelar, finalizar.  

### 🎟️ Cupons (`/cupom admin`)
- **`/cupom admin_criar_tipo`** → cria cupom resgatável em sorteio.  
- **`/cupom admin_criar_publico`** → cria código de desconto aberto.  
- **`/cupom admin_listar`** → lista cupons criados.  
- **`/cupom admin_excluir`** → apaga cupom.  

### ✅ Sistema de Verificação (`/verificacao`)
- **`/configurar verificacao definir`** → define canal/cargo para verificação.  
- **`/verificacao postar_painel`** → posta painel de verificação.  

### 📢 Ações em Massa (`/revalidar`)
- **`/revalidar remover_cargo`** → remove cargo de todos.  
- **`/revalidar notificar_todos`** → DM para todos os membros.  

---

## 🙋 Comandos para Clientes

- **Interagir com Painéis** → principal forma de compra.  
- **`/sacola ver`** → mostra sacola, permite editar/remover/aplicar cupom.  
- **`/minhascompras`** → últimas 10 compras.  
- **`/loja top`** → ranking dos maiores clientes.  
- **`/loja meugasto`** → gasto total + próxima recompensa.  
- **`/loja plano`** → plano atual (comissão ou assinatura).  
- **`/loja mudardeplano`** → troca plano para assinatura.  
- **`/loja robux calcular_robux`** → calcula Robux com e sem taxa 30%.  
- **`/cupom resgatar`** → tenta ganhar cupom de desconto.  
- **`/cupom meuscupons`** → lista cupons do cliente.  
- **`/sorteio minhasmensagens`** → saldo de mensagens para sorteios.  
