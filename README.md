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

##  Interface

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

















