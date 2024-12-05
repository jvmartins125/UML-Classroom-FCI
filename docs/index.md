<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;Sistema de matriculas-Escola infinito&gt;*
</center></font>

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* joao victor martins
* andre kim


# Descrição do Projeto

*&lt;O projeto visa Desenvolver um sistema digital para gerenciar o controle de presenças dos alunos da Escola Infinito, substituindo o processo manual em papel. A aplicação deverá permitir o registro de faltas de maneira intuitiva, gerar relatórios de frequência detalhados e enviar notificações automáticas aos responsáveis em caso de excesso de faltas. Além disso, o sistema deve ser acessível a partir de dispositivos móveis e navegadores, garantindo uma experiência acessível para todos os usuários, incluindo aqueles com necessidades especiais.&gt;*

# Análise de Requisitos Funcionais e Não-Funcionais
*&lt;1. Caso de Uso Login 
Atores 
Usuário (professor, responsável, administrador) 
Fluxo Principal 
1. O sistema exibe os campos Usuário e Senha. Também exibe o link "Esqueci minha senha" e o 
botão "Entrar". 
2. O usuário preenche os campos e clica em "Entrar". 
3. O sistema verifica se o usuário e senha estão corretos. 
4. Se as credenciais forem válidas, o sistema exibe a Tela Inicial correspondente ao perfil do 
usuário (professor, responsável, administrador). 
Fluxos Alternativos 
1. O usuário clica em "Esqueci minha senha". 
○ O sistema executa o caso de uso "Esqueci minha Senha". 
2. Se o usuário digitar credenciais inválidas, o sistema exibe a seguinte mensagem de erro: 
“Usuário ou Senha inválido. Por favor, preencha os dados corretamente ou registre-se.” 
Requisitos Funcionais 
1. Autenticação de usuários com e-mail e senha. 
2. Validação de credenciais no banco de dados. 
3. Diferenciação de perfis de usuários (professores, pais, administradores), com permissões 
distintas. 
4. Exibir mensagens de erro específicas para credenciais inválidas ou ausentes. 
5. Permitir que o usuário utilize o recurso "Esqueci minha Senha" caso não se lembre das 
credenciais. 
6. Caso o login tenha sucesso, redirecionar o usuário para a Tela Inicial correspondente ao seu 
papel no sistema. 
Requisitos Não Funcionais
1. O sistema deve garantir criptografia das credenciais no momento do login. 
2. Interface responsiva e acessível para dispositivos móveis. 
3. Implementar mecanismo de timeout para logout automático após 12 horas de inatividade.
  
   2. Caso de Recuperação de Senha 
