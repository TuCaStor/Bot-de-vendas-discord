# TuCaNo Store v3 — Documentação Oficial

O **TuCaNo Store** é um sistema automatizado de vendas, suporte e engajamento integrado diretamente ao Discord. Ele foi projetado para fornecer uma experiência de e-commerce fluida para os clientes e ferramentas robustas de administração e auditoria para os lojistas, contando com geração automatizada de pagamentos via **PIX**, emissão de cupons de desconto, controle de estoque inteligente e suporte centralizado.

---

## 🔗 Link de Convite Oficial
Para adicionar o bot ao seu servidor com as permissões administrativas recomendadas, clique no link abaixo:

> **[Convidar TuCaNo Store v3 para o Servidor](https://discord.com/oauth2/authorize?client_id=1360681926318624908&permissions=8&scope=bot)**

---

## 🪙 Modelos de Negócio e Faturamento

O bot oferece dois modelos de cobrança para os servidores que desejam utilizar a estrutura de e-commerce:

1. **Plano de Comissão (Padrão)**:
   * **Isenção Inicial (Teste)**: As primeiras **24 horas** após a criação da loja no servidor são totalmente gratuitas (0% de taxa) para testes.
   * **Funcionamento**: Após as 24h iniciais, é aplicada uma taxa de comissão de **2%** sobre o valor de cada venda concluída.
   * **Ciclo de Faturamento**: A cada **15 dias**, o sistema gera uma fatura consolidada e a envia na DM do dono do servidor.
   * **Prazo de Pagamento**: O lojista tem **7 dias** para realizar o pagamento via PIX. Caso a fatura vença, a loja é temporariamente bloqueada até a quitação.
2. **Plano de Assinatura (Premium)**:
   * **Funcionamento**: Custo fixo de **R$ 0,50 por dia** de assinatura (sem taxas sobre vendas).
   * **Vantagens**: Isenção total de comissão sobre vendas, remoção de anúncios e liberação imediata caso a loja estivesse bloqueada por saldo devedor.

---

## 🛠️ Guia de Configuração Rápida (Lojistas)

Para colocar sua loja para funcionar, siga estes passos simples:

1. **Vincule o seu Servidor**: Use `/loja vincular` para registrar seu servidor no plano básico com 24h de teste.
2. **Configure as Categorias e Canais**: Use `/configurar canais` para definir os canais de logs, comprovantes, avaliações e as categorias onde os canais de compra (tickets) serão criados.
3. **Configure o seu PIX**: No final do passo anterior (ou usando `/configurar pix`), insira sua chave PIX, nome do beneficiário e cidade para poder receber as vendas diretamente na sua conta de forma criptografada.
4. **Adicione um Cargo de Suporte**: Use `/configurar cargo_suporte adicionar` para permitir que sua equipe de moderadores/atendentes veja e interaja com os tickets de compra criados pelos clientes.
5. **Crie o seu Primeiro Produto**: Use `/produto adicionar` informando nome, tipo (Moeda ou Item Único), modelo de preço e estoque.
6. **Monte um Painel de Vendas**: Use `/painel criar` para gerar a mensagem visual da sua vitrine e use `/painel add_opcao` para atrelar seus produtos criados ao dropdown (menu de seleção) do painel.

---

## 📚 Índice de Comandos

### 🛒 1. Comandos para Clientes e Sacola (Públicos)
Esses comandos são de livre acesso para todos os membros do servidor realizarem suas compras e acompanharem seus dados.

*   **`/loja minha_loja`**
    *   *Descrição*: Abre o painel pessoal do cliente (visível apenas para ele) com atalhos para verificar a sacola de compras, histórico de transações e estatísticas de gastos.
*   **`/loja top [limite]`**
    *   *Descrição*: Exibe um ranking estilizado com os maiores apoiadores (clientes com maior gasto acumulado) da loja do servidor.
*   **`/loja meugasto`**
    *   *Descrição*: Informa ao usuário seu gasto total no servidor e quanto falta para atingir o próximo cargo de recompensa configurado na loja.
*   **`/loja robux calcular_robux [quantidade_robux]`**
    *   *Descrição*: Uma calculadora integrada que exibe o custo em BRL para adquirir uma quantidade específica de Robux, detalhando o valor real com e sem a cobertura da taxa de 30% do Roblox.
*   **`/sacola ver`**
    *   *Descrição*: Exibe os itens atualmente adicionados ao carrinho de compras do usuário. Permite aplicar cupons, editar quantidades, remover itens e prosseguir para a finalização da compra (abertura do ticket de pagamento).

---

### 📦 2. Comandos de Gerenciamento de Produtos (Administrativos)
Destinados a gerenciar o inventário e as configurações individuais de cada produto oferecido.

*   **`/produto adicionar [nome_exibicao] [tipo_produto] [modelo_preco] [valor_preco] [estoque] [quantidade_minima] [descricao] [url_imagem] [emoji]`**
    *   *Descrição*: Cadastra um novo produto na loja do servidor.
    *   *Campos*:
        *   `tipo_produto`: Moeda (CURRENCY) ou Item Único (UNIQUE_ITEM).
        *   `modelo_preco`: Preço por Unidade ou Preço por Milhar (Ex: Robux).
        *   `estoque`: Quantidade disponível (-1 para estoque infinito).
        *   `quantidade_minima`: Quantidade mínima de compra permitida (opcional).
        *   `emoji`: Emoji padrão atrelado ao item no painel.
*   **`/produto editar [produto] [novo_nome] [novo_valor_preco] [novo_estoque] [nova_quantidade_minima] [nova_descricao] [nova_url_imagem] [novo_emoji]`**
    *   *Descrição*: Edita os campos de um produto existente. Escreva `REMOVER` nos campos opcionais se desejar limpá-los do banco de dados. Os painéis que contêm o produto são atualizados automaticamente na hora.
*   **`/produto status [produto] [status]`**
    *   *Descrição*: Ativa ou desativa um produto. Produtos desativados não são exibidos nos painéis de venda e não podem ser adicionados ao carrinho.
*   **`/produto limiar_estoque [produto] [limite]`**
    *   *Descrição*: Define um alerta de estoque baixo. O bot enviará um aviso no canal de logs da loja quando o produto atingir um estoque igual ou menor que o definido.
*   **`/produto info [produto]`**
    *   *Descrição*: Exibe uma ficha técnica detalhada sobre as configurações do produto selecionado.
*   **`/produto listar`**
    *   *Descrição*: Lista os produtos cadastrados com menus interativos para edição e exclusão simplificada.
*   **`/produto excluir [produto]`**
    *   *Descrição*: Apaga permanentemente o produto do banco de dados.

---

### 🖼️ 3. Comandos de Painéis e Opções (Vitrine)
Responsáveis por estruturar as vitrines interativas (Embeds com menus dropdown) onde os clientes realizam as compras.

*   **`/painel criar [canal] [id_painel] [titulo] [descricao] [url_banner] [url_thumbnail] [cor_hex]`**
    *   *Descrição*: Cria um novo painel de vendas no canal especificado.
*   **`/painel postar [id_painel] [canal]`**
    *   *Descrição*: Envia ou move a mensagem de um painel de vendas existente para um novo canal do servidor.
*   **`/painel add_opcao [id_painel] [produto] [label] [descricao] [emoji]`**
    *   *Descrição*: Vincula um produto a um painel de vendas como uma opção selecionável no menu dropdown.
*   **`/painel remover_opcao [id_painel] [opcao]`**
    *   *Descrição*: Remove uma opção do menu de seleção do painel.
*   **`/painel editar [id_painel] [novo_titulo] [nova_descricao] [nova_url_banner] [nova_url_thumbnail] [nova_cor_hex]`**
    *   *Descrição*: Altera as propriedades de formatação visual do painel. Escreva `REMOVER` nas propriedades opcionais para limpá-las.
*   **`/painel editar_opcao [id_painel] [opcao] [novo_emoji] [novo_label] [nova_descricao]`**
    *   *Descrição*: Altera as propriedades visuais de uma opção específica contida no menu dropdown do painel (como o emoji exibido ou a descrição do item).
*   **`/painel sync [id_painel]`**
    *   *Descrição*: Força a mensagem do painel no canal do Discord a sincronizar visualmente com os dados armazenados no banco de dados (útil caso o bot tenha ficado offline ou para atualizar dados de estoque exibidos).
*   **`/painel excluir [id_painel]`**
    *   *Descrição*: Deleta o painel do banco de dados e remove a mensagem original associada a ele no Discord.

---

### 🎫 4. Comandos de Cupons e Descontos
Gerenciamento de cupons de inventário (obtidos por engajamento) e cupons públicos para campanhas promocionais.

*   **`/cupom resgatar`**
    *   *Descrição*: Gasta **20 mensagens** do saldo do chat do usuário para realizar um sorteio em tempo real de um cupom de desconto aleatório para o inventário dele.
*   **`/cupom meuscupons`**
    *   *Descrição*: Exibe uma lista com todos os cupons que o usuário possui no seu inventário pessoal e que ainda não foram utilizados.
*   **`/cupom admin_criar_tipo [nome] [valor_desconto] [peso_raridade]`**
    *   *Descrição*: Cria um novo tipo de cupom que poderá ser ganho pelos usuários no sorteio do comando `/cupom resgatar`. O `peso_raridade` define a chance do cupom ser sorteado (valores maiores representam cupons mais comuns).
*   **`/cupom admin_criar_publico [codigo] [valor_desconto] [usos_maximos]`**
    *   *Descrição*: Cria um código de desconto público (Ex: `PROMO10`) que qualquer cliente pode digitar manualmente na sacola para obter descontos. `usos_maximos` define o limite de resgates globais permitidos (-1 para infinito).
*   **`/cupom admin_listar`**
    *   *Descrição*: Lista todos os tipos de cupons e códigos de desconto configurados no servidor.
*   **`/cupom admin_remover_tipo [cupom]`**
    *   *Descrição*: Desativa um cupom de sorteio para que ele não seja mais distribuído aos usuários no comando `/cupom resgatar`. (Nota: Cupons já emitidos nos inventários dos usuários continuam utilizáveis).
*   **`/cupom admin_excluir [cupom]`**
    *   *Descrição*: Exclui permanentemente o tipo de cupom ou código público do banco de dados do servidor.

---

### 🎉 5. Comandos de Sorteios e Mensagens
Sistema de engajamento que permite recompensar membros ativos com sorteios que exigem requisitos customizados.

*   **`/sorteio criar [duracao] [premio] [vencedores] [cargo_req] [mensagens_req]`**
    *   *Descrição*: Cria um sorteio no canal atual.
    *   *Campos*:
        *   `duracao`: Exemplo: `30s`, `10m`, `2h`, `1d`.
        *   `cargo_req`: Apenas membros com este cargo podem clicar para entrar.
        *   `mensagens_req`: Define um **custo de entrada em mensagens**. Ao entrar no sorteio, a quantidade especificada é deduzida do saldo de mensagens do usuário.
*   **`/sorteio gerenciar`**
    *   *Descrição*: Abre um painel de controle interativo com a lista de todos os sorteios (ativos e finalizados), permitindo encerrar antes do tempo, rerolar vencedores ou excluí-los.
*   **`/sorteio minhasmensagens`**
    *   *Descrição*: Exibe ao usuário o seu saldo de mensagens contadas no servidor (utilizáveis como saldo de resgate para cupons e sorteios).

---

### 🔧 6. Comandos de Configuração (Administrativos)
Configurações de infraestrutura do bot no servidor.

*   **`/configurar canais`**
    *   *Descrição*: Associa os canais e categorias do seu servidor às funções do bot:
        *   *Categoria de Compras*: Onde os canais privados de tickets de pedidos serão abertos.
        *   *Categoria de Suporte*: Onde os tickets de suporte comuns serão criados.
        *   *Canal de Logs da Loja*: Canal privado onde o bot enviará transcripts de chat de tickets finalizados e backups automáticos.
        *   *Canal de Logs de Membros*: Canal privado onde o bot registrará a entrada e saída de membros e análise de suspeita de contas criadas recentemente.
        *   *Canal de Comprovantes*: Onde o bot postará os comprovantes das entregas feitas pelos administradores.
        *   *Canal de Avaliações*: Onde as notas e comentários dos clientes serão postados.
        *   *Canal de Comandos*: Onde os clientes podem rodar comandos como `/sacola ver`.
*   **`/configurar pix`**
    *   *Descrição*: Abre um formulário privado (Modal) para inserir ou atualizar as credenciais do PIX do lojista (Chave PIX, Nome Completo e Cidade). Os dados são protegidos por criptografia militar Fernet antes do salvamento no banco de dados.
*   **`/configurar campo_entrega [texto_do_campo]`**
    *   *Descrição*: Personaliza a pergunta de identificação solicitada no formulário de finalização da compra. (Ex: "Qual seu Nick no Roblox?" ou "Informe seu Riot ID"). Digite `PADRAO` para redefinir.
*   **`/configurar recompensa adicionar [cargo] [valor]`**
    *   *Descrição*: Cria uma regra de cargo por gasto cumulativo. Quando o cliente acumular o valor total especificado em compras entregues, o cargo será atribuído a ele automaticamente.
*   **`/configurar recompensa remover [valor]`**
    *   *Descrição*: Remove a regra de cargo associada ao valor de gasto selecionado.
*   **`/configurar recompensa listar`**
    *   *Descrição*: Lista todas as regras de cargos por gasto cadastrados no servidor.
*   **`/configurar cargo_suporte adicionar [cargo]`**
    *   *Descrição*: Permite que membros portadores de um cargo específico visualizem e respondam canais de tickets de suporte ou compras.
*   **`/configurar cargo_suporte remover [cargo]`**
    *   *Descrição*: Revoga a permissão do cargo para gerenciar novos tickets.
*   **`/configurar cargo_suporte listar`**
    *   *Descrição*: Lista todos os cargos autorizados a visualizar os tickets do servidor.
*   **`/configurar canal_ignorado adicionar [canal]`**
    *   *Descrição*: Faz com que mensagens enviadas no canal selecionado não sejam somadas à carteira de mensagens do usuário (ideal para canais de spam, comandos ou bots).
*   **`/configurar canal_ignorado remover [canal]`**
    *   *Descrição*: Remove o canal da lista de ignorados, voltando a contabilizar as mensagens dos membros.
*   **`/configurar canal_ignorado listar`**
    *   *Descrição*: Lista todos os canais ignorados na contagem de mensagens do servidor.
*   **`/configurar verificacao definir [canal] [cargo_verificado]`**
    *   *Descrição*: Configura a infraestrutura de verificação antispam por CAPTCHA, definindo em qual canal o botão ficará e qual cargo o membro receberá ao passar no teste.

---

### 🕹️ 7. Comandos de Gestão de Loja (Administrativos)
Estatísticas, relatórios, backups e diagnósticos da saúde do bot.

*   **`/gerenciar_loja painel_controle`**
    *   *Descrição*: Abre um painel interativo temporário (visível apenas para quem usou) contendo botões de atalho para todas as principais ações administrativas do bot.
*   **`/gerenciar_loja dashboard_fixo [canal]`**
    *   *Descrição*: Posta um painel de controle administrativo fixo em um canal privado de staff. Ele não expira e serve como atalho rápido de gerenciamento para a equipe de gerentes.
*   **`/gerenciar_loja estatisticas`**
    *   *Descrição*: Exibe um sumário de desempenho com o faturamento total da loja, ticket médio, quantidade de vendas concluídas, produtos mais vendidos e maiores clientes em gastos acumulados.
*   **`/gerenciar_loja relatorio [periodo] [data_inicio] [data_fim]`**
    *   *Descrição*: Gera um relatório de vendas detalhado contendo dados de ID de compra, comprador, data e valores. O bot envia o relatório em formato de arquivo `.csv`, otimizado e compatível com as formatações do Excel.
*   **`/gerenciar_loja diagnostico`**
    *   *Descrição*: Realiza uma auditoria de integridade nas configurações do servidor. O bot analisa se todos os canais de log, avaliações, categorias e cargos configurados ainda existem e se possui as permissões necessárias de escrita, leitura e hierarquia de cargos para funcionar corretamente.
*   **`/gerenciar_loja backup`**
    *   *Descrição*: Gera um arquivo `.json` de backup contendo todas as configurações da loja, produtos, painéis, cupons e histórico de compras. O bot envia o arquivo na DM do lojista por segurança.
*   **`/gerenciar_loja restaurar [arquivo_backup]`**
    *   *Descrição*: Restaura todas as propriedades, produtos, cupons e configurações do servidor a partir do upload de um arquivo de backup `.json` válido e que pertença a este servidor. **Atenção**: Esta ação substitui os dados atuais e é irreversível.

---

### ⚖️ 8. Comandos Globais de Superusuário (Bot Owner)
Comandos restritos exclusivamente ao desenvolvedor e dono do bot (configurado na hospedagem). Tentativas de uso por outros usuários geram um alerta de segurança e logs de auditoria.

*   **`/botadmin gerar_cobranca_licenca [usuario] [servidor_id] [dias] [valor]`**
    *   *Descrição*: Gera uma cobrança via PIX para o lojista adquirir ou renovar a assinatura Premium do bot para seu servidor.
*   **`/botadmin addgerente [usuario] [servidor_id]`**
    *   *Descrição*: Concede permissão manual de gerente de loja para um usuário em um servidor específico.
*   **`/botadmin removegerente [usuario] [servidor_id]`**
    *   *Descrição*: Revoga a permissão de gerente de um usuário em um servidor específico.
*   **`/botadmin licenca definir [servidor_id] [dias_de_validade]`**
    *   *Descrição*: Atribui ou estende manualmente os dias de licença Premium de um servidor e notifica automaticamente o dono do servidor na DM.
*   **`/botadmin licenca verificar [servidor_id]`**
    *   *Descrição*: Informa o status de faturamento (Premium ou comissão), validade e tempo restante de assinatura de um servidor.
*   **`/botadmin bloquear_loja [servidor_id]`**
    *   *Descrição*: Bloqueia manualmente a loja de um servidor (suspende dropdowns de venda e impede compras).
*   **`/botadmin desbloquear_loja [servidor_id]`**
    *   *Descrição*: Desbloqueia manualmente uma loja suspensa.
*   **`/botadmin avisar_geral [titulo] [mensagem] [tipo]`**
    *   *Descrição*: Realiza uma transmissão global, enviando um Embed de aviso com delay anti-spam de segurança diretamente na DM de **todos os donos de servidores e donos de lojas** registrados no bot (útil para anúncios de manutenção ou atualizações).
*   **`/modmail_admin configurar [categoria]`**
    *   *Descrição*: Configura a categoria do servidor de suporte central do bot onde os canais de tickets de atendimento criados via Modmail serão abertos.
*   **`/modmail_admin bloquear [usuario_id]`**
    *   *Descrição*: Bloqueia um usuário de utilizar o Modmail (ele não poderá abrir novos chamados de suporte).
*   **`/modmail_admin desbloquear [usuario_id]`**
    *   *Descrição*: Remove o bloqueio de Modmail de um usuário.
*   **`/sugestao [mensagem]`**
    *   *Descrição*: Envia uma sugestão/feedback de melhoria de forma privada diretamente para a DM do dono do bot. Possui limite de uso de 24h por usuário.

---

## 🔒 Funcionalidades de Destaque e Segurança

*   **Auditoria de Deleção de Canais**: Se um administrador mal-intencionado ou um invasor excluir manualmente um canal de ticket de compra diretamente pelo Discord (ignorando o botão "Concluir" do bot), o bot captura a exclusão via Logs de Auditoria, gera um **Transcript HTML completo** de todas as mensagens e mídias enviadas no ticket e o envia como anexo em um alerta de segurança privado para o dono do bot.
*   **Segurança de Credenciais**: Informações financeiras de chaves PIX de lojistas passam por criptografia bidirecional simétrica AES-128 via biblioteca **Cryptography (Fernet)** antes de tocarem no banco de dados SQLite, reduzindo riscos em caso de vazamento físico do arquivo `.db`.
*   **Modmail Avançado**: O sistema de Modmail permite que donos de lojas abram tickets de suporte direto na DM do bot para falar com a equipe de suporte do bot. Mensagens, mídias e arquivos são retransmitidos nos dois sentidos, e o sistema bloqueia tentativas de uso por usuários comuns (clientes finais), mantendo a fila focada em lojistas.
*   **Backups Semanais Automáticos**: Todos os domingos às 03:00 UTC, o bot gera e posta um backup estruturado em formato `.json` no canal de Logs de cada servidor, garantindo a possibilidade de restauração de produtos e histórico em caso de acidentes.
