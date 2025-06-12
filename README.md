# Siga-Prototipo

Este projeto tem como objetivo desenvolver um aplicativo móvel para auxiliar alunos no acesso a informações acadêmicas e realização de solicitações administrativas de maneira segura e intuitiva.

---

## Etapa 1 – Requisitos e Casos de Uso

### Atores

- **Aluno**: Usuário principal. Consulta informações acadêmicas e realiza solicitações.
- **Secretaria**: Responsável por processar as solicitações feitas pelos alunos.

## **Requisitos Funcionais (RF):**

1. **RF1 - Autenticação de Usuário:** O sistema deverá permitir que o aluno se autentique para acessar o aplicativo .
2. **RF2 - Recuperação ou Criação de Senha:** O sistema deverá permitir que o aluno recupere sua senha existente ou crie uma nova senha .
3. **RF3 - Autenticação por E-mail:** O processo de recuperação ou criação de senha deverá incluir a autenticação via e-mail .
4. **RF4 - Gerenciamento de Matrícula (Aluno):** O sistema deverá permitir que o aluno acesse e gerencie informações relacionadas à sua matrícula .
5. **RF5 - Visualização de Histórico Acadêmico:** O sistema deverá permitir que o aluno visualize seu histórico acadêmico .
6. **RF6 - Consulta de Matérias:** O sistema deverá permitir que o aluno visualize as matérias em que está matriculado .
7. **RF7 - Visualização de Frequência por Matéria:** O sistema deverá mostrar a frequência do aluno em cada matéria .
8. **RF8 - Visualização de Notas por Matéria:** O sistema deverá mostrar as notas do aluno em cada matéria .
9. **RF9 - Emissão de Comprovantes:** O sistema deverá permitir a emissão de comprovantes, que pode ser acessada tanto pela secretaria quanto como uma extensão da gestão de matrícula .
10. **RF10 - Download de Arquivos:** O sistema deverá permitir o download de arquivos, sendo uma extensão da funcionalidade de emissão de comprovantes .

## **Requisitos Não-Funcionais (RNF):**

1. **RNF1 - Usabilidade:** A interface do aplicativo deverá ser intuitiva e fácil de usar para o Aluno .
2. **RNF2 - Segurança na Autenticação:** O processo de autenticação de usuário e a recuperação/criação de senha deverão ser seguros para proteger os dados do aluno .
3. **RNF3 - Desempenho:** O aplicativo deverá ter um desempenho eficiente ao exibir o histórico acadêmico, matérias, frequências e notas .
4. **RNF4 - Confiabilidade:** O sistema deverá garantir a precisão e a integridade das informações apresentadas, como histórico e notas .
5. **RNF5 - Acessibilidade:** O aplicativo deve ser acessível para diferentes usuários, incluindo aqueles com necessidades especiais (não explicitamente nos diagramas, mas é uma boa prática para aplicativos).
6. **RNF6 - Escalabilidade:** O aplicativo deve ser capaz de suportar um número crescente de alunos e secretarias sem degradação significativa de desempenho .
7. **RNF7 - Manutenibilidade:** A estrutura do aplicativo deve ser modular e fácil de manter, permitindo futuras atualizações e correções de forma eficiente .
8. **RNF8 - Disponibilidade:** O aplicativo deve estar disponível para uso de Alunos e Secretaria na maior parte do tempo .
9. **RNF9 - Compatibilidade:** O aplicativo deve ser compatível com as plataformas e dispositivos comuns utilizados pelos alunos (ex: Android, iOS, web browsers).
10. **RNF10 - Confirmação de Ações (Implícito):** Para ações críticas como gestão de matrícula ou emissão de comprovantes, o sistema deve fornecer confirmações claras para o usuário (implícito para evitar erros).

