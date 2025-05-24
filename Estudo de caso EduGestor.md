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

Atores
Usuário:Qualquer ator que ainda não se logou no sistema.

Candidato: Aluno que se inscreve para uma vaga de monitoria ou estágio.

Executor: Aluno aprovado, que está desempenhando as atividades da vaga.

Relator: Aluno que está finalizando sua participação e submetendo o relatório final.

Professor:Avaliar candidaturas; acompanhar a execução das atividades dos alunos; avaliar relatórios finais; fornecer feedbacks e aprovações.
Regras de Negócio
RN001. Apenas usuários não logados podem tentar realizar o cadastro.
RN002. Apenas usuários não logados podem tentar realizar o login. 
RN003. Apenas usuários já cadastrados podem se logar. 
RN004. O campo de e-mail deve ser único por usuário. 
RN005. A senha deve conter no mínimo 8 caracteres e incluir letras e números.
RN006. Apenas o próprio usuário pode editar seu perfil.
RN007. Cada aluno pode se candidatar a no máximo uma vaga por tipo (monitoria ou estágio) simultaneamente. 
RN008. A justificativa deve conter no mínimo 200 caracteres.
RN009. O sistema deve verificar se o aluno está em situação acadêmica regular.
RN010. Cada candidatura deve ser avaliada por pelo menos um membro da comissão. 
RN011. Não é possível avaliar uma candidatura duas vezes pelo mesmo avaliador.
RN012. Uma vez que a avaliação é finalizada, não pode ser alterada (exceto por administradores). 
RN013. Uma candidatura só pode ser avaliada uma vez, a menos que o sistema permita reavaliações com justificativa.
RN014. A aprovação de uma candidatura pode implicar em bloqueio de outras para a mesma vaga (dependendo do processo seletivo).
RN015. A rejeição deve ser registrada com motivo, caso exigido pela política da empresa.


Mensagens de Erro
ME101. Os dados digitados já foram utilizados no cadastro do sistema.
ME102. Erro ao acessar informação, confira conexão com a internet.
ME103. Erro ao logar no sistema,usuário não cadastrado.  
ME104. Campos incorretos. 
ME105. Erro,e-mail já está em uso. 
ME106. Erro de comunicação com o banco, tente novamente mais tarde. 
ME107. Campos inválidos ou não preenchidos. 
ME108. A decisão já foi tomada. 
ME109. Erro ao atualizar status.



Diagrama dos Casos de Uso



























































Especificações dos Casos de Uso


Atores
Usuário:Qualquer ator que ainda não se logou no sistema.

Candidato: Aluno que se inscreve para uma vaga de monitoria ou estágio.

Executor: Aluno aprovado, que está desempenhando as atividades da vaga.

Relator: Aluno que está finalizando sua participação e submetendo o relatório final.

Professor:Avaliar candidaturas; acompanhar a execução das atividades dos alunos; avaliar relatórios finais; fornecer feedbacks e aprovações.
Regras de Negócio
RN001. Apenas usuários não logados podem tentar realizar o cadastro.
RN002. Apenas usuários não logados podem tentar realizar o login. 
RN003. Apenas usuários já cadastrados podem se logar. 
RN004. O campo de e-mail deve ser único por usuário. 
RN005. A senha deve conter no mínimo 8 caracteres e incluir letras e números.
RN006. Apenas o próprio usuário pode editar seu perfil.
RN007. Cada aluno pode se candidatar a no máximo uma vaga por tipo (monitoria ou estágio) simultaneamente. 
RN008. A justificativa deve conter no mínimo 200 caracteres.
RN009. O sistema deve verificar se o aluno está em situação acadêmica regular.
RN010. Cada candidatura deve ser avaliada por pelo menos um membro da comissão. 
RN011. Não é possível avaliar uma candidatura duas vezes pelo mesmo avaliador.
RN012. Uma vez que a avaliação é finalizada, não pode ser alterada (exceto por administradores). 
RN013. Uma candidatura só pode ser avaliada uma vez, a menos que o sistema permita reavaliações com justificativa.
RN014. A aprovação de uma candidatura pode implicar em bloqueio de outras para a mesma vaga (dependendo do processo seletivo).
RN015. A rejeição deve ser registrada com motivo, caso exigido pela política da empresa.


