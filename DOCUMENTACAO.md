# 📖 Documentação Técnica - Workflow Lumen

Este documento detalha o funcionamento lógico do workflow `projeto-lumen-pessoal`.

## ⚙️ Arquitetura da Solução


### 1. Coleta e Tratamento de Dados
O fluxo supera a limitação do plano *Personal* do Asana ao buscar metadados dentro das notas de subtarefas específicas:
- **Subtarefa "Abertura"**: Extrai a data e hora de criação.
- **Subtarefa "Encerramento"**: Extrai a data limite de resposta.

### 2. Nó "Cálculo de Dias" (Inteligência)
O processamento é feito via JavaScript, garantindo precisão no fuso horário de Brasília (**UTC-03:00**):
- **Prioridade 1**: Verifica se a data atual ultrapassou o "Encerramento". Se sim, marca como `Vencidos`.
- **Prioridade 2**: Calcula o tempo decorrido desde a "Abertura". Se `>= 10 dias`, marca como `Mais de 10 dias`.

### 3. Automação de Movimentação
O nó **Switch** (Conferência de Prazos) atua como um roteador, movendo os cartões para as seções correspondentes no Asana através da API, garantindo que o quadro visual esteja sempre atualizado sem intervenção humana.

### 4. Interface Telegram
- **Comando `/lumen`**: Trigger via Webhook para execução sob demanda.
- **Logs de Execução**: Relatórios HTML formatados contendo o resumo totalizador de tarefas processadas por categoria.