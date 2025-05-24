Estudo de Caso APS
Projeto EduGestor
Introdução
O sistema EduGestor é uma plataforma desenvolvida para aprimorar e facilitar a gestão da educação no ambiente universitário. Seu principal objetivo é oferecer maior eficiência no controle de notas, trabalhos e frequência dos alunos, além de apoiar a administração de atividades acadêmicas como o projeto final de curso e o estágio supervisionado.
A plataforma conta com processos bem estruturados para cadastro, seleção e gerenciamento de rotinas típicas de um ambiente educacional organizado, contribuindo para uma administração mais ágil, eficaz e integrada.
Sumário
Requisitos Funcionais
Cadastro de Usuários: O sistema deve permitir o cadastro de usuários com diferentes perfis: aluno e professor.
Autenticação e Login: Deve possibilitar que os usuários realizem login com suas credenciais, garantindo segurança e individualidade no uso.
Submissão de Candidatura (Fase: Candidato): Alunos devem poder se candidatar a vagas de monitoria ou estágio por meio do preenchimento de um formulário com informações pessoais, acadêmicas e justificativa de interesse.
Avaliação de Candidatura: Professores poderão visualizar e avaliar essas candidaturas, aprovando ou rejeitando cada uma conforme os critérios estabelecidos.
Acompanhamento de Execução (Fase: Executor): Uma vez aprovados, os alunos entram na fase de execução, durante a qual poderão registrar suas atividades periódicas no sistema.
Supervisão de Atividades: Os professores poderão acompanhar as atividades registradas, comentá-las, aprová-las ou solicitar ajustes.
Submissão de Relatório Final (Fase: Relatório): Ao final do período de atividade, o aluno deverá enviar um relatório final, detalhando as tarefas realizadas e os resultados alcançados.
Avaliação de Relatório Final: O professor responsável poderá avaliar o relatório, atribuir um parecer (aprovado, reprovado ou com necessidade de correções) e registrar um feedback.
Histórico de Participação: O sistema manterá um histórico completo da participação do aluno, incluindo candidaturas, execuções e relatórios, acessível tanto ao próprio aluno quanto aos professores.
Notificações: O sistema enviará notificações sobre atualizações importantes, como aprovação de candidaturas ou avaliação de relatórios.
Geração de Documentos: O sistema deve possibilitar a geração automática de documentos como declarações de participação, comprovantes de atividade e relatórios formatados.

Requisitos Não-Funcionais
Desempenho: O sistema deve ser capaz de responder às solicitações dos usuários em até 2 segundos, mesmo com múltiplos acessos simultâneos.
Escalabilidade: A aplicação deve ser escalável, permitindo o aumento de capacidade conforme o número de usuários cresce, sem perda de desempenho.
Segurança: O sistema deve garantir a proteção dos dados dos usuários através de criptografia de senhas e conexões seguras (HTTPS), além de autenticação por sessão.
Disponibilidade: O sistema deve estar disponível para acesso online 99,5% do tempo, exceto em janelas programadas de manutenção.
Usabilidade: A interface deve ser intuitiva, responsiva e acessível, com uma navegação simples tanto em dispositivos móveis quanto em computadores.
Compatibilidade: O sistema deve funcionar corretamente nos principais navegadores modernos (Chrome, Firefox, Edge e Safari).
Backup e Recuperação: Deve ser realizado backup automático dos dados diariamente, com possibilidade de recuperação em caso de falhas ou perdas acidentais.
Manutenibilidade: O sistema deve ser modular, com código-fonte bem documentado, facilitando futuras manutenções, correções ou evoluções.
Auditabilidade: Todas as ações relevantes (como submissões, aprovações e alterações de dados) devem ser registradas em logs para fins de auditoria.
Conformidade com LGPD: O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD), garantindo o direito dos usuários à privacidade e ao controle de seus dados pessoais.
Código dos Requisitos Não Funcionais
NF001. O cadastro no banco de dados deve ser realizada em menos de 2 segundos.
NF002. O sistema deve ser acessível em dispositivos móveis e desktops.
NF003. A consulta no banco de dados tem que ser feito em menos de 10 segundos.
NF004. O sistema deve mascarar a senha ao exibi-la.
NF005. As alterações devem ser registradas com data, hora e ID do usuário para auditoria.
NF006. A interface deve ser responsiva para uso em dispositivos móveis.
NF007. A candidatura deve ser registrada com data, hora e identificador único.
NF008. O sistema deve enviar notificação automática para o professor responsável.
NF009. A interface do formulário deve ser responsiva e acessível.
NF010. O sistema deve garantir que apenas usuários autenticados e com permissão possam avaliar candidaturas.
NF011. O sistema deve registrar logs de todas as ações de avaliação para auditoria.
NF012. O sistema deve prevenir ações simultâneas conflitantes sobre a mesma candidatura.
NF013. Em caso de falha durante a operação, o sistema deve registrar o erro e permitir nova tentativa sem duplicar a ação.