### Diagrama de Casos de Uso
## login:
| Caso de Uso                  | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| **Autenticação de Usuário** | O aluno insere suas credenciais (e-mail e senha) para acessar o sistema. |
| **Recupera ou Criar senha** | Caso o aluno não tenha senha ou a tenha esquecido, pode criar ou recuperar uma nova. É uma **extensão** da autenticação. |
| **Autenticação via email**  | Forma alternativa de autenticação por e-mail (ex: link enviado para acesso). É uma **inclusão** opcional. |
| **Home do App**             | Tela inicial do aplicativo exibida após login bem-sucedido. |
---
![CasoDeUsoLogin](/images/login.png)
---
## App:
| Caso de Uso                   | Descrição                                                                 |
|------------------------------|---------------------------------------------------------------------------|
| **Histórico Acadêmico**      | Visualiza histórico com disciplinas, notas e status de aprovação.         |
| **Matérias**                 | Lista de matérias em que o aluno está matriculado.                        |
| **Mostra Frequência**        | Exibe a frequência do aluno em cada matéria.                              |
| **Mostra Notas**             | Mostra as notas obtidas nas disciplinas.                                  |
| **Gestão de Matrícula**      | Permite interações com a matrícula (ex: trancamento, renovação).          |
| **Emissão de Comprovantes**  | Solicitação de documentos como atestados de matrícula.                    |
| **Download de Arquivos**     | Permite baixar documentos gerados (aluno e secretaria). **Extensão** da emissão de comprovantes. |
---
![CasoDeUsoApp](/images/app.png)
---

## Etapa 2 – Interface

### Telas Principais

- **Login**: Campos de CPF e senha.
---
![Login](/images/Login-Figma.jpg)
---
- **Esqueceu a Senha ou Primeiro Acesso**: Para Criar uma nova Senha ou Criar a Primeira senha da Conta.
---
![CriarNovaSenha](/images/Criar_Nova_Senha-Figma.jpg)
---
- **Home**: Tela principal do app.
---
![Home](/images/Home_Figma.jpg)
---
- **Matricula**: Central de serviços administrativos referente a matriculas.
---
![Matricula](/images/Matricula-Figma.jpg)
---
- **Materias**: Mostra a frequencias e Notas das Materias Matriculadas no Semestre atual.
---
![Materias](/images/Materias-Figma.jpg)
---
- **Historico**: Mostra a frequencias, Notas e Materias por Semestres.
---
![Historico](/images/Historico-Figma.jpg)
---

## Etapa 6 - Casos de Teste