Mensagens de Erro
ME101. Os dados digitados já foram utilizados no cadastro do sistema.
ME102. Erro ao acessar informação, confira conexão com a internet.
ME103. Erro ao logar no sistema,usuário não cadastrado.  
ME104. Campos incorretos. 
ME105. Erro,e-mail já está em uso. 
ME106. Erro de comunicação com o banco, tente novamente mais tarde. 
ME107. Campos inválidos ou não preenchidos. 
ME108. A decisão já foi tomada. 
ME109. Erro ao atualizar status.



Diagrama dos Casos de Uso



























































Especificações dos Casos de Uso

Atores
Usuário:Qualquer ator que ainda não se logou no sistema.

Candidato: Aluno que se inscreve para uma vaga de monitoria ou estágio.

Executor: Aluno aprovado, que está desempenhando as atividades da vaga.

Relator: Aluno que está finalizando sua participação e submetendo o relatório final.

Professor:Avaliar candidaturas; acompanhar a execução das atividades dos alunos; avaliar relatórios finais; fornecer feedbacks e aprovações.
Regras de Negócio
RN001. Apenas usuários não logados podem tentar realizar o cadastro.
RN002. Apenas usuários não logados podem tentar realizar o login. 
RN003. Apenas usuários já cadastrados podem se logar. 
RN004. O campo de e-mail deve ser único por usuário. 
RN005. A senha deve conter no mínimo 8 caracteres e incluir letras e números.
RN006. Apenas o próprio usuário pode editar seu perfil.
RN007. Cada aluno pode se candidatar a no máximo uma vaga por tipo (monitoria ou estágio) simultaneamente. 
RN008. A justificativa deve conter no mínimo 200 caracteres.
RN009. O sistema deve verificar se o aluno está em situação acadêmica regular.
RN010. Cada candidatura deve ser avaliada por pelo menos um membro da comissão. 
RN011. Não é possível avaliar uma candidatura duas vezes pelo mesmo avaliador.
RN012. Uma vez que a avaliação é finalizada, não pode ser alterada (exceto por administradores). 
RN013. Uma candidatura só pode ser avaliada uma vez, a menos que o sistema permita reavaliações com justificativa.
RN014. A aprovação de uma candidatura pode implicar em bloqueio de outras para a mesma vaga (dependendo do processo seletivo).
RN015. A rejeição deve ser registrada com motivo, caso exigido pela política da empresa.


Mensagens de Erro
ME101. Os dados digitados já foram utilizados no cadastro do sistema.
ME102. Erro ao acessar informação, confira conexão com a internet.
ME103. Erro ao logar no sistema,usuário não cadastrado.  
ME104. Campos incorretos. 
ME105. Erro,e-mail já está em uso. 
ME106. Erro de comunicação com o banco, tente novamente mais tarde. 
ME107. Campos inválidos ou não preenchidos. 
ME108. A decisão já foi tomada. 
ME109. Erro ao atualizar status.



Diagrama dos Casos de Uso



























































Especificações dos Casos de Uso











UPE – Universidade de Pernambuco






UC001
Cadastrar Usuário
EduGestor
V0.1






































Especificação de Caso de Uso Cadastrar Usuário
Versão 0.1



Histórico de Revisões

Data
Versão
Descrição
Autor
19/05/25
0.1
Versão inicial
Erasmo























































Índice
Cadastrar Usuário	4
Atores	4
Pré-Condições	4
Fluxo de Eventos	4
Fluxo Básico	4
Fluxos Alternativos	4
A1 Usuário não consegue se cadastrar no sistema.	4
Exceções	4
E1 Usuário já cadastrado no sistema.	4
E2 Sem conexão com à internet.	4
Pós-Condições	4
Requisitos Não Funcionais	5
Regras de Negócio	5



































Especificação de Caso de Uso


Cadastrar Usuário
Breve Descrição
Este caso de uso permite que o ator se cadastre na plataforma e depois informe o tipo de usuário que é.
Atores
Primário:Usuário não logado no sistema.
Pré-Condições
Usuário não estar logado no sistema.
Fluxo de Eventos
Este caso de uso é iniciado quando o ator deseja realizar o seu cadastro no sistema
Fluxo Básico
(P1) O ator acessa o sistema EduGestor pela primeira vez.
(P2) O sistema exibe a tela de cadastro com a lista de tipos de atores disponíveis.
(P3) O ator realiza o seu cadastro e seleciona o tipo de ator que ele irá desempenhar no sistema.
(P4) O sistema confirma que o usuário foi cadastrado.
(P5) O caso de uso é encerrado.

Fluxos Alternativos
A1 Usuário não consegue se cadastrar no sistema
Condição: Para ocorrer no passo P3 do fluxo básico, caso o ator do sistema tente se cadastrar no sistema, mas por algum motivo não é autorizado.
A1.1 O ator tenta se cadastrar na plataforma usando os dados já utilizados anteriormente.
A1.2 O sistema informa ao usuário. [E1](Caso o usuário já seja cadastrado)[E2](caso o usuário não tenha conexão com a internet)
A1.3 O caso de uso retorna para o passo P4.

Exceções
E1 Usuário já cadastrado.
	E1.1 O sistema exibe uma mensagem ME101[“Os dados digitados já foram utilizados no cadastro do sistema”]


E2 Sem conexão à internet.
Condição: Pode ocorrer no passo A1.2 do fluxo alternativo A1 caso o ator não tenha os dados salvos localmente e não tenha acesso à internet.
E2.1 O sistema exibe uma mensagem ME102 [“Erro ao acessar informação, confira conexão com a internet.”]
E2.2 O sistema retorna para o passo A1.2 do fluxo alternativo (A1)
Pós-Condições
N/A.

Requisitos Não Funcionais
NF001. O cadastro no banco de dados deve ser realizada em menos de 2 segundos.
NF002. O sistema deve ser acessível em dispositivos móveis e desktops.

Regras de Negócio
RN001. Apenas usuários não logados podem tentar realizar o cadastro.






















































UPE – Universidade de Pernambuco






UC002
Fazer login no sistema
EduGestor
V0.1






































Especificação de Caso de Uso Fazer login no sistema
Versão 0.1



Histórico de Revisões

Data
Versão
Descrição
Autor
19/05/25
0.1
Versão inicial
Erasmo






















































Índice
Fazer login no sistema	4
Atores	4
Pré-Condições	4
Fluxo de Eventos	4
Fluxo Básico	4
Fluxos Alternativos	4
A1 Usuário não consegue se logar no sistema.	4
Exceções	4
E1 Usuário não cadastrado no sistema.	4
E2 Sem conexão com a internet.	4
E3 Usuário ou senha incorretas 	4
Pós-Condições	4
Requisitos Não Funcionais	5
Regras de Negócio	5
































Especificação de Caso de Uso


Fazer login no sistema
Breve Descrição
Este caso de uso permite que o ator se logar na plataforma,fazendo uso das suas credenciais..
Atores
Primário:Usuário não logado no sistema.
Pré-Condições
Usuário não estar logado no sistema.
Fluxo de Eventos
Este caso de uso é iniciado quando o ator deseja realizar o seu login no sistema
Fluxo Básico
(P1) O ator acessa o sistema EduGestor.
(P2) O sistema exibe a tela de login para o usuário.
(P3) O ator realiza o seu login fazendo uso do seu usuário e senha.
(P4) O sistema confirma que o usuário foi logado.
(P5) O caso de uso é encerrado.

Fluxos Alternativos
A1 Usuário não consegue se cadastrar no sistema
Condição: Para ocorrer no passo P3 do fluxo básico, caso o ator do sistema tente se cadastrar no sistema, mas por algum motivo não é autorizado.
A1.1 O ator tenta se cadastrar na plataforma usando os dados já utilizados anteriormente.
A1.2 O sistema informa ao usuário. [E1](Caso o usuário já seja cadastrado)[E2](caso o usuário não tenha conexão com a internet)
A1.3 O caso de uso retorna para o passo P2.

