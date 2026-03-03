# 🏛️ Projeto Lumen Pessoal (Automação LAI/Asana)

O **Projeto Lumen Pessoal** é uma solução de automação desenvolvida para otimizar a gestão de solicitações de acesso à informação (LAI) e tarefas críticas. Ele utiliza o **n8n** para contornar limitações de planos gratuitos do Asana, implementando uma lógica avançada de prazos e movimentação automática.

## 🚀 Principais Recursos
- **Gestão de Prazos**: Cálculo automático baseado em metadados de subtarefas.
- **Triagem Automatizada**: Organização de cartões em seções por criticidade (Vencidos, >10 dias, <10 dias).
- **Controle via Telegram**: Comandos remotos e relatórios de execução em tempo real.

## 📁 Estrutura do Repositório
- `workflow-lumen.json`: O fluxo para importação no n8n (versão tratada para privacidade).
- [DOCUMENTACAO.md](./DOCUMENTACAO.md): Detalhamento técnico da lógica de cada nó e funcionamento do sistema.
- [CHANGELOG.md](./CHANGELOG.md): Histórico de versões e melhorias.

## 🛠️ Como Instalar
1. Importe o arquivo `.json` na sua instância n8n.
2. Configure as credenciais do Asana e Telegram conforme indicado na [Documentação](./DOCUMENTACAO.md).
3. Ajuste os IDs de projeto e seções no Asana.

---
*Desenvolvido por **Vinícios Campos** | Especialista em Governança de Dados e Gestão de Projetos.*