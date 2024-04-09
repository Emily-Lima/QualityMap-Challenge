
# Desafio técnico QualityMap

Esse projeto de automação de testes faz parte de um desafio técnico da empresa QualityMap para uma vaga de QA Senior.

## Projeto Front-End (Website nopCommerce)

**Sobre:** É um simples sistema de e-commerce que deve ter sua tela de registro automatizada com validações de cenários de sucesso e validação de mensagens de erros.
**Acesso:** https://demo.nopcommerce.com/

## Projeto Back-End (APIs serverest)

**Sobre:** É um simples sistema de APIs que deve ter um cenário de automação para cada método HTTP, sendo eles POST, GET, PUT e DELETE.
**Acesso:** https://serverest.dev

## Embasamento técnico

Nesse projeto, foi usado como embasamento técnico os materiais do ISTQB, “Conselho Internacional de Qualificações em Testes de Software”, sendo usado especificamente materiais de fundamentos e de automação de testes.

## Abordagem de testes

O BDD, “Desenvolvimento Orientado a Comportamento” foi usado nesse projeto através da adoção de uma linguagem de fácil entendimento, no caso o Gherkin, dessa forma os cenários de testes foram todos escritos Gherkin para facilitar a compreensão dos testes.

## Estratégia da automação

A automação de testes foi desenvolvida conforme as boas práticas de clean code usando um alto nível de manutenibilidade, reuso e simplicidade de código. pensando nisso foi adotada 2 estratégias diferentes na automação de testes, sendo elas:

1.  **PageObjects ➞ Automação Front-End:** Foi empregado dessa forma para melhorar a abstração da interface do usuário, reusabilidade, manutenção simplificada e separação de responsabilidades.
    
2.  **Custom Commands ➞ Automação Back-End:** Foi empregado dessa forma para melhorar a abstração de ações repetitivas, facilidade de uso, padronização de funcionalidades, legibilidade e reutilização de lógica de teste.

## Cobertura de testes

Os testes foram projetados pensando garantir que o software funciona como esperado em 2 tipos de dispositivos, cada um com sua resolução específica, sendo elas:

**Desktop:** Testes com resolução de 1920x1080.

**Mobile:** Testes com resolução de 375x667.

## Resumo dos testes

A automação de testes está dividida em casos de sucesso e casos de falhas, cada teste é independente e pode ser executado de maneira isolada ou em conjunto, os dados apresentados abaixo são referentes a execução em conjunto.

**Back-End:** 19 cenários de sucesso e 24 cenários de falhas
**Front-End:** 14 cenários de sucesso e 24 cenários de falhas

## Tecnologias usadas

- **Node** - Ambiente de execução JavaScript

- **NPM** - Gerenciador de pacotes do Node

- **Cypress** - Framework de automação de testes

- **Gherkin** - Linguagem para descrição dos cenários

- **Faker.js** - Ferramenta de geração de dados falsos

- **Allure Report** - Ferramenta de relatórios e dashboard de testes

- **Java JDK 11** - Kit de Desenvolvimento Java 11

## Pré-requisitos

- Node instalado na versão v20.12.0 ou superior
- NPM instalado na versão 10.5.0 ou superior
- Google Chrome na versão 123.0.6312.86 ou superior
- Java JDK 11 (Apenas se quiser ter acesso aos daskboard de testes)

## Passos para executar
Faça o clone do projeto em sua maquina ou caso prefira, baixe os arquivos do projeto em sua maquina e extraia eles, depois, com o terminal aberto na pasta raiz do peojeto, execute os comandos abaixo:

`npm install cypress`

Se você quiser executar o projeto com o ambiente visual, execute o comando abaixo e depois escolha a opção Teste E2E, Chrome, clique em **frontend-testing.cy.js** para executar o projeto de front-end ou clique em **backend-testing.cy.js** para executar o projeto de back-end.

Se você deseja executar o projeto sem o ambiente visual, execute o seguinte comando:

`npx cypress run`

Agora, caso queira acessar relatórios completos com gráficos e mais detalhes, você pode fazer isso através do Allure Report, para isso é necessário ter o Java JDK 11 ou superior e as variáveis ​​de ambiente JAVA_HOME já configuradas.

Execute os comandos:

`npx cypress run`

e depois

`allure serve`

Seu navegador padrão irá abrir já com os resultados dos testes e caso queira limpar o historico do teste anterior, você pode executar o seguinte comando:

`npm run clear`

Exemplos dos relatorios de testes: