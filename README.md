# 🤖 Guia de Comandos - TuCaNo Store Bot

## 📞 Suporte e Contato
Para suporte, contate: **`moshiini_`** no Discord.
Ou entre no nosso servidor oficial: [https://discord.gg/rPFqpK2gqX](https://discord.gg/rPFqpK2gqX)

---

## ➕ Adicione o Bot
[**Clique aqui para convidar o Bot para seu servidor**](https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot)

---

## 🚀 Começando do Zero (Configuração Obrigatória)
*Apenas o Dono do Servidor ou Admins podem fazer isso.*

### 1. Vincular a Loja
O passo mais importante. Ativa o bot e define o sistema de faturamento.
*   **Comando:** `/loja vincular`
*   **O que faz:** Cria o registro da sua loja no banco de dados.

### 2. Configurar Canais
Defina onde o bot vai trabalhar.
*   **Comando:** `/configurar canais`
*   **Parâmetros Importantes:**
    *   `categoria_tickets`: Categoria onde os carrinhos de compra serão criados.
    *   `canal_logs`: **(Essencial)** Canal privado onde ficam históricos de vendas e backups.
    *   `canal_provas`: Onde as fotos de entrega são postadas.
    *   `canal_logs_membros`: Para ver quem entra e sai (com análise de conta fake).

### 3. Configurar PIX
Para receber o dinheiro das vendas.
*   **Comando:** `/configurar pix`
*   **O que faz:** Abre um formulário seguro para colocar sua Chave PIX, Nome e Cidade.

---

## 🎛️ Painel de Controle (O Jeito Fácil)
**Esqueça a decoração de comandos!** Use o painel interativo para gerenciar tudo com cliques.

### 📌 Dashboard Fixo (Recomendado)
Cria um painel permanente em um canal de staff.
*   **Comando:** `/gerenciar_loja dashboard_fixo canal:#staff-loja`
*   **O que permite fazer com cliques:**
    *   📦 **Gerenciar Produtos:** Adicionar, Editar, Excluir, Mudar Preço/Estoque.
    *   🖼️ **Gerenciar Painéis:** Criar menus de venda, adicionar opções aos menus, postar no canal.

### 🕹️ Painel Temporário
Se você não quer fixar uma mensagem, abra um menu só para você.
*   **Comando:** `/gerenciar_loja painel_controle`

---

## 🛠️ Comandos Manuais de Loja (Alternativos)
*Use estes comandos se preferir não usar o Painel Visual.*

### 📦 Produtos
*   `/produto adicionar` - Cadastra um novo item.
    *   *Ex: `/produto adicionar nome_exibicao:Ouro tipo_produto:Moeda modelo_preco:Milhar valor_preco:10 estoque:-1`*
*   `/produto editar` - Altera preço, nome ou estoque.
*   `/produto status` - Ativa/Desativa um produto (some do menu sem excluir).
*   `/produto limiar_estoque` - Define quando o bot avisa que o estoque está baixo.
*   `/produto excluir` - Apaga o produto permanentemente.

### 🖼️ Painéis de Venda
*   `/painel criar` - Cria a mensagem bonita com o menu.
*   `/painel add_opcao` - Adiciona um produto dentro de um painel existente.
*   `/painel remover_opcao` - Tira um produto do painel.
*   `/painel sync` - **Importante:** Atualiza visualmente o painel (estoque, preços) se algo mudar.

---

## ⚙️ Configurações e Admin

### 📊 Relatórios e Backups
*   `/gerenciar_loja estatisticas` - Vendas totais, lucro e top produtos.
*   `/gerenciar_loja relatorio` - Baixa uma planilha Excel (CSV) com todas as vendas.
*   `/gerenciar_loja backup` - Envia um arquivo de segurança com toda sua loja.
*   `/gerenciar_loja restaurar` - Reconstrói a loja usando um arquivo de backup.

### 🏆 Recompensas e Cargos
*   `/configurar recompensa adicionar` - Cliente ganha cargo X ao gastar valor Y.
*   `/configurar cargo_suporte adicionar` - Define quem pode ver/responder tickets.

### ✅ Verificação
*   `/configurar verificacao definir` - Configura canal e cargo de verificação.
*   `/verificacao postar_painel` - Envia o botão de "Verificar-se" no canal.

### 🚫 Canais Ignorados
*   `/configurar canal_ignorado adicionar` - O bot não conta mensagens de sorteio nestes canais.

---

## 🎉 Sorteios e Cupons

### 🎁 Sorteios
*   `/sorteio criar` - Inicia um sorteio avançado.
    *   *Ex: `/sorteio criar duracao:24h premio:Nitro Vencedores:1`*
*   `/sorteio gerenciar` - Painel para encerrar, rerrolar (sortear de novo) ou cancelar.

### 🎟️ Cupons
*   `/cupom admin_criar_publico` - Cria código tipo "NATAL10".
*   `/cupom admin_criar_tipo` - Cria cupom para ser ganho em sorteio/resgate.
*   `/cupom admin_listar` - Vê todos os cupons ativos.

---

## 👤 Comandos para Clientes (Públicos)

*   `/minha_loja` - **O Hub do Cliente.** Mostra histórico, gastos e cupons.
*   `/sacola ver` - Mostra o carrinho de compras atual.
*   `/cupom resgatar` - Troca mensagens por cupons de desconto.
*   `/sugestao` - Envia uma sugestão para a administração.
*   `/loja robux calcular_robux` - Calculadora de taxas do Roblox.

---

## 🔒 Área Restrita (Dono do Bot)
*Comandos exclusivos do desenvolvedor/hoster do bot.*

### 📢 Ações em Massa
*   `/revalidar notificar_todos` - Envia DM para **todos** do servidor.
*   `/revalidar remover_cargo` - Remove um cargo de **todos** os membros.

### 🛡️ Moderação de Sugestões
*   `/sugestao_admin bloquear` - Impede um usuário de enviar sugestões.
*   `/sugestao_admin desbloquear` - Libera o usuário.

### 🔑 Licenças (Cobrança)
*   `/botadmin gerar_cobranca_licenca` - Cria cobrança para servidor Premium.
*   `/botadmin licenca definir` - Ativa licença manualmente.
*   `/botadmin bloquear_loja` - Trava uma loja remotamente.