Exceções
E1 Usuário não cadastrado.
	E1.1 O sistema exibe uma mensagem ME103[“Usuário não cadastrado no sistema. ”]
            E1.2 O sistema retorna ao passo P2.

E2 Sem conexão à internet.
Condição: Pode ocorrer no passo A1.2 do fluxo alternativo A1 caso o ator não tenha os dados salvos localmente e não tenha acesso à internet.
E2.1 O sistema exibe uma mensagem ME102 [“Erro ao acessar informação, confira conexão com a internet.”]
E2.2 O sistema retorna para o passo A1.2 do fluxo alternativo (A1)

E3 Usuário ou senha incorretos.
	E1.1 O sistema exibe uma mensagem ME105[“Usuário ou senha incorretos.”]
	E1.2 O sistema retorna ao passo P2.
Pós-Condições
N/A.

Requisitos Não Funcionais
NF003. A consulta no banco de dados tem que ser feito em menos de 10 segundos.

Regras de Negócio
	  RN002. Apenas usuários não logados podem tentar realizar o login. 
RN003. Apenas usuários já cadastrados podem se logar.



















































UPE – Universidade de Pernambuco






UC003
Editar perfil do usuário
EduGestor
V0.1




































































Especificação de Caso de Uso Editar perfil do  usuário
Versão 0.1



Histórico de Revisões

Data
Versão
Descrição
Autor
20/05/25
0.1
Versão inicial
Erasmo
















































Índice
Editar perfil do usuário	4
Atores	4
Pré-Condições	4
Fluxo de Eventos	4
Fluxo Básico	4
Fluxos Alternativos	4
A1 Usuário não consegue atualizar o seu perfil	4
Exceções	4
E1 Campos inválidos ou incompletos	4
E2 Tentativa de salvar e-mail já existente (duplicado)	4
E3 Erro de conexão com banco de dados	4
Pós-Condições	4
Requisitos Não Funcionais	5
Regras de Negócio	5
































Especificação de Caso de Uso


Fazer login no sistema
Breve Descrição
Permite ao usuário alterar suas informações cadastrais, como nome, e-mail, senha e dados complementares, conforme o perfil.
Atores
Primário: Usuário (Aluno ou Professor).
Pré-Condições
O usuário deve estar autenticado (logado) no sistema.
O sistema deve estar disponível.
Fluxo de Eventos
Este caso de uso é iniciado quando o ator deseja atualizar o seu perfil no sistema.
Fluxo Básico
(P1) O usuário acessa sua conta e seleciona a opção "Editar Perfil".


(P2) O sistema exibe um formulário com os dados atuais do perfil.


(P3) O usuário altera as informações desejadas.


(P4) O usuário clica no botão "Salvar alterações".


(P5) O sistema valida os dados inseridos.


(P6) O sistema atualiza os dados no banco.


(P7) O sistema exibe a mensagem "Perfil atualizado com sucesso".

Fluxos Alternativos
A1 Usuário não consegue atualizar o seu perfil
Condição: Para ocorrer no passo P3 do fluxo básico, caso o ator do sistema tenta atualizar o seu perfil, mas por algum motivo não é autorizado.
A1.1 O ator tenta atualizar os dados na página.
A1.2 O sistema informa ao usuário. [E1](Campos inválidos ou incompletos)[E2](Tentativa de salvar e-mail já existente(duplicado)[E3](Erro de conexão com o banco de dados))
A1.3 O caso de uso retorna para o passo P3.

Exceções
E1 Campos inválidos ou incompletos.
	E1.1 O sistema exibe uma mensagem ME104[“Campos incorretos.”] e impede o salvamento até que os dados sejam corrigidos.

E2 Tentativa de salvar e-mail já existente (duplicado):
E2.1  O sistema informa ME105[“Erro,e-mail já está em uso.”]  que o e-mail já está em uso e solicita a escolha de outro.

E3 Erro de conexão com o banco de dados:
	E3.1 O sistema exibe uma mensagem de erro ME107[“Erro de comunicação com o banco, tente novamente mais tarde.”] e orienta o usuário a tentar novamente mais tarde.
em.


Pós-Condições
Os dados atualizados são salvos com sucesso no banco de dados.
O sistema exibe uma mensagem de confirmação.
O log da alteração é registrado para fins de auditoria.

