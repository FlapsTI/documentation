# Requisitos - Sistema de Controle de Ponto e Gestão de Funcionários

## Visão Geral
Sistema para registro de ponto (entrada, saída e intervalos), gestão de dados cadastrais de funcionários, geração de relatórios de frequência, e gerenciamento de contratos e escalas. O sistema deve diferenciar acessos entre funcionários e administradores, com suporte a offline.

## Requisitos Funcionais

### 1. Cadastro e Gestão de Funcionários

#### 1.1 Criação de Funcionários
- O sistema deve permitir criar um novo funcionário com nome completo, CPF(validado), endereço completo, contato, cargo, projeto e matrícula(gerada automaticamente).
- Todo funcionário deve ter nome completo.
- Todo funcionário deve ter CPF (validado).
- Todo funcionário deve ter endereço completo.
- Todo funcionário deve ter número de telefone para contato.
- Todo funcionário deve ter um cargo (ex.: Motorista, Operário de máquinas, Arquiteto, Engenheiro, Sócio).
- Todo funcionário deve ter descrição do projeto em que trabalha (opcional).
- Todo funcionário deve ter uma matrícula com 5 dígitos (único).

#### 1.2 Atualização de Funcionários
- O sistema deve permitir que administradores editem dados cadastrais de funcionários.
- O sistema deve permitir atualização de cargo, projeto ou contato.
- Alterações devem ser registradas com data e quem alterou.

#### 1.3 Remoção de Funcionários
- O sistema deve permitir que administradores deletem funcionários.
- Ao deletar, o sistema deve manter histórico (não deletar permanentemente dados históricos).

#### 1.4 Consulta de Funcionários
- O sistema deve listar todos os funcionários.
- O sistema deve permitir filtrar funcionários por cargo, projeto ou status.
- O sistema deve permitir buscar funcionário por nome ou matrícula.

### 2. Autenticação e Permissões

#### 2.1 Tipos de Usuários
- O sistema deve diferenciar login de funcionário e administrador.
- Administradores: Engenheiros, Arquitetos e Sócios.
- Funcionários: demais colaboradores.

#### 2.2 Controle de Acesso
- O sistema deve exigir autenticação para acesso.
- O sistema deve validar permissões por perfil de usuário.
- Funcionários devem acessar apenas suas informações.
- Administradores devem ter acesso total ao sistema.

### 3. Registro de Ponto

#### 3.1 Registros de Horário (a verificar)
- O funcionário/administrador deve registrar hora de entrada.
- O funcionário/administrador deve registrar hora de saída.
- O funcionário/administrador deve registrar início de intervalo.
- O funcionário/administrador deve registrar fim de intervalo.
- Horários devem ser registrados com base no relógio do dispositivo.
- O sistema deve permitir múltiplos intervalos por dia.
- Cada registro deve incluir data, hora e status.

#### 3.2 Validações
- O sistema deve impedir registro de saída antes de entrada.
- O sistema deve validar duração mínima de intervalo.
- O sistema deve permitir correção de registros com justificativa (admin).

#### 3.3 Status de Trabalho
- O funcionário deve poder mudar status para "Em Serviço".
- O funcionário deve poder mudar status para "Fora de Serviço".
- O sistema deve registrar data/hora de mudança de status.

### 4. Banco de Horas

#### 4.1 Cálculos
- O sistema deve calcular horas trabalhadas diariamente.
- O sistema deve calcular horas descansadas (intervalo) diariamente.
- O sistema deve acumular horas trabalhadas mensalmente.
- O sistema deve acumular horas extras ou déficit mensal.

#### 4.2 Status e Gestão
- O sistema deve manter banco de horas por funcionário.
- O sistema deve permitir visualizar saldo atual de banco de horas.
- O sistema deve permitir consultar histórico de banco de horas.

### 5. Gestão de Status do Funcionário
- O sistema deve permitir definir status: "Operante", "Férias", "Licença", "Afastado".
- O sistema deve registrar data de início e fim de cada status.
- O sistema deve permitir visualizar funcionários por status.
- Relatórios devem considerar status do período analisado.

