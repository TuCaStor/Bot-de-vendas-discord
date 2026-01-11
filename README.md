# 🤖 Guia de Comandos - TuCaNo Store Bot

## Para suporte contate: `moshiini_` no Discord ou entre nesse sv `https://discord.gg/rPFqpK2gqX`

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

-   **`/loja vincular`**
    -   > **Exemplo:** `/loja vincular`

### 2. Configure os Canais
Defina onde cada ação do bot irá acontecer.

-   **`/configurar canais`**
    -   > **Exemplo:** `/configurar canais categoria_tickets:#tickets-compras canal_logs:#bot-logs canal_provas:#entregas`
    -   > **`categoria_tickets`**: Onde os carrinhos de compra serão criados.
    -   > **`categoria_suporte`**: Para tickets de suporte geral.
    -   > **`canal_provas`**: Canal onde as provas de entrega são postadas.
    -   > **`canal_avaliacoes`**: Onde as avaliações dos clientes aparecem.
    -   > **`canal_logs`**: **(MUITO IMPORTANTE)** Canal privado com históricos e backups.
    -   > **`canal_comandos_sacola`**: *[Opcional]* Canal dedicado para `/sacola`.

### 3. Configure o PIX
Para receber pagamentos. O comando abrirá um formulário.

-   **`/configurar pix`**
    -   > **Exemplo:** `/configurar pix`
    -   > **Chave PIX**: seu.email@exemplo.com
    -   > **Nome do Beneficiário**: João da Silva
    -   > **Cidade**: SAO PAULO

### 4. Personalize o Campo de Entrega
Por padrão, o bot pede "Nick do Roblox". Personalize para qualquer jogo/serviço!

-   **`/configurar campo_entrega`**
    -   > **Exemplo:** `/configurar campo_entrega texto_do_campo:Qual seu Riot ID (Ex: Nick#BR1)?`
    -   > Use `PADRAO` para voltar ao padrão.

---

## 🕹️ Comandos de Hub e Painéis Interativos

### 🎛️ Dashboard de Administração
Painel fixo e persistente para gerenciar a loja.

-   **`/gerenciar_loja dashboard_fixo`**
    -   > **Exemplo:** `/gerenciar_loja dashboard_fixo canal:#painel-admin`
    -   > Posta um painel permanente em um canal privado que sobrevive a reinicializações do bot.

### 🧾 Hub do Cliente
Um único comando para tudo que o cliente precisa.

-   **`/minha_loja`**
    -   > **Exemplo:** `/minha_loja`
    -   > Abre um painel pessoal com botões para:
    -   > 🛒 Ver Sacola
    -   > 📜 Histórico de compras
    -   > 💸 Gasto total + progresso para próxima recompensa
    -   > 🎟️ Cupons disponíveis

---

## 🛠️ Gerenciamento da Loja (Admins e Gerentes)

### 📦 Produtos (`/produto`)
-   **`/produto adicionar`**
    -   > **Exemplo:** `/produto adicionar nome_exibicao:1000 Gemas tipo_produto:Moeda modelo_preco:Preço por Milhar valor_preco:5.50 estoque:-1`
-   **`/produto listar`**
    -   > **Exemplo:** `/produto listar` (Abre um menu suspenso com botões [✏️ Editar] e [🗑️ Excluir]).
-   **`/produto editar`**
    -   > **Exemplo:** `/produto editar produto:1000 Gemas novo_valor_preco:6.00 novo_estoque:50000`
-   **`/produto excluir`**
    -   > **Exemplo:** `/produto excluir produto:1000 Gemas`
-   **`/produto status`**
    -   > **Exemplo:** `/produto status produto:1000 Gemas status:Desativar`
-   **`/produto info`**
    -   > **Exemplo:** `/produto info produto:1000 Gemas`
-   **`/produto limiar_estoque`**
    -   > **Exemplo:** `/produto limiar_estoque produto:Poção de Cura limite:10`

### 🖼️ Painéis (`/painel`)
-   **`/painel criar`**
    -   > **Exemplo:** `/painel criar canal:#loja-principal id_painel:loja_principal titulo:✨ Loja Principal ✨ descricao:Bem-vindo! Selecione um item abaixo.`
-   **`/painel editar`**
    -   > **Exemplo:** `/painel editar id_painel:loja_principal nova_descricao:Promoção de Fim de Semana! Aproveite!`
-   **`/painel excluir`**
    -   > **Exemplo:** `/painel excluir id_painel:loja_principal`
-   **`/painel add_opcao`**
    -   > **Exemplo:** `/painel add_opcao id_painel:loja_principal produto:1000 Gemas label:💎 Comprar 1000 Gemas`
-   **`/painel remover_opcao`**
    -   > **Exemplo:** `/painel remover_opcao id_painel:loja_principal opcao:💎 Comprar 1000 Gemas`