Requisitos Não Funcionais
NF004. O sistema deve mascarar a senha ao exibi-la.
NF005. As alterações devem ser registradas com data, hora e ID do usuário para auditoria.
NF006. A interface deve ser responsiva para uso em dispositivos móveis.

Regras de Negócio
	  RN004. O campo de e-mail deve ser único por usuário. 
RN005. A senha deve conter no mínimo 8 caracteres e incluir letras e números.
  RN006. Apenas o próprio usuário pode editar seu perfil.











UPE – Universidade de Pernambuco






UC004
Submeter candidatura para vaga de estágio ou monitoria
EduGestor
V0.1



































































Especificação de Caso de Uso 
Submeter candidatura para vaga de estágio ou monitoria
Versão 0.1



Histórico de Revisões

Data
Versão
Descrição
Autor
21/05/25
0.1
Versão inicial
Erasmo












































Índice
Submeter candidatura para vaga de estágio ou monitoria	4
Atores	4
Pré-Condições	4
Fluxo de Eventos	4
Fluxo Básico	4
Fluxos Alternativos	4
A1 Usuário não consegue submeter a candidatura	4
Exceções	4
E1 Campos obrigatórios não preenchidos ou inválidos.	4
E2 Aluno já possui candidatura ativa para a mesma vaga.	4
E3 Prazo para candidaturas encerrado.	4
Pós-Condições	4
Requisitos Não Funcionais	5
Regras de Negócio	5
































Especificação de Caso de Uso


Fazer login no sistema
Breve Descrição
Permite que o aluno se candidate a uma vaga de estágio ou monitoria disponível no sistema, preenchendo um formulário com dados pessoais, acadêmicos e justificativa de interesse.
Atores
Primário: Aluno
Pré-Condições
O aluno deve estar autenticado no sistema.
Deve haver pelo menos uma vaga aberta disponível para candidatura.
O prazo para envio de candidaturas deve estar vigente.
Fluxo de Eventos
Este caso de uso é iniciado quando o ator deseja atualizar o seu perfil no sistema.
Fluxo Básico

(P1) O aluno acessa a área de vagas disponíveis.


(P2) O sistema exibe uma lista com as vagas abertas.


(P3) O aluno seleciona uma vaga desejada.


(P4) O sistema exibe um formulário de candidatura.


(P5) O aluno preenche os campos obrigatórios (ex: semestre atual, disciplinas cursadas, justificativa).


(P6) O aluno clica em "Enviar candidatura".


(P7) O sistema valida os dados e registra a candidatura.


(P8) O sistema exibe uma mensagem de sucesso e envia uma notificação ao professor responsável.


Fluxos Alternativos
A1 Usuário não consegue submeter a candidatura
Condição: Para ocorrer no passo P6 do fluxo básico, caso o ator do sistema tente submeter a candidatura do seu perfil, mas por algum motivo não é autorizado.
A1.1 O ator tenta se candidatar a candidatura para vaga de estágio ou monitoria.
A1.2 O sistema informa ao usuário. [E1](Campos obrigatórios não preenchidos ou inválidos)[E2](Aluno já possui candidatura ativa para a mesma vaga)[E3](Prazo para candidaturas encerrado))
A1.3 O caso de uso retorna para o passo P5.

Exceções
E1 Campos obrigatórios não preenchidos ou inválidos.
	E1.1 O sistema exibe uma mensagem ME108[“Campos inválidos ou não preenchidos.”] o sistema destaca os campos em erro e impede o envio até correção.
E1.2 O sistema retorna para o ponto A1.3.

E2 Aluno já possui candidatura ativa para a mesma vaga:
E2.1  O sistema bloqueia a ação e informa ME109[“Erro,só é permitido uma cadidatura por vaga.”] que apenas uma candidatura por vaga é permitida.
  E2.2 O sistema retorna para o ponto A1.3.

E3 Prazo para candidaturas encerrado:
	E3.1 O sistema informa ME110[“A vaga não está aceitando mais incrições”] que a vaga não está mais aceitando inscrições.
