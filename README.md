# 🤖 Guia Oficial - TuCaNo Store Bot

## 📞 Suporte e Contato
Para suporte, contate: **`moshiini_`** no Discord.
Ou entre no nosso servidor oficial: [https://discord.gg/rPFqpK2gqX](https://discord.gg/rPFqpK2gqX)

---

## ➕ Adicione o Bot
[**Clique aqui para convidar o Bot para seu servidor**](https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot)

---

## 🚀 Começando do Zero (Configuração Obrigatória)
*Estes passos devem ser feitos pelo Dono do Servidor ou Administrador.*

### 1. Vincular a Loja
O passo mais importante. Ativa o bot no servidor.
*   **Comando:** `/loja vincular`

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

## 🎛️ Painel de Controle (O Jeito Fácil)
**Recomendado!** Esqueça a decoração de comandos manuais. Use o painel interativo para gerenciar tudo com cliques.

### 📌 Dashboard Fixo
Cria um menu permanente em um canal da Staff.
*   **Comando:** `/gerenciar_loja dashboard_fixo canal:#staff-loja`
*   **Funcionalidades:**
    *   📦 **Gerenciar Produtos:** Adicionar, Editar Preço/Estoque, Excluir.
    *   🖼️ **Gerenciar Painéis:** Criar menus de venda, adicionar itens ao menu, postar no canal.

---

## 🛠️ Comandos Manuais de Loja (Avançado)
*Use estes comandos para ajustes finos que o Painel de Controle ainda não cobre.*

### 📦 Produtos (`/produto`)
*   **Criar Produto:** `/produto adicionar`
    *   *Parâmetros:* Nome, Tipo (Item/Moeda), Preço, Estoque.
    *   **💡 Dica Pro (Sistema de Suporte):** Se você criar um **Item Único** com **Preço 0** e **Estoque Infinito (-1)**, o bot entende que é um serviço. Ao "comprar", ele abrirá automaticamente um **Ticket de Suporte** em vez de cobrar pagamento.
    *   **Novo:** Use o campo `emoji` para definir um ícone padrão (ex: 💎).

*   **Editar Produto:** `/produto editar`
    *   Use para mudar Preço, Estoque ou Nome.
    *   **Quantidade Mínima:** É aqui que você define a `nova_quantidade_minima` (ex: obrigar a comprar no mínimo 1000 moedas).

*   **Outros:**
    *   `/produto status`: Ativa/Desativa um produto (some do menu sem excluir).
    *   `/produto limiar_estoque`: Bot avisa quando o estoque estiver baixo (ex: abaixo de 5).

### 🖼️ Painéis de Venda (`/painel`)
*   **Criar/Postar:** `/painel criar` e `/painel sync`.
    *   **Nota:** O comando `/painel sync` força a atualização visual (estoque, preços, emojis) na mensagem do canal.
*   **Editar Aparência:** `/painel editar_opcao`
    *   Use este comando para mudar o **Emoji** ou **Nome** de um item *apenas* dentro daquele painel específico, sem alterar o produto original.

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
*   `/configurar canal_ignorado adicionar` - O bot não conta mensagens de sorteio nestes canais (ex: flood).

---

## 🤝 Engajamento (Sorteios e Cupons)

### 🎉 Sorteios (`/sorteio`)
*   `/sorteio criar` - Inicia um sorteio (tempo, ganhadores, requisitos de cargo/mensagens).
*   `/sorteio gerenciar` - Painel para encerrar antes da hora, rerrolar (sortear de novo) ou cancelar.

### 🎟️ Cupons (`/cupom`)
*   `/cupom admin_criar_publico` - Cria código tipo "NATAL10" (qualquer um usa).
*   `/cupom admin_criar_tipo` - Cria cupom para ser ganho em sorteios (item de inventário).

---

## 👤 Comandos para Clientes (Públicos)

*   `/minha_loja` - **O Hub do Cliente.** Mostra histórico, gastos e cupons.
*   `/sacola ver` - Mostra o carrinho de compras atual.
*   `/sugestao` - Envia uma sugestão diretamente para a administração (com delay de 24h).
*   `/cupom resgatar` - Troca mensagens por chances de ganhar cupons.
*   `/loja robux calcular_robux` - Calculadora de taxas do Roblox.

---

## 🔒 Área Restrita (Dono do Bot)
*Comandos exclusivos do desenvolvedor/hoster do bot.*

### 📢 Ações em Massa
*   `/revalidar notificar_todos` - Envia DM para **todos** os membros do servidor (Cuidado!).
*   `/revalidar remover_cargo` - Remove um cargo de **todos** os membros.

### 🛡️ Moderação de Sugestões
*   `/sugestao_admin bloquear` - Impede um usuário chato de enviar sugestões.
*   `/sugestao_admin desbloquear` - Libera o usuário.

### 🔑 Licenças (Cobrança)
*   `/botadmin gerar_cobranca_licenca` - Gera PIX para servidor Premium.
*   `/botadmin licenca definir` - Ativa licença manualmente.
*   `/botadmin bloquear_loja` - Trava uma loja remotamente por falta de pagamento.
