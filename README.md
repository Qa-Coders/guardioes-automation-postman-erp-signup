# Guardiões Automation Postman

[![ERP Postman Automation API Test](https://github.com/Qa-Coders/guardioes-automation-newman-nodeexpress-erp/actions/workflows/ci_ApiTreinPostman.yml/badge.svg)](https://github.com/Qa-Coders/guardioes-automation-newman-nodeexpress-erp/actions/workflows/ci_ApiTreinPostman.yml)[![pages-build-deployment](https://github.com/Qa-Coders/guardioes-automation-newman-nodeexpress-erp/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/Qa-Coders/guardioes-automation-newman-nodeexpress-erp/actions/workflows/pages/pages-build-deployment)

### DESCRIÇÃO:

Desenvolvido pela equipe Guardiões do Qa.Coders Academy, o objetivo deste projeto é desenvolver as habilidades práticas em automação dos testes de API com diferentes conjuntos de dados, validação dos resultados e a criação de um pipeline de CI/CD utilizando o Git Actions para executar e validar as Collections no Postman de forma automatizada.

> **Este repositório tem uma página de publicação do "report" do teste que utiliza o Github Pages para servir páginas estáticas. Esse relatório será renovado todas as vezes que o teste for realizado.**

### URL Base: 

​	https://postman-treinamento.qacoders-academy.com.br/

## HACKATHON

## Instalação do Ambiente

* É necessário ter o Node JS com a versão mais recente instalada em sua máquina. Recomendamos que utilize a versão LTS (*Long-term support*) porque é a mais estável. 

### Instalação no Windows:

Acesse a ** [página de download do Node.js](https://nodejs.org/en/download/).**

Ao clicar na opção Windows Installer da versão LTS, será iniciado o download automático do pacote instalador;

![Site NodeJs](./.images/tela_site_node.png)

Prossiga com a instalação clicando em "Next” para instalar as configurações padrão e clique em "Install”. Pode ser que algumas janelas do terminal se abram, que é justamente a responsável pela instalação das ferramentas para módulos nativos. Basta clicar em qualquer tecla para continuar e esperar até que seja finalizada:

![Prompt Terminal](./.images/prompt_install_node.png)

### Instalação no Linux:

Para instalar a versão LTS no Linux Ubuntu, digite os comandos abaixo no terminal bash ou outro de sua preferência:

```sh default
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
```

```sh default
sudo apt-get install -y nodejs
```

Após rodar o comando o terminal exibirá a tela de execução como mostrada na figura abaixo: 

![Bash do Linux](./.images/bash_install_node_linux.png)

### **Instalação no MacOS:**

A instalação no macOS é similar com a instalação do Windows, pois também pode acessar **[página de download do Node.js](https://nodejs.org/en/download/)** e iniciar o processo por lá.

![versao Download para MacOs](./.images/tela_download_node_mac.png)

Caso queira instalar pelo terminal, é necessário que tenha instalado o gerenciador de pacotes [**homebrew](https://brew.sh/index_pt-br) .**

Para instalar, basta digitar o comando `sudo brew install node js` no terminal e será instalada a versão mais recente.

Verifique se a instalação ocorreu corretamente e digite os comandos abaixo em seu terminal.

```sh default
node --version
```

Após a exibição da versão instalada, verifique também a versão do gerenciador de pacotes para o Node( NPM) com o comando `npm --version`.

Certifique-se que a versão mais recente do "NPM” esteja instalada. Saiba mais em: https://docs.npmjs.com/

### **Instalação do Newman:**

Nos respectivos terminais de comando de cada sistema operacional, digite o comando:

```sh default
npm install -g newman
```

**Verifique a versão instalada:**

```sh default
newman --version
```

**Instalação do newman-reporter-htmlextra**

```sh default
npm install -g newman-reporter-htmlextra
```

**Verifique a versão instalada:**

```sh default
newman-reporter-htmlextra --version
```

### **Git e GitHub**

No Git e GitHub, realize as seguintes etapas:

1. Instale e Configure a conta do Git. Para saber mais, [acesse o git](https://git-scm.com/download/win)
2. Abra o terminal e clone o repositório no GitHub com os comandos abaixo:

```sh default
git clone https://github.com/Qa-Coders/guardioes-automation-newman-nodeexpress-erp.git
```

  2.1 Após clonar entrar na pasta local do repositório com o comando:

```sh default
cd guardioes-automation-newman-nodeexpress-erp
```

  2.2 Para gerar o relatório do Newman execute o comando abaixo:

```sh default
newman run ./AutomacaoCadastroLoginAcesso_Login.postman_collection.json -e ./CadastroLoginAcesso_Login.postman_environment.json --reporters cli, -r htmlextra --reporter-htmlextra-export ./docs/index.html
```

  2.3 Caso no relatório aparece erro de Certificado SSL execute o comando abaixo (acrescentando “-k” para ignorar o certificado):

```sh default
newman run ./AutomacaoCadastroLoginAcesso_Login.postman_collection.json -e ./CadastroLoginAcesso_Login.postman_environment.json -k --reporters cli, -r htmlextra --reporter-htmlextra-export ./docs/index.html
```
  2.4 Para visualizar o relatório gerado navegue até a pasta "docs" criada dentro do repositório e de dois (2) no arquivo index.html para ser aberto no navegador padrão.

<img src="./.images/pasta_docs.png" alt="Pasta Docs" width="67%" />

<img src="./.images/arquivo_index.png" alt="Arquivo index.html" width="67%" />

<img src="./.images/print_relatorio.png" alt="Reltório no Browser" width="50%" />

3. Configuração do pipeline de CI/CD no Git Actions, que será responsável por automatizar a execução dos testes no Postman sempre que houver alterações no repositório.

​	Para verificar como é script acessem o script no caminho abaixo:

​	[Link para o arquivo .yml](https://github.com/Qa-Coders/guardioes-automation-newman-nodeexpress-erp/blob/master/.github/workflows/ci_ApiTreinPostman.yml)

### Importar Collection e Environment no Postman:

1. Crie um Workspace no Postman caso não tenha. Para mais informações, acesse o [site](https://www.softwaretestinghelp.com/postman-collections-import-export-generate-code/).
2. Importe os dois JSON. Para mais informações, acesse o [site](https://www.softwaretestinghelp.com/postman-collections-import-export-generate-code/).

### Projeto Desenvolvido por:

- Adriano de Oliveira Santos
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/adriano-de-oliveira-santos-784979253/)](https://www.linkedin.com/in/adriano-de-oliveira-santos-784979253/)
- Amauri Almeida de Souza Junior
  -  [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/amauri-almeida26/)](https://www.linkedin.com/in/amauri-almeida26/)
- Daiane Barbosa Soares
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/daiane-barbosa-soares-a0841aa9/)](https://www.linkedin.com/in/daiane-barbosa-soares-a0841aa9/)
- Francisbele Sampaio
  -  [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/francisbele-sampaio-473477108)](https://www.linkedin.com/in/francisbele-sampaio-473477108)
- Gledson da Silva Sousa
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/mwlite/in/gledson-sousa/)](https://www.linkedin.com/mwlite/in/gledson-sousa/)
- Isadora dos Santos Arcosy
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/isadoraarcosy)](https://www.linkedin.com/in/isadoraarcosy)
- Liza Almeida e Lima
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=www.linkedin.com/in/lizaalmeidaelima)](www.linkedin.com/in/lizaalmeidaelima)
- Lorena da Silva Ferreira de Brito
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/lorenafbrito/)](https://www.linkedin.com/in/lorenafbrito/)
- Luciana Santos
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/luesantos)](https://www.linkedin.com/in/luesantos)
- Mariana Nogueira de Morais
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/mariana-nogueira-829a4b265)](https://www.linkedin.com/in/mariana-nogueira-829a4b265)
- Raquel Helena Swire Guimarães
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/rhswire)](https://www.linkedin.com/in/rhswire)
- Sidney Moreira
  - [![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/sidmoreira/)](https://www.linkedin.com/in/sidmoreira/)
