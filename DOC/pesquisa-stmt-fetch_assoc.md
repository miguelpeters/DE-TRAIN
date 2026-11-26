# Pesquisa STMT e FETCH ASSOC

## Equipe: Miguel Kormann Peters, Leonardo de Aguiar, Theo Maccari, Tiago Cabral

## Turma: TTDESM4


## - stmt:

No PHP, $stmt (abreviação de statement, ou "instrução" / "declaração") é uma convenção muito comum para nomear a variável ou o objeto que representa uma instrução SQL preparada (prepared statement).


basicamente é uma variável que utilizam para representar uma instrução em SQL preparada (que é o prepared statements), um método de segurança utilizado para evitar SQL injections (que é alguém colocar um código SQL em um campo para causar conflito no banco de dados). 
Normalmente, quando uma aplicação precisa consultar um funcionário pelo e-mail, por exemplo, ela envia uma instrução ao banco de dados informando que deseja encontrar um registro que corresponda àquele endereço.
Com o uso de instruções preparadas, a estrutura da consulta é separada dos valores fornecidos pelo usuário. Isso proporciona maior organização ao código e contribui para a segurança da aplicação.Por exemplo, uma consulta pode solicitar ao banco de dados todos os dados de um funcionário cujo e-mail corresponda a determinado valor. O espaço reservado permite que diferentes endereços de e-mail sejam utilizados sem precisar construir uma nova consulta manualmente. 
É importante ressaltar que os Prepared Statements são uma medida de segurança fundamental, mas não substituem outras práticas, como controle de permissões, validação de dados e proteção das credenciais de acesso ao banco. 









## - fetch_assoc:

Em PHP, a função “fetch_assoc()”  (da extensão MySQLi) serve para buscar uma linha de resultado de uma consulta ao banco de dados e retorná-la como um array associativo.Ele é muito utilizado quando precisamos consultar informações de tabelas do banco de dados e acessar seus valores pelo nome das colunas.
Sua utilização normalmente acontece depois da execução de uma consulta
O fetch_assoc() trabalha com um mecanismo conhecido como ponteiro de leitura.Esse ponteiro indica qual linha do conjunto de resultados será recuperada na próxima chamada do método.
Quando a consulta retorna vários funcionários, por exemplo, a primeira chamada recupera o primeiro registro disponível. Na chamada seguinte, o ponteiro avança e o próximo registro é recuperado.
Em sistemas administrativos, é comum existir uma página responsável por exibir todos os funcionários, gerentes, trens ou rotas cadastrados.Nessas situações, o PHP realiza uma consulta ao banco de dados e utiliza o fetch_assoc() para recuperar cada registro.
As informações recuperadas podem ser utilizadas para preencher tabelas HTML, apresentar dados em páginas administrativas ou gerar relatórios.