### 6. Escalas e Alocação de Serviços
- O sistema deve permitir criar escalas personalizada de funcionários.
- O sistema deve permitir alocar funcionários a diferentes serviços.
- O sistema deve permitir visualizar escala de um funcionário.
- O sistema deve permitir visualizar funcionários alocados a um serviço.
- **[NOTA: Detalhar com cliente - funcionalidade ainda não clara]**

### 7. Relatórios

#### 7.1 Relatório de Frequência
- O sistema deve gerar relatório de frequência dos funcionários.
- O relatório deve conter nome do funcionário.
- O relatório deve conter matrícula do funcionário.
- O relatório deve conter frequência em dias trabalhados na semana.
- O relatório deve conter frequência em horas totais trabalhadas na semana.
- O relatório deve conter frequência em horas descansadas na semana.
- O relatório deve ser filtrável por período (dia, semana, mês).
- O relatório deve ser filtrável por funcionário.
- O relatório deve ser exportável em .xlsx e .csv.

#### 7.2 Relatório de Horas
- O sistema deve gerar relatório de banco de horas.
- O relatório deve mostrar saldo de horas por funcionário.
- O relatório deve mostrar horas extras e déficit.

### 8. Gestão de Contratos

#### 8.1 Geração de Contratos
- O sistema deve gerar contrato de contratação com informações necessárias.
- O contrato deve incluir dados pessoais do funcionário.
- O contrato deve incluir dados do cargo e projeto.
- O contrato deve incluir termos e condições padrão.

#### 8.2 Assinatura Digital
- O sistema deve permitir integração com assinatura digital gov.br.
- O sistema deve formalizar contratos via assinatura digital.
- O sistema deve armazenar contratos assinados.
- O sistema deve permitir visualizar e baixar contratos assinados.

## Requisitos Não Funcionais

### Usabilidade
- A interface deve ajustar automaticamente para smartphones (481-768px), tablets (835-1024px) e desktops (1367-1440px).
- Funcionalidades para funcionários devem ser realizáveis em até 3 cliques.
- Todos os campos de formulário devem usar máscaras: CPF, telefone, datas (dd/mm/aaaa), horários (hh:mm).
- Interface deve seguir diretrizes de acessibilidade WCAG 2.2, ePWG e ISO/IEC 25010.
- Contrastes de cor adequados, fontes legíveis, vocabulário claro.

### Desempenho
- Navegação entre telas não deve ultrapassar 3 segundos.
- Geração de relatórios não deve ultrapassar 10 segundos.
- Sistema deve manter responsividade com muitos registros.

### Suportabilidade
- O sistema deve funcionar em Google Chrome (versões recentes).
- O sistema deve funcionar em Mozilla Firefox (versões recentes).
- O sistema deve funcionar em Safari (versões recentes).
- O sistema deve funcionar corretamente em dispositivos mobile.
- **O sistema deve funcionar de forma offline** com sincronização ao reconectar.

### Segurança
- O sistema deve ser seguro para uso empresarial.
- Deve possuir diferentes permissões por perfil de acesso.
- Registros de ponto devem ser imutáveis após confirmação.
- Alterações em dados devem ser rastreáveis (auditoria).
- Dados sensíveis (CPF, contato) devem ser protegidos.

### Confiabilidade
- Registros de ponto devem ser persistidos mesmo em caso de falha.
- Sincronização offline deve garantir integridade dos dados.

## Notas e Considerações
- **[REVISÃO PENDENTE]** Funcionalidade de escalas personalizada - solicitar detalhamento com cliente (Vilbs).
- Definir duração mínima de intervalo e máxima de jornada.
- Definir políticas de tolerância para atrasos.
- Validar se há integração necessária com sistema de folha de pagamento.
- Confirmar formato de assinatura digital com setor jurídico.


## Histórico de versão

|Nome| Data | Comentário|
|------ |------- |------|
|[Caio Sabino](github.com/caiomsabino) | 13/11/2025 | Adição e formatação dos textos presentes no docs. |