Atores 
Usuário (professor, responsável, administrador) 
Fluxo Principal 
1. O sistema exibe o campo "E-mail" e os botão "Enviar". 
2. O usuário preenche o campo "E-mail" e clica em "Enviar". 
3. O sistema verifica se o e-mail informado está registrado no banco de dados. 
4. Se o e-mail for válido, o sistema envia um link para redefinição de senha para o e-mail 
informado. 
5. O sistema exibe uma mensagem de sucesso: “Um link para redefinição de senha foi enviado 
para o seu e-mail. Por favor, verifique sua caixa de entrada.” 
Fluxos Alternativos 
● E-mail não registrado: 
Se o e-mail digitado não estiver cadastrado no sistema, o sistema exibe a seguinte mensagem 
de erro: “O e-mail informado não está registrado. Por favor, tente novamente com um e-mail 
válido ou entre em contato com o suporte.” 
Pós-Condições 
1. Se o e-mail estiver cadastrado, o sistema envia o link de redefinição de senha e exibe a 
mensagem de confirmação ao usuário. 
2. Se o e-mail não estiver cadastrado, o sistema informa ao usuário e permanece na tela 
"Esqueci minha Senha". 
Requisitos Funcionais 
1. Verificação se o e-mail informado está cadastrado no sistema. 
2. Envio de um link de redefinição de senha por e-mail. 
3. Exibir mensagens de sucesso ou erro após a verificação do e-mail. 
4. Oferecer a opção de retornar à tela de login sem alterar os dados preenchidos.
Requisitos Não Funcionais 
1. O sistema deve garantir que o link de redefinição de senha expire após 24 horas. 
2. O sistema deve garantir que o link enviado seja criptografado para garantir a segurança do 
usuário. 
3. Implementar controle de requisições para evitar tentativas excessivas de redefinição de 
senha (limitando a 5 tentativas por hora). 
3. Caso de Uso Cadastro de Professores 
Atores 
Administrador 
Fluxo Principal 
1. O administrador seleciona a opção "Cadastro de Professores". 
2. O sistema exibe um formulário para cadastro de professores, com campos como "Nome", 
"Disciplina", "E-mail" e "Telefone". 
3. O administrador preenche os campos obrigatórios e clica em "Salvar". 
4. O sistema valida as informações e, se corretas, salva o novo professor. 
5. O sistema exibe uma mensagem de sucesso e retorna à tela de lista de professores. 
Fluxos Alternativos 
● Se algum campo for preenchido incorretamente: 
1. O sistema exibe uma mensagem de erro, indicando os campos a serem corrigidos. 
2. O administrador corrige as informações e tenta novamente. 
● O administrador decide cancelar o cadastro: 
1. O administrador clica no botão "Cancelar". 
2. O sistema descarta as informações e retorna à Tela Inicial. 
Pós-Condições 
● Se o cadastro for bem-sucedido, o novo professor estará disponível para ser associado a uma 
turma. 
● Em caso de erro, o sistema exibe mensagens apropriadas para correção. 
Requisitos Funcionais 
● Permitir o cadastro de novos professores.● Validar os campos obrigatórios. 
● Exibir mensagens de erro específicas para entradas inválidas. 
● Permitir o cancelamento do cadastro. 
Requisitos Não Funcionais 
● Interface amigável e acessível em dispositivos móveis. 
● Garantir a integridade dos dados cadastrados. 4. Caso de Uso Cadastro de Alunos 
Atores 
Administrador 
Fluxo Principal 
1. O administrador acessa o sistema e escolhe a opção "Cadastro de Alunos". 
2. O sistema exibe um formulário com campos como "Nome", "Ano", "Turma" (se disponível), 
"Responsável", "E-mail do Responsável" e "Data de Nascimento". 
3. O administrador preenche os dados necessários e clica no botão "Salvar". 
4. O sistema valida os dados e, se corretos, salva o novo aluno no banco de dados. 
5. Uma mensagem de sucesso é exibida e o sistema retorna à lista de alunos cadastrados. 
Fluxos Alternativos 
● Caso algum campo seja preenchido incorretamente: 
1. O sistema exibe uma mensagem de erro apontando os erros. 
2. O administrador faz as correções e tenta novamente. 
● O administrador opta por cancelar: 
1. O administrador clica em "Cancelar". 
2. O sistema descarta os dados e retorna à Tela Inicial. 
Pós-Condições 
● Se o cadastro for bem-sucedido, o aluno estará disponível para ser associado a uma turma. 
● Em caso de erro, o sistema permitirá a correção dos dados antes de finalizar o cadastro. 
Requisitos Funcionais● Permitir o cadastro de novos alunos. 
● Validar os campos obrigatórios como nome, responsável e data de nascimento. 
● Exibir mensagens de erro adequadas para entradas inválidas. 
● Permitir o cancelamento da operação de cadastro. 
Requisitos Não Funcionais 
● Interface responsiva e de fácil utilização. 
● Garantir a segurança e integridade dos dados dos alunos. 
5 . Caso de Uso: Cadastro de Turmas com Associação de Alunos e 
Professores 
Atores 
Administrador 
Fluxo Principal 
1. O administrador faz login no sistema e acessa a Tela Inicial. 
2. O administrador seleciona a opção "Cadastro de Turmas". 
3. O sistema exibe um formulário para cadastro de turmas com os seguintes campos: "Nome da 
Turma", "Ano", "Turno", "Professor Principal", "Demais Professores" e "Alunos". 
4. O administrador preenche os campos obrigatórios, como "Nome da Turma" e "Ano". 
5. O administrador seleciona o "Professor Principal" e os "Demais Professores" a partir de uma 
lista de professores previamente cadastrados. 
6. O administrador seleciona os alunos a serem associados à turma a partir de uma lista de 
alunos cadastrados. 
7. O administrador clica no botão "Salvar". 
8. O sistema valida as informações, verificando se todos os campos obrigatórios foram 
preenchidos e se os professores e alunos selecionados estão devidamente cadastrados. 
9. Se os dados estiverem corretos, o sistema salva a nova turma e exibe uma mensagem de 
sucesso. 
10. O sistema retorna à tela de lista de turmas, mostrando a nova turma cadastrada com seus 
professores e alunos associados. 
Fluxos Alternativos 
● O administrador preenche algum campo de forma incorreta ou deixa algum campo 
obrigatório em branco: 
1. O sistema exibe uma mensagem de erro, indicando os campos que precisam ser 
corrigidos.2. O administrador corrige as informações e tenta novamente. 
● O administrador decide cancelar o cadastro: 
1. O administrador clica no botão "Cancelar". 
2. O sistema descarta as informações inseridas e retorna à Tela Inicial. 
Pós-Condições 
● Se o cadastro for bem-sucedido, a turma será criada e os professores e alunos selecionados 
estarão associados a ela. 
● Caso haja erro, o sistema permite correções antes de finalizar o cadastro. 
Requisitos Funcionais 
● Permitir o cadastro de novas turmas com a associação de professores (principal e demais) e 
alunos. 
● Validar os campos obrigatórios no cadastro de turmas, professores e alunos. 
● Exibir mensagens de erro específicas para entradas inválidas. 
● Permitir o cancelamento do cadastro sem perda de informações. 
Requisitos Não Funcionais 
● Interface amigável e responsiva para dispositivos móveis. 
● Garantir a integridade dos dados associados à turma (professores e alunos). 
● Otimizar a navegação e carregamento das listas de professores e alunos para seleção. 
6 . Caso de Uso: Cadastro de Pais/Responsáveis com Associação de Alunos 
Atores 
Administrador 
Fluxo Principal 
1. O administrador seleciona a opção "Cadastro de Pais/Responsáveis". 
2. O sistema exibe um formulário com os campos "Nome", "E-mail", "Telefone", e uma lista para 
selecionar os alunos associados. 
3. O administrador preenche os dados obrigatórios do responsável. 
4. O administrador seleciona um ou mais alunos para associar a esse responsável, a partir de 
uma lista de alunos cadastrados. 
5. O administrador clica no botão "Salvar".6. O sistema valida os dados inseridos e verifica a integridade da associação entre o responsável 
e os alunos (ex: um aluno pode estar associado a mais de um responsável). 
7. Se os dados forem válidos, o sistema salva o novo responsável e a associação com os alunos. 
8. O sistema exibe uma mensagem de sucesso e retorna à tela de lista de responsáveis. 
Fluxos Alternativos 
● O administrador preenche algum campo incorretamente ou deixa campos obrigatórios em 
branco: 
1. O sistema exibe uma mensagem de erro, indicando os campos que precisam ser 
corrigidos. 
2. O administrador corrige as informações e tenta novamente. 
● O administrador não encontra o aluno na lista: 
1. O sistema permite que o administrador pause o cadastro do responsável e vá 
cadastrar o aluno faltante. 
2. Após cadastrar o aluno, o administrador retorna ao cadastro do responsável. 
● O administrador decide cancelar o cadastro: 
1. O administrador clica em "Cancelar". 
2. O sistema descarta as informações e retorna à Tela Inicial. 
Pós-Condições 
● Se o cadastro for bem-sucedido, o responsável estará associado aos alunos selecionados, e 
essa associação será refletida no sistema para notificações, relatórios, e visualização de 
presença. 
● Caso haja erro, o sistema permite correções antes de finalizar o cadastro. 
Requisitos Funcionais 
● Permitir o cadastro de novos responsáveis com a associação a um ou mais alunos. 
● Validar a associação entre responsáveis e alunos, permitindo múltiplos responsáveis por 
aluno e múltiplos alunos por responsável. 
● Exibir mensagens de erro adequadas para entradas inválidas. 
● Permitir o cancelamento ou correção do cadastro sem perda de informações. 
Requisitos Não Funcionais 
● Interface responsiva e fácil de usar em dispositivos móveis. 
● Garantir a segurança e privacidade dos dados dos alunos e responsáveis. 
● Otimização da lista de alunos para seleção eficiente, especialmente em instituições com 
muitos alunos.&gt;*

# Diagrama de Atividades

*&lt;Diagrama para visualizer as pessoas das áreas de negócios e de desenvolvimento de uma organização para entender o processo e comportamento.&gt;*

# Diagrama de Casos de Uso

*&lt;Diagrama para visualizar o comportamento dos atores&gt;*

# Descrição dos Casos de Uso

*&lt;Descrição do comportamento entre os atores/resquisitos&gt;*

# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
