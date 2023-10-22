### Processando e Transformando Dados com Power BI

### Desafio 

 Aplicar as etapas de coleta, obtenção e transformação de dados com Power BI e MySQL na Azure. 

### Resolução

#### Banco de Dados
O primeiro passo foi criar uma instância para MySQL na Azure. Em seguida, utilizando o Workbench, montar o banco de dados com as informações fornecidas. Por fim, integrar o Power BI com o My SQL no Azure.

#### Transformação dos dados
- O banco de dados possui apenas um valor nulo, que se refere à posição de gerente de um dos colaboradores. Após uma análise mais aprofundada, observei que esse colaborador é o único alocado no setor “*headquarter*” e é responsável por supervisionar os dois outros gerentes, o que significa que ele não possui um gerente direto. Para melhorar a clareza e por conveniência, optei por substituir o valor "*null*" por "presidente".
- Para extrair a informação da coluna de endereço, que inicialmente era uma coluna complexa do banco de dados, foi preciso realizar um processo de separação por delimitador em duas etapas na extremidade direita. Em seguida, realizou-se uma etapa de separação pela extremidade esquerda, resultando na obtenção apenas das informações das ruas. Como uma das ruas era composta por duas palavras, houve a ocorrência de um traço em uma célula, o qual foi substituído por um espaço.
- As ações seguintes foram as mesclas de algumas tabelas a fim de obter as informações solicitadas. O motivo de ter sido utilizada a mescla ao invés da atribuição é que era necessário adicionar mais informações em uma tabela com base em uma coluna em comum entre elas, e não acrescentar linhas com informações que não se conectam diretamente com as informações contidas na tabela usada como referência.
- Para realizar a análise final, eu criei uma tabela que trazia informações detalhadas dos projetos, bem como dos colaboradores relacionados a eles. 


