# SA-Ferrorama
## Equipe: Leonardo Aguiar, Miguel Kormann, Theo Maccari, Tiago Cabral.

## Proposta do sistema:
A proposta do nosso sistema é criar um site que permita visualizar informações sobre trens coletadas a partir de sensores IOT instalados em trilhos.

## Objetivos:
- Permitir a visualização das informações dos trens.
- Coletar informações sobre os sensores IOTs.
- Criar uma plataforma para visualização dos relatórios coletados dos sensores.
- Permitir o gerenciamento de trens, rotas e sensores.

## Tecnologias Utilizadas:
- HTML
- CSS
- Javascript
- PHP
- MySql
- XAMPP

## Metodologias de Desenvolvimento:
- Kanban
- Scrum

## Requisitos para a execução:
- XAMPP instalado
- PHP compatível com a versão utilizada no projeto
- MariaDB
- phpMyAdmin
- Navegador atualizado
- Servidor Apache habilitado

## Regras de Negócio:
- Para acessar as funcionalidades do sistema, é necessário realizar login com uma conta de funcionário ou gerente.
- Apenas gerentes podem cadastrar novas contas de funcionários.
- Gerentes e funcionários possuem acesso às funcionalidades operacionais do sistema.
- Apenas gerentes possuem permissão para acessar a visualização e o gerenciamento de usuários.
- O sistema deve validar os dados informados durante os cadastros e alterações, impedindo o envio de informações inválidas.
- O sistema deve apresentar mensagens de alerta para informar erros, campos preenchidos incorretamente e operações realizadas com sucesso.
- O usuário poderá permanecer conectado entre diferentes acessos caso não realize o logout.
- O acesso às páginas e funcionalidades restritas deve respeitar as permissões correspondentes ao tipo de usuário autenticado.

## Requisitos Funcionais:
- O sistema deve permitir que funcionários e gerentes realizem login utilizando suas credenciais cadastradas.
- O sistema deve permitir que o usuário encerre sua sessão por meio da funcionalidade de logout.
- O sistema deve permitir que gerentes cadastrem novos funcionários.
- O sistema deve permitir que gerentes visualizem, editem e excluam contas de usuários.
- O sistema deve permitir visualizar as informações dos trens cadastrados.
- O sistema deve permitir cadastrar novos trens, informando seus dados e associando-os aos funcionários responsáveis.
- O sistema deve permitir editar e excluir os trens já registrados.
- O sistema deve permitir visualizar as rotas cadastradas.
- O sistema deve permitir cadastrar novas rotas e associá-las aos trens correspondentes.
- O sistema deve permitir editar e excluir as rotas já registradas.
- O sistema deve permitir visualizar os sensores cadastrados.
- O sistema deve permitir cadastrar novos sensores e registrar suas informações.
- O sistema deve permitir editar e excluir os sensores já registrados.
- O sistema deve permitir validar os campos dos formulários antes de realizar operações de cadastro ou alteração.
- O sistema deve apresentar mensagens de confirmação ou alerta após operações realizadas, como cadastros, edições e exclusões.
- O sistema deve permitir retornar às páginas iniciais correspondentes ao perfil do usuário autenticado.

## Requisitos Não-Funcionais:
- O sistema deve apresentar um tempo de resposta adequado durante a navegação e execução de suas funcionalidades.
- A interface deve possuir uma organização intuitiva, facilitando a utilização por funcionários e gerentes.
- O sistema deve apresentar compatibilidade com navegadores modernos.
- O layout deve se adaptar a diferentes resoluções de tela, proporcionando uma experiência de utilização adequada.
- As informações sensíveis dos usuários devem ser protegidas por mecanismos adequados de segurança.
- As senhas devem ser armazenadas utilizando métodos seguros de hash, evitando o armazenamento em texto puro.
- O sistema deve utilizar mecanismos de controle de acesso para impedir que usuários não autorizados acessem funcionalidades restritas.
- As operações que envolvem alterações nos dados devem possuir validações para evitar inconsistências no banco de dados.
- O código deve possuir uma organização que facilite futuras manutenções e correções.
- O banco de dados deve manter a integridade e a consistência das informações armazenadas.
- O sistema deve apresentar mensagens claras e compreensíveis para orientar os usuários durante sua utilização.

## Segurança e controle de acesso

O sistema possui autenticação e controle de permissões de acordo com o tipo de usuário.

- Gerente: pode cadastrar, editar e excluir usuários, definir perfis e redefinir senhas.
- Funcionário: pode acessar o painel e as áreas operacionais, mas não pode administrar contas.
As senhas são armazenadas utilizando password_hash(), garantindo maior segurança. As operações de alteração de usuários utilizam requisições POST e tokens CSRF para ajudar a proteger o sistema.

O cadastro inicial do administrador é realizado pelo terminal, não ficando disponível como formulário público.

## Estrutura

DE-TRAIN/
│
├── assets/
│   ├── imgs/                  # Imagens e ícones utilizados no sistema
│   └── style/
│       └── style.css          # Estilização das páginas
│
├── database/
│   └── ferrorama.sql          # Arquivo do banco de dados
│
├── DOC/                       # Documentações e pesquisas do projeto
│   ├── Documentação-DeTrain.md
│   ├── Pesquisa-API.md
│   ├── Pesquisa-CRUD.md
│   ├── Pesquisa-PDO.md
│   ├── Pesquisa-SCRUM.md
│   ├── Pesquisa-Visual.md
│   ├── Pesquisa-XAMPP.md
│   └── Relatorio-uso-ia.md
│
├── infra/
│   ├── conexao.php            # Conexão com o banco de dados
│   └── lembrar_login.php      # Funcionalidade de manter login
│
├── public/
│   ├── cadastro_funcionario.php
│   ├── cadastro_rota.php
│   ├── cadastro_sensor.php
│   ├── cadastro_trem.php
│   ├── cadastro_usuario.php
│   ├── home_funcionario.php
│   ├── home_gerente.php
│   ├── landing_page.php
│   ├── login.php
│   ├── logout.php
│   ├── nav.php
│   ├── processa_funcionario.php
│   ├── processa_rota.php
│   ├── processa_sensor.php
│   ├── processa_trem.php
│   ├── recuperarSenha.php
│   ├── visualizar_rota.php
│   ├── visualizar_sensor.php
│   ├── visualizar_trem.php
│   └── visualizar_usuario.php
│
├── scripts/
│   ├── cadastro_funcionario.js
│   ├── cadastro_usuario.js
│   ├── login.js
│   └── script.js
│
├── index.php                  # Página inicial
├── LICENSE                    # Licença do projeto
├── README.md                  # Documentação principal
└── Manual.md                  # Manual do sistema para usuários

## Telas




## Objetivo Acadêmico
Projeto desenvolvido para fins acadêmicos na disciplina de Programação de Aplicativos, 
com o objetivo de colocar em prática conhecimentos de desenvolvimento web, 
programação em PHP, banco de dados e segurança da informação.

## Status do projeto
Concluido.
