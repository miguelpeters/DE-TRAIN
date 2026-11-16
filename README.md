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

## Estrutura do Projeto

Abaixo está a organização dos arquivos e diretórios do DE-TRAIN.

<img width="296" height="900" alt="image" src="https://github.com/user-attachments/assets/9ad22008-4861-479e-8011-13e7ccfbd35a" />
<img width="296" height="653" alt="image" src="https://github.com/user-attachments/assets/ac55f58e-27d5-4a37-9416-2d9a74372647" />

## Principais Telas

Index:
<img width="1600" height="786" alt="image" src="https://github.com/user-attachments/assets/b9b8f56c-46d8-4c11-ac2b-53e2e8b0e6fc" />

Landing Page:
<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/1df8a603-6c79-48f1-80d5-787ea3bfcd9c" />

Login:
<img width="1600" height="785" alt="image" src="https://github.com/user-attachments/assets/9c4ee675-c2b3-4420-8c92-70dbae8c103a" />

Home:
<img width="1600" height="789" alt="image" src="https://github.com/user-attachments/assets/e833b335-77f1-4188-8629-3e278637d2f6" />

Cadastro:
<img width="1600" height="782" alt="image" src="https://github.com/user-attachments/assets/99d3d36e-84b0-48f3-9cd5-16a00040f533" />

Visualização:
<img width="1600" height="784" alt="image" src="https://github.com/user-attachments/assets/e0aaf9e0-0c57-4fc2-b73d-b6bb9ff396bb" />

## Manual do Usuário

O manual apresenta orientações sobre a utilização das funcionalidades do DE-TRAIN.

[Acessar Manual do Usuário (PDF)](Manual.pdf)

## Objetivo Acadêmico
Projeto desenvolvido para fins acadêmicos na disciplina de Programação de Aplicativos, 
com o objetivo de colocar em prática conhecimentos de desenvolvimento web, 
programação em PHP, banco de dados e segurança da informação.

## Status do projeto
Concluido.