E3.2 O sistema retorna para o ponto A1.3.


Pós-Condições

A candidatura é registrada no sistema e marcada como "Pendente de Avaliação".
O professor responsável pela vaga é notificado da nova candidatura.
A candidatura fica visível no histórico do aluno.

Requisitos Não Funcionais
NF007. A candidatura deve ser registrada com data, hora e identificador único.
NF008. O sistema deve enviar notificação automática para o professor responsável.
NF009. A interface do formulário deve ser responsiva e acessível.

Regras de Negócio
	  RN007. Cada aluno pode se candidatar a no máximo uma vaga por tipo (monitoria ou estágio) simultaneamente. 
RN008. A justificativa deve conter no mínimo 200 caracteres.
  RN009. O sistema deve verificar se o aluno está em situação acadêmica regular.
































UPE – Universidade de Pernambuco






UC005
Avaliar candidatura de aluno
EduGestor
V0.1












































































Especificação de Caso de Uso 
Avaliar Candidatura de Aluno
Versão 0.1



Histórico de Revisões

Data
Versão
Descrição
Autor
23/05/25
0.1
Versão inicial
Erasmo














































Índice
Avaliar Candidatura de Aluno	4
Atores	4
Pré-Condições	4
Fluxo de Eventos	4
Fluxo Básico	4
Fluxos Alternativos	4
A1 O avaliador não termina a avaliação.	4
Exceções	4
E1 Documentação Incompleta.	4
E2 Avaliador decide salvar rascunho da avaliação.	4
Pós-Condições	4
Requisitos Não Funcionais	5
Regras de Negócio	5
































Especificação de Caso de Uso


Fazer login no sistema
Breve Descrição
Este caso de uso descreve o processo pelo qual o coordenador ou avaliador designado analisa e avalia a candidatura de um aluno para um curso ou programa, com base nos critérios previamente definidos (ex: histórico escolar, documentos, carta de motivação, etc).
Atores
Primário: Professor
Pré-Condições
O aluno já deve ter submetido sua candidatura no sistema.


O coordenador ou avaliador deve estar autenticado no sistema.
Fluxo de Eventos
Este caso de uso é iniciado após o aluno ter enviado uma candidatura para o sistema.
Fluxo Básico

(P1) O avaliador acessa o sistema e faz login.


(P2) O sistema autentica o usuário e apresenta o painel de avaliação.


(P3) O avaliador seleciona uma candidatura pendente da lista.


(P4) O sistema exibe os dados completos do candidato (documentos, notas, histórico etc.).


(P5) O avaliador analisa as informações e atribui um parecer: Deferido ou Indeferido.


(P6) O avaliador pode adicionar comentários justificando a decisão.


(P7) O avaliador confirma a avaliação.


(P8) O sistema salva o resultado da avaliação e registra a data e o avaliador responsável.


(P9) O sistema atualiza o status da candidatura para "Avaliada".


Fluxos Alternativos
A1 O avaliador não termina a avaliação 
Condição: Para ocorrer no passo P4 do fluxo básico, caso o ator do sistema tenta validar a avaliação, mas por algum motivo não é finalizada.
A1.1 O ator tenta avaliar a candidatura do aluno.
A1.2 O sistema informa ao usuário. [E1](Documentação Incompleta)[E2](Avaliador decide salvar rascunho da avaliação)
A1.3 O caso de uso retorna para o passo P6.

Exceções
E1 Documentação Incompleta.
	Condição: Se o avaliador perceber que faltam documentos.
	E1.1 Ele marca a candidatura como "Documentação Incompleta".
E1.2 O sistema envia notificação ao aluno solicitando os documentos faltantes.
E1.3 A candidatura permanece em "Pendente" até regularização.


E2 Avaliador decide salvar rascunho da avaliação:
E2.1  O avaliador pode optar por salvar a avaliação como rascunho, sem enviar o parecer final.
E2.2. O sistema armazena o rascunho para posterior edição.




Pós-Condições

A candidatura é marcada como “Avaliada” com o resultado da análise (deferida ou indeferida).


O aluno pode ser notificado do resultado, dependendo do fluxo do processo seletivo.

Requisitos Não Funcionais

