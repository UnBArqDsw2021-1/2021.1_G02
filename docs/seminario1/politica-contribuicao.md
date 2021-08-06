# Política de Contribuição

## 1. Introdução
Este documento tem como objetivo apresentar as ferramentas, políticas e regras adotadas pelo projeto **Tá Na Mesa** para auxiliar quem deseja contribuir.

## 2. Ferramentas 
| Ferramenta | Finalidade |
|---|---|
| GitHub | Hospedagem e versionamento de código |
| GitHub Actions | Ferramenta de integração contínua |
| GitHub Pages | Hospedagem de página web para repositório GitHub |
| Docker | Ferramenta de isolamento de ambiente |
| Docker-Compose | Ferramenta de gerenciamento de containers |
| MkDocs | Biblioteca do Python para gerar sites estáticos |


## 3 Política de Issues
Caso encontre um bug ou tenha alguma sugestão de melhoria para o software é possível criar uma issue seguindo os passos abaixo:

1. Escolha o tipo de issue a ser criado (funcionalidade, documentação ou correção de bug)
2. Escreva um título sucinto para a issue
3. Preencha a descrição da issue seguindo os passos e as orientações do template que será mostrado
4. Preencha informações adicionais caso possua (executores, épico, marco, etc)

Tanto o título como a descrição da issue devem estar escritos em português e seguir suas regras de sintaxe e semântica. 

## 4 Política de Branches

### 4.1 Repositórios de Código
![Git Flow Código](../../assets/img/politica-contribuicao/GitFlowDevelopment.png)

<figcaption>Figura 01. Imagem que contém o git flow de desenvolvimento.</figcaption>

O Git Flow dos repositórios de código será tratado da forma mostrada na imagem acima. Para uma mudança chegar a branch master (branch estável) os passos abaixo são seguidos:

1. Toda nova branch deve ser feita a partir da develop
2. Ao resolver a issue proposta, a nova branch deve ser merjada e comparada em relação a develop
3. Caso o PR seja aprovado pela equipe, a nova branch será deletada e seu conteúdo integrado a develop
4. Na develop será testada a integração entre as funcionalidades recentemente adicionadas
5. Quando a equipe atestar a estabilidade da develop seu conteúdo é integrado a master

### 4.2 Repositório de Documentação
![Git Flow Documentação](../../assets/img/politica-contribuicao/GitFlowDocumentation.png)

<figcaption>Figura 02. Imagem que contém o git flow de documentação.</figcaption>

O Git Flow do repositório de documentação será tratado da forma mostrada na imagem acima. Para uma mudança chegar a branch master (branch estável) os passos abaixo são seguidos:

1. Toda nova branch deve ser feita a partir da master
2. Ao resolver a issue proposta, a nova branch deve ser merjada e comparada em relação a master
3. Caso o PR seja aprovado pela equipe, a nova branch será deletada e seu conteúdo integrado a master

### 4.3 Regras de Nomenclatura
Toda nova branch criada nos repositórios do projeto **Tá Na Mesa** deve se propor a resolver uma issue específica, o nome da branch deve seguir as seguintes regras:

1. Conter o código da issue fornecido pelo GitHub
2. Ser curto e expressivo a respeito da issue a ser tratada
3. As palavras devem ser separadas por underscore "-"
4. Ser escrito em "lower case"

Exemplo:

    2-vision-document

## 5 Política de Commits
Os commits devem ser atômicos (uma contribuição pequena para resolver um problema específico). A mensagem do commit deve começar com o numero da issue no github entre parênteses, deve conter o que foi feito de maneira sucinta e direta, além disso ela precisa estar em português, começar com um verbo e com a primeira letra maiúscula. 

Contribuições feitas por mais de uma pessoa devem conter o comando "Co-authored-by" para identificar todos os autores envolvidos.

Exemplo de contribuição feita por um autor:

    git commit -m "(#18) Adiciona estrutura inicial do documento de identidade visual"

Exemplo de contribuição feita por mais de um autor:

    git commit -m "(#48) Cria model do usuário

    Co-authored-by: Pessoa <emailgit@email.com>"


## 6 Política de Pull Request
Para realizar um Pull Request (PR) para o repositório é necessário seguir os passos abaixo.

1. Ao resolver uma issue suba suas contribuições e crie um Pull Request
2. Escreva um título sucinto para o PR 
3. Preencha a descrição do PR seguindo os passos e as orientações do template que será mostrado
4. Ligue o PR com a issue que ele resolve
5. Preencha informações adicionais caso possua (executores, revisores, etc)

Um PR só poderá ser merjado após duas aprovações.

### 6.1 Política de Aprovação
Para um Pull Request ser aprovado nos repositórios de código, a contribuição feita deve:

1. Resolver apenas a issue específica ao qual se habilita a tratar
2. Respeitar todos os critérios de aceitação definidos na issue
3. Estar descrita na língua portuguesa
4. Possuir cobertura de testes 
5. Ser aprovada na integração contínua e nas ferramentas que ela executa
6. Conter lógica eficaz para preservar performance do aplicativo
7. Conter boas práticas de programação para preservar a qualidade do código
8. Não adicionar nenhum comportamento inesperado ao aplicativo

Para um Pull Request ser aprovado no repositório de documentação a contribuição feita deve:

1. Ser relevante para o projeto
2. Resolver apenas a issue específica ao qual se habilita a tratar
3. Respeitar todos os critérios de aceitação definidos na issue
4. Estar na língua portuguesa e seguir as normas desta 
5. Estar na pasta e formato adequados
6. Ser aprovada na integração contínua e nas ferramentas que ela executa

## 7 Política de Documentação
Para contribuir com a documentação do projeto, as regras definidas de commit, issue e PR também se aplicam, além destas pedimos atenção aos pontos abaixo:

1. Um novo documento deve ser criado dentro da pasta que corresponda a entrega que será efetuada do projeto
2. Para adicionar imagens a um documento deve-se fazer o upload delas em uma nova sub-pasta dentro da pasta images. Exemplo: "images/NomeDoNovoDocumento/gitflow.jpeg"
3. Todo documento deve conter um tópico de Introdução para dizer do que ele se trata

Caso o documento seja extenso e possua múltiplos autores, um histórico de versão deve ser inserido ao final dele, respeitando as seguintes regras: o versionamento da documentação deve seguir um padrão X.Z, onde X e Z são numerais inteiros não negativos que crescem em ordem crescente. 

Ao fazer grandes incrementos, a variável X cresce (1.0, 2.0, 3.0) e ao fazer pequenos incrementos, a variável Z cresce (1.1, 1.2, 1.3), ambas variáveis começam em zero e crescem de um em um. Ao subir a versão de X, o valor de Z volta pra zero (1.4 -> 2.0). O documento só entra na versão 1.0 se naquele momento ele estiver teoricamente finalizado.

## Histórico de Revisões

| Data       | Versão | Descrição                                              | Autor(es)                                 |
| :--------- | :----- | :----------------------------------------------------- | :---------------------------------------- |
| 05/08/2021 | 1.0   | Cria documento de Política de contribuição | [Lucas Boaventura](https://github.com/lboaventura25) |
| 05/08/2021 | 2.0   | Revisa o português e altera estrutura do commit | [Lucas Boaventura](https://github.com/lboaventura25) |