-   **`/painel sync`**
    -   > **Exemplo:** `/painel sync id_painel:loja_principal` (Força a atualização visual do painel).

### 🕹️ Administração Geral (`/gerenciar_loja`)
-   **`/gerenciar_loja painel_controle`**
    -   > **Exemplo:** `/gerenciar_loja painel_controle` (Abre um painel interativo efêmero).
-   **`/gerenciar_loja estatisticas`**
    -   > **Exemplo:** `/gerenciar_loja estatisticas`
-   **`/gerenciar_loja relatorio`**
    -   > **Exemplo:** `/gerenciar_loja relatorio periodo:Últimos 7 dias`
-   **`/gerenciar_loja diagnostico`**
    -   > **Exemplo:** `/gerenciar_loja diagnostico`
-   **`/gerenciar_loja backup`**
    -   > **Exemplo:** `/gerenciar_loja backup` (Envia o arquivo de backup para sua DM).
-   **`/gerenciar_loja restaurar`**
    -   > **Exemplo:** `/gerenciar_loja restaurar arquivo_backup:[Anexe o arquivo .json aqui]`

### ⚙️ Configurações Avançadas (`/configurar`)
-   **`/configurar recompensa adicionar`**
    -   > **Exemplo:** `/configurar recompensa adicionar cargo:@Cliente VIP valor:100`
-   **`/configurar recompensa listar`**
    -   > **Exemplo:** `/configurar recompensa listar`
-   **`/configurar cargo_suporte adicionar`**
    -   > **Exemplo:** `/configurar cargo_suporte adicionar cargo:@Equipe da Loja`
-   **`/configurar canal_ignorado adicionar`**
    -   > **Exemplo:** `/configurar canal_ignorado adicionar canal:#bate-papo`

### 🎉 Sorteios (`/sorteio`)
-   **`/sorteio criar`**
    -   > **Exemplo:** `/sorteio criar duracao:3d premio:1 Mês de Nitro Basic vencedores:2 cargo_req:@Membro Ativo`
-   **`/sorteio gerenciar`**
    -   > **Exemplo:** `/sorteio gerenciar` (Abre um menu para gerenciar sorteios ativos e finalizados).

### 🎟️ Cupons (`/cupom admin`)
-   **`/cupom admin_criar_tipo`**
    -   > **Exemplo:** `/cupom admin_criar_tipo nome:Cupom Raro de 15% valor_desconto:15 peso_raridade:5`
-   **`/cupom admin_criar_publico`**
    -   > **Exemplo:** `/cupom admin_criar_publico codigo:BEMVINDO10 valor_desconto:10 usos_maximos:100`
-   **`/cupom admin_listar`**
    -   > **Exemplo:** `/cupom admin_listar`
-   **`/cupom admin_excluir`**
    -   > **Exemplo:** `/cupom admin_excluir cupom:Código 10% OFF - BEMVINDO10`

### ✅ Sistema de Verificação (`/verificacao`)
-   **`/configurar verificacao definir`**
    -   > **Exemplo:** `/configurar verificacao definir canal:#verifique-se cargo_verificado:@Membro Verificado`
-   **`/verificacao postar_painel`**
    -   > **Exemplo:** `/verificacao postar_painel titulo:✅ Verificação Obrigatória descricao:Para acessar o servidor, clique no botão abaixo e siga as instruções na sua DM.`

### 📢 Ações em Massa (`/revalidar`)
-   **`/revalidar remover_cargo`**
    -   > **Exemplo:** `/revalidar remover_cargo cargo:@Evento de Natal`
-   **`/revalidar notificar_todos`**
    -   > **Exemplo:** `/revalidar notificar_todos mensagem:Olá a todos! O servidor entrará em manutenção amanhã às 14h.`

---

## 🙋 Comandos para Clientes

-   **Interagir com Painéis**
    -   > Clicar nos botões e menus de seleção nos canais de loja é a principal forma de compra.
-   **`/sacola ver`**
    -   > **Exemplo:** `/sacola ver`
-   **`/minhascompras`**
    -   > **Exemplo:** `/minhascompras`
-   **`/loja top`**
    -   > **Exemplo:** `/loja top limite:5`
-   **`/loja meugasto`**
    -   > **Exemplo:** `/loja meugasto`
-   **`/loja plano`**
    -   > **Exemplo:** `/loja plano`
-   **`/loja mudardeplano`**
    -   > **Exemplo:** `/loja mudardeplano` (Para comprar ou estender a assinatura premium).
-   **`/loja robux calcular_robux`**
    -   > **Exemplo:** `/loja robux calcular_robux quantidade_robux:1000`
-   **`/cupom resgatar`**
    -   > **Exemplo:** `/cupom resgatar`
-   **`/cupom meuscupons`**
    -   > **Exemplo:** `/cupom meuscupons`
-   **`/sorteio minhasmensagens`**
    -   > **Exemplo:** `/sorteio minhasmensagens`