NF010. O sistema deve garantir que apenas usuários autenticados e com permissão possam avaliar candidaturas.
NF011. O sistema deve registrar logs de todas as ações de avaliação para auditoria.




Regras de Negócio
	  RN010. Cada candidatura deve ser avaliada por pelo menos um membro da comissão. 
RN011. Não é possível avaliar uma candidatura duas vezes pelo mesmo avaliador.
  RN012. Uma vez que a avaliação é finalizada, não pode ser alterada (exceto por administradores).













UPE – Universidade de Pernambuco






UC006
Aprovar ou rejeitar candidatura
EduGestor
V0.1





































Especificação de Caso de Uso Aprovar ou rejeitar candidatura
Versão 0.1



Histórico de Revisões

Data
Versão
Descrição
Autor
24/05/25
0.1
Versão inicial
Erasmo























































Índice
  Aprovar ou rejeitar candidatura	4
Atores	4
Pré-Condições	4
Fluxo de Eventos	4
Fluxo Básico	4
Fluxos Alternativos	4
A1 Usuário não consegue aprovar ou rejeitar candidatura	4
Exceções	4
E1 Candidatura já avaliada	4
E2 Falha de comunicação ou erro do sistema	4
Pós-Condições	4
Requisitos Não Funcionais	5
Regras de Negócio	5



































Especificação de Caso de Uso


Cadastrar Usuário
Breve Descrição
Este caso de uso descreve o processo pelo qual um administrador ou recrutador avalia uma candidatura recebida para uma vaga e toma a decisão de aprová-la ou rejeitá-la.


Atores
Primário:Administrador (ou Recrutador).
Pré-Condições
O administrador está autenticado no sistema.


Existem candidaturas pendentes associadas a uma vaga.
Fluxo de Eventos
Este caso de uso é iniciado quando o ator deseja realizar o seu cadastro no sistema
Fluxo Básico
     (P1) O administrador acessa o sistema.


(P2) O sistema exibe a lista de candidaturas pendentes.


(P3) O administrador seleciona uma candidatura para análise.


(P4) O sistema exibe os detalhes da candidatura (currículo, carta de apresentação, etc.).


(P5) O administrador clica em “Aprovar” ou “Rejeitar”.


(P6) O sistema atualiza o status da candidatura de acordo com a decisão.


(P7) O sistema confirma a ação ao administrador.



Fluxos Alternativos
A1 Usuário não consegue aprovar ou rejeitar candidatura
Condição: Para ocorrer no passo P5 do fluxo básico, caso o ator do sistema tente clicar em “Aprovar” ou “Rejeitar”, mas por algum motivo não é autorizado.
A1.1 O ator tenta aprovar ou rejeitar a candidatura.
A1.2 O sistema informa ao usuário. [E1](Candidatura já avaliada)[E2]( Falha de comunicação ou erro do sistema)
A1.3 O caso de uso retorna para o passo P4.

Exceções
E1 Candidatura já avaliada
	E1.1 Se o status da candidatura já for "Aprovada" ou "Rejeitada", o sistema exibe uma mensagem. ME108[“A decisão já foi tomada”]


E2  Falha de comunicação ou erro do sistema
E2.1 Se ocorrer uma falha na atualização do status, o sistema informa o erro ao administrador.ME109 [“Erro ao atualizar status”]
E2.2 A decisão não é registrada e o administrador pode tentar novamente.
Pós-Condições
A candidatura será marcada como "Aprovada" ou "Rejeitada".


O candidato será notificado da decisão, se aplicável.
Requisitos Não Funcionais
NF012. O sistema deve prevenir ações simultâneas conflitantes sobre a mesma candidatura.
NF013. Em caso de falha durante a operação, o sistema deve registrar o erro e permitir nova tentativa sem duplicar a ação.

Regras de Negócio
RN013. Uma candidatura só pode ser avaliada uma vez, a menos que o sistema permita reavaliações com justificativa.
RN014. A aprovação de uma candidatura pode implicar em bloqueio de outras para a mesma vaga (dependendo do processo seletivo).
RN015. A rejeição deve ser registrada com motivo, caso exigido pela política da empresa.