| ID do Caso de Teste | Módulo/Funcionalidade    | Requisito(s) Associado(s) | Pré-condição                                      | Passos de Teste                                                                                                                                                                                                                                         | Resultado Esperado                                                                                                                                                              | Resultado Real | Status (Passou/Falhou) | Prioridade (Alta/Média/Baixa) |
|---------------------|---------------------------|----------------------------|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|--------------------------|-------------------------------|
| CT_LOGIN_001        | Autenticação              | RF1, RNF2                  | Usuário cadastrado no sistema.                  | 1. Abrir o aplicativo.  2. Inserir CPF válido.  3. Inserir senha válida.  4. Clicar em "Entra".                                                                                                                     | O usuário deve ser redirecionado para a "Home do App".                                                                                                                           |                |                          |  Alta                          |
| CT_LOGIN_002        | Autenticação              | RF1, RNF2                  | Usuário cadastrado no sistema.                  | 1. Abrir o aplicativo.  2. Inserir CPF válido.  3. Inserir senha inválida.  4. Clicar em "Entra".                                                                                                                   | O sistema deve exibir mensagem de erro "CPF ou senha inválidos".                                                                                                                |                |                          |  Alta                          |
| CT_LOGIN_003        | Autenticação              | RF1, RNF2                  | Usuário não cadastrado.                         | 1. Abrir o aplicativo.  2. Inserir CPF não cadastrado.  3. Inserir qualquer senha.  4. Clicar em "Entra".                                                                                                           | O sistema deve exibir mensagem de erro "CPF ou senha inválidos".                                                                                                                |                |                          |  Média                         |
| CT_REC_SENHA_001    | Recuperação de Senha      | RF2, RF3                   | Usuário cadastrado, mas sem acesso à senha.     | 1. Na tela de login, clicar em "Esqueceu a senha?".  2. Inserir o e-mail de recuperação associado ao CPF.  3. Verificar o recebimento do e-mail com o código.  4. Inserir o código.  5. Inserir e confirmar nova senha.  6. Clicar em "Entra".             | A senha deve ser redefinida e o usuário deve ser redirecionado para a tela de login ou "Home do App".                                                                          |                |                          |  Alta                          |
| CT_MATRICULA_001    | Gerenciamento de Matrícula| RF4                        | Usuário logado.                                 | 1. Na "Home do App", clicar em "Matrícula".  2. Clicar em "Fazer Matrícula".  3. Seguir os passos do fluxo de matrícula (ou verificar a interface).                                                                | A tela de "Fazer Matrícula" deve carregar corretamente e apresentar as opções de disciplinas/cursos.                                                                           |                |                          | Alta                          |
| CT_HIST_001         | Histórico Acadêmico       | RF5                        | Usuário logado e com dados de histórico.        | 1. Na "Home do App", clicar em "Histórico".                                                                                                                                                                        | A tela de "Histórico" deve carregar mostrando o "1º Semestre" e o "2º Semestre" (se existirem dados) com colunas "Matéria", "F", "P", "T", "N1", "N2", "NF".                   |                |                          | Alta                          |
| CT_MATERIAS_001     | Consulta de Matérias      | RF6, RF7, RF8              | Usuário logado e matriculado em matérias.       | 1. Na "Home do App", clicar em "Matérias".                                                                                                                                                                         | A tela de "Matérias" deve carregar exibindo matérias com seus respectivos dados de frequência, presenças, faltas, notas e média final.                                         |                |                          | Alta                          |
| CT_EMISS_001        | Emissão de Comprovantes   | RF9                        | Usuário logado.                                 | 1. Acessar a seção de "Matrícula".  2. Clicar em "Emissão de Comprovante".  3. Selecionar "Atestado de Matrícula Simples".                                                                                         | O sistema deve gerar o atestado ou iniciar o download, ou exibir uma prévia.                                                                                                   |                |                          | Média                         |
| CT_DOWNLOAD_001     | Download de Arquivos      | RF10                       | Usuário logado.                                 | 1. Acessar a seção de "Matrícula".  2. Clicar em "Arquivos".  3. Clicar em "Baixar PDF".                                                                                                                            | O arquivo PDF deve ser baixado para o dispositivo do usuário.                                                                                                                    |                |                          | Média                         |
| CT_USAB_001         | Usabilidade (RNF)         | RNF1                       | -                                                | 1. Navegar por todas as telas principais (Home, Matérias, Histórico, Matrícula, Login).                                                                                                                            | As transições entre as telas devem ser fluidas, os elementos clicáveis devem ser responsivos e intuitivos.                                                                     |                |                          | Alta                          |
| CT_DESEMP_001       | Desempenho (RNF)          | RNF3                       | Usuário logado.                                 | 1. Acessar a tela de "Histórico Acadêmico".  2. Cronometrar o tempo de carregamento da tela.                                                                                                                       | O carregamento da tela deve ser rápido (ex: menos de 3 segundos).                                                                                                               |                |                          | Alta                          |
| CT_SEG_001          | Segurança (RNF)           | RNF2                       | Tentativa de login com credenciais inválidas.   | 1. Tentar logar 5 vezes com CPF válido e senha inválida.                                                                                                                                                           | Após 3 tentativas, o sistema deve bloquear temporariamente o acesso ou solicitar um captcha.                                                                                   |                |                          | Alta                          |
| CT_COMP_001         | Compatibilidade (RNF)     | RNF9                       | Celular Android (versão X.X)                    | 1. Instalar e abrir o aplicativo.  2. Realizar login e navegar pelas telas principais.                                                                                                                              | Todas as funcionalidades e elementos de UI devem ser exibidos e funcionar corretamente.                                                                                         |                |                          | Média                         |













