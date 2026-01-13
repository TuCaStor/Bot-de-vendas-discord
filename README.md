# 🤖 Guia Oficial - TuCaNo Store Bot

## 📞 Suporte e Contato
Para suporte, contate: **`moshiini_`** no Discord.
Ou entre no nosso servidor oficial: [https://discord.gg/rPFqpK2gqX](https://discord.gg/rPFqpK2gqX)

---

## ➕ Adicione o Bot
[**Clique aqui para convidar o Bot para seu servidor**](https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot)

---

## 🆘 Suporte Técnico (Exclusivo para Lojistas)
**Precisa de ajuda com o bot?**
O sistema de suporte via DM é restrito exclusivamente para **Donos de Servidores** e **Donos de Lojas**.

*   **Como funciona:** Envie um "Oi" na DM (privado) do bot.
*   **O que acontece:** Um ticket será aberto diretamente com a administração do bot.
*   **Atenção:** Clientes comuns que tentarem enviar mensagem serão bloqueados automaticamente pelo sistema.

---

## 🚀 Começando do Zero (Configuração Obrigatória)
*Passos essenciais para o Dono do Servidor.*

### 1. Vincular a Loja (Ativação)
Ativa o bot e define o sistema financeiro.
*   **Comando:** `/loja vincular`
*   **🎁 Bônus:** As primeiras **24 horas** após vincular são **GRÁTIS** (0% de taxa) para você testar tudo!
*   **Taxas (Pós-teste):** Comissão de **2%** sobre vendas OU Assinatura fixa de **R$ 0,50/dia**.

### 2. Configurar Canais
Defina onde o bot vai trabalhar.
*   **Comando:** `/configurar canais`
*   **Exemplo:** `/configurar canais categoria_tickets:#Compras canal_logs:#logs-privado`
*   **Detalhes:**
    *   `categoria_tickets`: Onde os carrinhos de compra serão abertos.
    *   `canal_logs`: **(Essencial)** Canal privado para histórico de vendas e backups.
    *   `canal_provas`: Onde as fotos de entrega são enviadas.
    *   `canal_logs_membros`: Monitora entrada/saída de membros (anti-fake).

### 3. Configurar Pagamento (PIX)
*   **Comando:** `/configurar pix`
*   **O que faz:** Abre um formulário seguro para colocar sua Chave PIX, Nome e Cidade.

---

## 🎛️ Painel de Controle (Recomendado)
**O jeito mais fácil de usar!** Esqueça a decoração de comandos. Gerencie tudo com cliques.

### 📌 Dashboard Fixo
Cria um menu permanente em um canal da Staff.
*   **Comando:** `/gerenciar_loja dashboard_fixo canal:#staff-loja`
*   **O que faz:**
    *   📦 **Gerenciar Produtos:** Adicionar, Editar (Preço/Estoque), Excluir.
    *   🖼️ **Gerenciar Painéis:** Criar menus, adicionar itens, postar no canal.

---

## 🛠️ Comandos Manuais de Loja (Avançado)
*Use estes comandos para ajustes finos e personalizações.*

### 📦 Produtos (`/produto`)
*   **Criar:** `/produto adicionar`
    *   *Campos:* Nome, Tipo (Item/Moeda), Preço, Estoque, Emoji (ícone).
    *   **💡 Truque de Suporte:** Se criar um **Item Único** com **Preço 0** e **Estoque Infinito (-1)**, o bot cria um botão de "Abrir Ticket" em vez de cobrar.
*   **Editar:** `/produto editar`
    *   Use para mudar Preço, Estoque, Nome ou Emoji.
    *   **Qtd. Mínima:** Defina `nova_quantidade_minima` aqui (ex: cliente só pode comprar acima de 1000 un).
*   **Outros:**
    *   `/produto status`: Ativa/Desativa um produto (some do menu sem excluir).
    *   `/produto limiar_estoque`: Bot avisa quando o estoque estiver baixo.

### 🖼️ Painéis de Venda (`/painel`)
*   **Criar:** `/painel criar` - Cria o registro do painel no sistema.
*   **Postar:** `/painel postar` - Envia um painel já criado para um canal específico.
*   **Sincronizar:** `/painel sync` - Força a atualização visual (estoque, preços) na mensagem já postada.
*   **Adicionar Opção:** `/painel add_opcao` - Coloca um produto dentro do menu.
*   **Personalizar:** `/painel editar_opcao`
    *   Permite mudar o **Emoji** ou **Nome** de um item *apenas* dentro daquele painel específico (sem alterar o produto original).

---

## ⚙️ Administração e Segurança

### 📊 Dados e Backups
*   `/gerenciar_loja estatisticas` - Vendas totais, lucro e itens mais vendidos.
*   `/gerenciar_loja relatorio` - Baixa uma planilha Excel (CSV) completa.
*   `/gerenciar_loja backup` - Envia um arquivo de segurança da sua loja na sua DM.
*   `/gerenciar_loja restaurar` - Reconstrói a loja inteira usando o arquivo de backup.

### ✅ Verificação e Segurança
*   `/configurar verificacao definir` - Configura canal e cargo de verificação.
*   `/verificacao postar_painel` - Envia o botão de "Verificar-se" no canal.

### 🚫 Canais Ignorados
*   `/configurar canal_ignorado adicionar` - O bot não conta mensagens de sorteio nestes canais (anti-flood).

---

## 🤝 Engajamento (Sorteios e Cupons)

### 🎉 Sorteios (`/sorteio`)
*   `/sorteio criar` - Inicia um sorteio (tempo, ganhadores, requisitos).
*   `/sorteio gerenciar` - Painel para encerrar antes, rerrolar ou cancelar.

### 🎟️ Cupons (`/cupom`)
*   `/cupom admin_criar_publico` - Cria código tipo "NATAL10" (qualquer um usa).
*   `/cupom admin_criar_tipo` - Cria cupom para ser ganho em sorteios (item de inventário).

---

## 👤 Comandos para Clientes (Públicos)

*   `/minha_loja` - **O Hub do Cliente.** Mostra histórico, gastos e cupons.
*   `/sacola ver` - Mostra o carrinho de compras atual.
*   `/sugestao` - Envia uma sugestão para a administração (Delay de 24h).
*   `/cupom resgatar` - Troca mensagens por chances de ganhar cupons.
*   `/loja robux calcular_robux` - Calculadora de taxas do Roblox.

---

## 🔒 Área Restrita (Dono do Bot)
*Comandos exclusivos do desenvolvedor/hoster do bot.*

### 📢 Ações em Massa
*   `/botadmin avisar_geral` - Envia um aviso na DM de todos os donos de lojas/servidores.
*   `/revalidar notificar_todos` - Envia DM para **todos** os membros do servidor atual.
*   `/revalidar remover_cargo` - Remove um cargo de **todos** os membros.

### 🛡️ Moderação Global
*   **Suporte (Modmail):**
    *   `/modmail_admin configurar`: Define onde os tickets da DM aparecem.
    *   `/modmail_admin bloquear/desbloquear`: Bane usuários do suporte.
*   **Sugestões:**
    *   `/sugestao_admin bloquear/desbloquear`: Impede usuários de enviar sugestões.

### 🔑 Licenças e Faturamento
*   `/botadmin gerar_cobranca_licenca`: Gera cobrança para servidor Premium.
*   `/botadmin licenca definir`: Ativa licença manualmente.
*   `/botadmin bloquear_loja`: Trava uma loja remotamente.
