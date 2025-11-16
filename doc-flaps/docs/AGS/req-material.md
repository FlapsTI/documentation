# Requisitos - Sistema de Gestão de EPIs e EPCs

## Visão Geral
Sistema para controle de entrada, saída, rastreamento e geração de relatórios de Equipamentos de Proteção Individual (EPIs) e Equipamentos de Proteção Coletiva (EPCs). O sistema deve permitir registro de movimentações vinculadas a funcionários e gerar relatórios automáticos conforme pedido.

## Requisitos Funcionais

### 1. Controle de Entrada e Saída
- O sistema deve registrar a entrada de EPIs e EPCs no almoxarifado.
- O sistema deve registrar a saída de EPIs e EPCs do almoxarifado.
- Cada movimentação deve ser vinculada a um funcionário específico.
- O sistema deve registrar o responsável pela entrega ou retirada (ex.: almoxarife).
- O sistema deve armazenar a data da retirada do material.
- O sistema deve armazenar a data prevista para devolução do material.
- O sistema deve permitir configurar prazos de devolução diferentes para cada tipo de material.
- O sistema deve calcular automaticamente o prazo de devolução em dias a partir da data de retirada.
- O sistema deve emitir alertas quando o prazo de devolução estiver próximo ao vencimento.
- O sistema deve emitir alertas quando o prazo de devolução estiver vencido.

### 2. Cadastro de Materiais
- O sistema deve permitir cadastrar novos tipos de EPI.
- O sistema deve permitir cadastrar novos tipos de EPC.
- Cada tipo de material deve ter um prazo padrão de devolução configurável.
- O sistema deve permitir editar informações de tipos de materiais cadastrados.
- O sistema deve permitir deletar tipos de materiais (com validação se estão em uso).

### 3. Consultas e Rastreamento
- O sistema deve permitir consultar os materiais atualmente em posse de cada funcionário.
- O sistema deve permitir filtrar materiais por funcionário.
- O sistema deve permitir filtrar materiais por tipo.
- O sistema deve permitir visualizar o histórico de movimentações de cada material.

### 4. Relatórios
- O sistema deve gerar um relatório mensal com todos os movimentos de entrada e saída.
- O sistema deve permitir visualizar o relatório diretamente na aplicação.
- O sistema deve permitir exportar o relatório em formato .xlsx (Excel).
- O sistema deve permitir exportar o relatório em formato .csv.
- O sistema deve enviar automaticamente por e-mail o relatório mensal para responsáveis cadastrados.
- O relatório deve incluir: tipo de material, funcionário, data de retirada, data de devolução prevista e data de devolução real (se houver).

### 5. Gestão de Permissões e Acesso
- O sistema deve permitir registro de retirada/devolução por usuários admin.
- O sistema deve permitir consulta de materiais por usuários com permissão.
- O sistema deve permitir edição de registros com rastreamento de quem editou.
- O sistema deve permitir cadastro de novos tipos de EPI/EPC por usuários admin.
- O sistema deve respeitar permissões definidas por perfil de usuário.

## Requisitos Não Funcionais

### Usabilidade
- A interface deve ser intuitiva e acessível.
- Os formulários devem utilizar máscaras de entrada (datas em dd/mm/aaaa).
- Funcionalidades de gestão devem ser acessíveis em até 3 cliques.

### Desempenho
- A navegação entre telas não deve ultrapassar 3 segundos.
- Relatórios devem ser gerados em tempo razoável (< 10 segundos para dados mensais).

### Suportabilidade
- O sistema deve funcionar em navegadores Chrome, Firefox e Safari (versões recentes).
- O sistema deve ser responsivo para dispositivos mobile.

### Segurança
- O sistema deve exigir autenticação de usuário.
- Acesso deve ser controlado por permissões de perfil.
- Movimentações devem ser rastreáveis (quem, quando, o quê).

## Notas e Considerações
- Alertas/notificações de devolução dependem de funcionalidade de notificações implementada na aplicação.
- Definir processo de aprovação para exclusão de tipos de materiais.
- Validar duplicidade de códigos/nomes de materiais.



## Histórico de versão

|Nome| Data | Comentário|
|------ |------- |------|
|[Caio Sabino](github.com/caiomsabino) | 13/11/2025 | Adição e formatação dos textos presentes no docs. |