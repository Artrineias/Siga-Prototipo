# Siga-Prototipo

Este projeto tem como objetivo desenvolver um aplicativo móvel para auxiliar alunos no acesso a informações acadêmicas e realização de solicitações administrativas de maneira segura e intuitiva.

---

## Etapa 1 – Requisitos e Casos de Uso

### Atores

- **Aluno**: Usuário principal. Consulta informações acadêmicas e realiza solicitações.
- **Secretaria**: Responsável por processar as solicitações feitas pelos alunos.

### Requisitos Funcionais (RF)

- **RF01**: Autenticação de usuário (login, recuperação de senha, primeiro acesso).
- **RF02**: Consulta de notas, faltas, horários e histórico.
- **RF03**: Acesso a materiais de aula.
- **RF04**: Solicitações (matrícula, trancamento, emissão de documentos).
- **RF05**: Recebimento de notificações.

### Requisitos Não Funcionais (RNF)

- **RNF01**: Resposta abaixo de 3 segundos.
- **RNF02**: Interface intuitiva.
- **RNF03**: Dados criptografados e conformidade com a LGPD.
- **RNF04**: Disponibilidade de 99.5%.
- **RNF05**: Compatível com Android e iOS recentes.

### Diagrama de Casos de Uso

####Login

```
graph TD
    Usuario([Usuário])
    CriarSenha(["Criar nova senha ou primeiro login"])
    ValidarEmail(["Validação com Email cadastrado"])
    NovaSenha(["Cadastra nova senha"])
    Logar(["Logar"])
    Autenticar(["Autenticar Usuário e Senha"])
    AcessoApp(["Acesso ao App"])

    Usuario --> Logar
    Usuario --> CriarSenha

    CriarSenha --> ValidarEmail --> NovaSenha --> Autenticar

    Logar --> Autenticar --> AcessoApp

```


####App

``` 
graph TD
    Aluno([Aluno])
    App((App))
    Secretaria([Secretaria])

    Aluno --> App

    App --> GerenciarMatricula["Gerenciamento de Matrícula"]
    App --> Historico["Histórico"]
    App --> Materias["Matérias"]
    
    GerenciarMatricula --> FazerMatricula["Fazer a Matrícula"]
    GerenciarMatricula --> PedirTrancar["Pedir para Trancar Semestre"]
    GerenciarMatricula --> PedirDocumento["Pedir Documento ligados à instituição"]
    
    Materias --> ListaSemestres["Lista de Semestres Anteriores"]
    ListaSemestres --> MaisDetalhes["Mostrar matérias cursadas no semestre, notas e faltas"]

    Materias --> MateriasEmCurso["Mostra todas as matérias em curso"]
    MateriasEmCurso --> NotasTrabalhos["Notas de Prova e Trabalhos + Média Final"]
    MateriasEmCurso --> FrequenciaFaltas["Frequência e Faltas"]

    Secretaria --> BaixarDocumentos["Baixar os Documentos"]

```

---

##  Interface

### Telas Principais

- **Login**: Campos de RA e senha.
![Login](/images/Login-Figma.jpg)
---
- **Esqueceu a Senha ou Primeiro Acesso**: Para Criar uma nova Senha ou Criar a Primeira senha da Conta.
![CriarNovaSenha](/images/Criar_Nova_Senha-Figma.jpg)
---
- **Home**: Tela principal do app.
![Home](/images/Home_Figma.jpg)
---
- **Matricula**: Central de serviços administrativos referente a matriculas.
![Matricula](/images/Matricula-Figma.jpg)
---
- **Materias**: Mostra a frequencias e Notas das Materias Matriculadas no Semestre atual.
![Materias](/images/Materias-Figma.jpg)
---
- **Historico**: Mostra a frequencias, Notas e Materias por Semestres.
![Historico](/images/Historico-Figma.jpg)
---

















