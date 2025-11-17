# Requisitos - Landing Page e Gestão de Turmas

## Visão Geral

Site web para apresentar profissionais de terapia, listar serviços oferecidos e gerenciar turmas de terapia com alunos. A plataforma deve ser atrativa, responsiva, otimizada para SEO básico e integrada com WhatsApp. Inclui CRUD para gestão de turmas com informações de alunos e contatos.

## Protótipo

Link para o protótipo no Figma: <a href="https://bead-fairy-29083975.figma.site" target="_blank">Protótipo Figma</a>

## Requisitos Funcionais

### 1. Landing Page / Cartão Digital

#### 1.1 Apresentação da Clínica

- O site deve exibir apresentação e informações das profissionais.
- O site deve listar os serviços oferecidos com descrição.
- O site deve exibir informações gerais dos atendimentos.

#### 1.2 Grupos Terapêuticos

- O site deve exibir descrição da metodologia dos grupos terapêuticos.

#### 1.3 Contato e Integração

- O site deve incluir link direto para WhatsApp.
- O link do WhatsApp deve abrir com mensagem padrão de interesse.
- O site deve incluir links para redes sociais.
- O site deve exibir formulário de contato do cliente(opcional).
- O site deve exibir endereço e telefone de contato.

#### 1.4 Design e Visual

- O design deve seguir paleta de cores: tons de verde e terra.
- O visual deve remeter a calma, natureza e contexto de saúde.
- O design deve ser coerente com identidade visual da clínica.
- O site deve ter visual limpo, acolhedor e profissional.

### 2. Site / Página de Vitrine

#### 2.1 Responsividade

- O site deve ser responsivo para celular.
- O site deve ser responsivo para computador/desktop.
- O site deve se adaptar a diferentes tamanhos de tela.

#### 2.2 SEO e Descoberta

- O site deve ser otimizado para mecanismo de busca (Google).
- O site deve conter meta tags descritivas.
- O site deve conter palavras-chave relevantes.
- O site deve ter tempo de carregamento otimizado.

#### 2.3 Manutenção

- **Sem necessidade de personalização pelo cliente final.**
- **Manutenção realizada pela equipe técnica.**

### 3. Integração WhatsApp

#### 3.1 Link e Mensagem

- O site deve gerar link direto para WhatsApp.
- O link deve abrir conversa com número cadastrado.
- O site deve enviar mensagem padrão de interesse automaticamente.
- A mensagem deve incluir contexto (qual serviço o interessado quer conhecer).

### 4. Gestão de Turmas

#### 4.1 CRUD de Turmas

- O sistema deve permitir criar nova turma com nome, horário, dias, descrição, informações de alunos e capacidade máxima de alunos permitidas.
- O sistema deve exibir lista de turmas cadastradas.
- O sistema deve permitir editar informações de turma.
- O sistema deve permitir deletar turma (com confirmação).

#### 4.2 CRUD de Alunos

- O sistema deve permitir adicionar novo aluno com nome completo, data de nascimento, descrição, nome do parente, contato do parente.
- O sistema deve permitir visualizar os alunos cadastrados.
- O sistema deve permitir atulizar cadastro de aluno.
- O sistema deve permitir deletar um aluno.

#### 4.3 Gestão de Alunos na Turma

- O sistema deve permitir adicionar aluno à turma.
- O sistema deve permitir remover aluno da turma.
- O sistema deve exibir lista de alunos de uma turma.
- O sistema deve permitir editar informações de aluno.

### 5. Funcionalidades Futuras (Possível Expansão)

- Cadastro de crianças com histórico de atendimento.
- CRUD completo de turmas com mais configurações.
- site de agendamento/presença.
- Chatbot com novos clientes.
- Comunicação automatizada com responsáveis.
- Portal para responsáveis acompanharem progresso.

## Requisitos Não Funcionais

### Usabilidade

- Interface intuitiva e de fácil navegação.
- Formulários com máscara de telefone (opcional).
- Funcionalidades devem ser acessíveis em até 3 cliques.
- Design responsivo para todos os tamanhos de tela.

### Desempenho

- O site deve carregar em menos de 3 segundos.
- Navegação entre páginas deve ser fluida e rápida.

### Suportabilidade

- O site deve funcionar em Google Chrome (versões recentes).
- O site deve funcionar em Mozilla Firefox (versões recentes).
- O site deve funcionar em Safari (versões recentes).
- O site deve funcionar em dispositivos mobile (smartphones e tablets).

### Segurança

- Dados de alunos e responsáveis devem ser protegidos.
- Acesso à gestão de turmas deve ser restrito (autenticação).
- Apenas usuários autorizados podem editar turmas e alunos.

### Acessibilidade

- O site deve seguir boas práticas de contraste e legibilidade.
- O site deve ser navegável por teclado.
- O site deve ser compatível com leitores de tela.

## Notas e Considerações

- **Paleta de cores:** Definir tom específico de verde e terra com cliente (buscar referências).
- **Logo:** A ver com cliente se vai desenvolver.
- **Metodologia:** A seção de metodologia será avaliada em reunião com cliente.
- **Nomenclatura:** Confirmar termo para "diagnóstico/doença" a ser usado no site.
- **Expansões futuras:** Priorizar com cliente antes de implementação.
- **Integração WhatsApp:** Utilizar API do WhatsApp Business (opcional) ou link simples para WhatsApp Web.

## Histórico de versão

| Nome                                  | Data       | Comentário                                        |
| ------------------------------------- | ---------- | ------------------------------------------------- |
| [Caio Sabino](github.com/caiomsabino) | 13/11/2025 | Adição e formatação dos textos presentes no docs. |
