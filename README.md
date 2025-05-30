# repositorio_modelo

## Boas Práticas
- O nome do repositório precisa ter o memso nome do Projeto. Por exemplo: Projeto SIGA.
- Todo arquivo READM: precisa informar:
  - Visão geral do projeto
  - Tecnologias utilizadas
  - Como instalar ou utilizar esse projeto
  - Quem contribuiu (A Equipe)
  - Como pode contribuir? (Comunidade externa que visualiza esse Repositório PUBLICO)

## Organização de Pastas
- Toda linguagem de programação ou framework exige uma organização em pastas. Em comum todas elas tem essa estrutura:
  - /src -> A é pasta indicada para colocar o código fonte do projeto
  - /test -> A é pasta indicada para colocar os testes unitários
  - /public ->  A pasta é indicada para coloar o Front-end ou qualquer arquivo que precisa ficar à nível público. A nível público de API, teríamos o ENDPOINTs (ROTAS DE ACESSO)
  - /config -> (ou scripts) arquivos de configuração ou instalação de bibliotecas do projeto (isso também pode ficar na raiz do projeto - config é uma pasta opcional)
  - /docs -> A pasta é indicada para guardar imagens ou docs relacionados ao projeto. Por exemplo: Diagramas, Fluxogramas, Mapa Mentais, Canvas, etc.

## Utilizar boas práticas em Commits
É necessário realizar os dois:
  - Commits Atômicos: Realizar commits pequenos -> a unidade de trabalho
  - Commits Semnântico: É informar com sufixo e em poucas palavras o que foi realizado nessa unidade de trabalho

## Na raiz do Projeto
- É necessário ter:
  - O gitignore: é o arquivo para informar ao git quais extensões ou pastas que precisam ser ignoradas
  - License: é informado qual é a licença do projeto (Obrigatório quando o projeto é público)
  - Contribuiting: é informado quem são os autores e como contribuir
  - Changelog: é utilizado para informar o histórico de versões do Projeto

## Gerenciar Branchs
- Um projeto pode ter algumas dessas branchs abaixo:
  - main (ou master): 
    - Versão estável do projeto (ou aquilo que o público está utilizando no momento)
    - Normalmente a main é atualizada no final de cada sprint, recebe tudo que foi realizado na homolog (foi testado e comprovado)
  - homolog ou log:
    - versão posterior a de desenvolvimento, ou seja, é a de testes.
    - Normalmente ela antecipa a main
    - Normalmente a homolog é atualizada no final de cada sprint, recebendo todas as modificações criadas na develop
  - develop: 
    - Versão em desenvolvimento, normalmente é utilizada por desenvolvedores do Projeto. 
    - Centralizadora das modificações realizadas pelos devs
    - No final ela é mesclada a homolog
    - Normalmente a develop é considerada mais atualizada comparada a main e homolog

- Branchs relacionadas ao card Kanban:
  - Por exemplo:  [sufixo-atomic-feat]/[nome-card]
  - cada card do Kanban vai ter uma branch
  - cada dev pega um ou N cards do Kanban
  - cada branch é baseada da develop
  - no final ela é mesclada a develop

- Flow das branchs:
  - branch-de-trabalho -> develop -> homolog -> main