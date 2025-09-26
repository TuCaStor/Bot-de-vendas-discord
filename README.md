# 🤖 Guia de Comandos - TuCaNo Store Bot

# Para suporte contate: tucaca_1_40280 no discord

Bem-vindo ao guia completo de comandos para o seu bot de loja! Este documento foi feito para ajudar os donos de servidor a configurar e gerenciar suas lojas de forma rápida e fácil.

## ➕ Adicione o Bot ao seu Servidor

Para começar, adicione o TuCaNo Store Bot ao seu servidor Discord clicando no link abaixo:

[**Clique aqui para convidar o Bot**](https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot)

---

## 🚀 Primeiros Passos e Configuração Essencial

Após adicionar o bot, siga esta sequência para deixar sua loja 100% funcional.

### 1. Ative a Loja no seu Servidor

Este é o primeiro e mais importante comando! Ele ativa o bot no seu servidor, colocando-o no plano de comissão padrão e vinculando a sua conta de dono para o faturamento.

- **`/loja vincular`**

### 2. Configure os Canais

Defina onde cada ação do bot irá acontecer. Sem isso, os tickets e logs não funcionarão.

- **`/configurar canais`**
  - > **`categoria_tickets`**: A categoria onde os carrinhos de compra serão criados.
  - > **`categoria_suporte`**: A categoria para tickets de suporte geral.
  - > **`canal_provas`**: Canal onde as provas de entrega são postadas.
  - > **`canal_avaliacoes`**: Canal onde as avaliações dos clientes são exibidas.
  - > **`canal_logs`**: **(MUITO IMPORTANTE)** Canal privado onde o bot enviará históricos de conversas e backups.
  - > **`canal_comandos_sacola`**: *[Opcional]* Canal dedicado para os comandos `/sacola`.

### 3. Configure o PIX

Para receber pagamentos, configure sua chave PIX. Ela será criptografada e armazenada de forma segura.

- **`/configurar pix`**
  - Abre um formulário para você inserir seus dados de pagamento.
  - > **Chave PIX**: Seu e-mail, telefone, CPF/CNPJ ou chave aleatória.
  - > **Nome do Beneficiário**: Seu nome completo, como aparece no PIX.
  - > **Cidade**: A cidade registrada na chave PIX (ex: SAO PAULO).

---

## 🛠️ Gerenciamento da Loja (Administradores e Gerentes)

Comandos para o dia a dia da sua loja.

### 📦 Gerenciamento de Produtos (`/produto`)

- **`/produto adicionar`**: Adiciona um novo produto.
- **`/produto editar`**: Edita um produto existente.
- **`/produto excluir`**: Apaga um produto permanentemente.
- **`/produto status`**: Ativa ou desativa um produto.
- **`/produto listar`**: Mostra todos os produtos cadastrados.
- **`/produto info`**: Exibe detalhes completos de um produto.
- **`/produto limiar_estoque`**: Define um alerta para quando o estoque de um item estiver baixo.

### 🖼️ Gerenciamento de Painéis (`/painel`)

Painéis são as vitrines interativas onde os clientes escolhem os produtos.

- **`/painel criar`**: Cria um novo painel de vendas em um canal.
- **`/painel editar`**: Edita o título, descrição, imagens ou cor de um painel.
- **`/painel excluir`**: Apaga permanentemente um painel e sua mensagem.
- **`/painel add_opcao`**: Adiciona um produto como opção em um painel.
- **`/painel remover_opcao`**: Remove um produto de um painel.
- **`/painel sync`**: Força a atualização de um painel para refletir as mudanças mais recentes.

### 🕹️ Gerenciamento Geral (`/gerenciar_loja`)

- **`/gerenciar_loja painel_controle`**: Abre um menu interativo para gerenciar produtos e painéis.
- **`/gerenciar_loja estatisticas`**: Mostra um resumo de vendas, produtos mais vendidos e maiores clientes.
- **`/gerenciar_loja relatorio`**: Exporta um relatório de vendas detalhado em formato `.csv`.
- **`/gerenciar_loja diagnostico`**: Verifica se todas as configurações do bot no servidor estão corretas.
- **`/gerenciar_loja backup`**: Gera um arquivo de backup de toda a sua loja e envia na sua DM.
- **`/gerenciar_loja restaurar`**: **(CUIDADO)** Restaura a loja a partir de um arquivo de backup.

### ⚙️ Configurações Adicionais (`/configurar`)

- **`/configurar recompensa adicionar`**: Define um cargo que será dado automaticamente quando um cliente atingir um valor total de gastos.
- **`/configurar recompensa listar`**: Lista todas as recompensas configuradas.
- **`/configurar cargo_suporte adicionar`**: Permite que um cargo veja e responda a todos os tickets.
- **`/configurar canal_ignorado adicionar`**: Faz com que mensagens em um canal não contem para sorteios.

### 🎉 Gerenciamento de Sorteios (`/sorteio`)

- **`/sorteio criar`**: Inicia um novo sorteio.
- **`/sorteio gerenciar`**: Abre um painel para finalizar, rerolar ou cancelar sorteios.

### 🎟️ Gerenciamento de Cupons (`/cupom admin`)

- **`/cupom admin_criar_tipo`**: Cria um cupom que pode ser resgatado por sorteio.
- **`/cupom admin_criar_publico`**: Cria um código de desconto que qualquer um pode usar (ex: `BEMVINDO10`).
- **`/cupom admin_listar`**: Lista todos os cupons e códigos criados.
- **`/cupom admin_excluir`**: Apaga permanentemente um cupom ou código.

### ✅ Sistema de Verificação (`/verificacao`)

- **`/configurar verificacao definir`**: Define o canal e o cargo para o sistema de verificação.
- **`/verificacao postar_painel`**: Posta a mensagem com o botão "Verificar" no canal configurado.

### 📢 Ações em Massa (`/revalidar`)

- **`/revalidar remover_cargo`**: **(CUIDADO)** Remove um cargo de todos os membros do servidor.
- **`/revalidar notificar_todos`**: **(CUIDADO)** Envia uma mensagem na DM de todos os membros do servidor.

---

## 🙋 Comandos para Clientes e Usuários

Estes são os comandos que os membros do seu servidor usarão.

- **Interagir com os Painéis**: A principal forma de compra é clicando nos menus dos painéis de venda.
- **`/sacola ver`**: Mostra sua sacola de compras, permitindo remover itens, editar quantidades e aplicar cupons.
- **`/minhascompras`**: Mostra seu histórico das últimas 10 compras.
- **`/loja top`**: Exibe o ranking dos clientes que mais gastaram na loja.
- **`/loja meugasto`**: Mostra seu gasto total e qual a próxima recompensa de cargo.
- **`/loja plano`**: Verifica o plano atual da sua loja (Comissão ou Assinatura).
- **`/loja mudardeplano`**: Permite comprar uma assinatura para a loja, mudando do plano de comissão.
- **`/loja robux calcular_robux`**: Ajuda a calcular o preço de Robux com e sem a taxa de 30% do Roblox.
- **`/cupom resgatar`**: Gasta mensagens para tentar a sorte e ganhar um cupom de desconto.
- **`/cupom meuscupons`**: Lista todos os cupons que você possui.
- **`/sorteio minhasmensagens`**: Verifica seu saldo de mensagens para usar em sorteios.
