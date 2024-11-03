# 
O arquivo em PNG refere-se ao desafio da aula de modelagem de dados para um e-commerce. O desafio foi modelar as entidades Cliente PF e PJ, Pagamento e a Entrega, que não tinham sido modeladas em aula.
<p> O contexto do desafio foi o seguinte: </p>  
<p>Refinando</p>
<p>• Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não
pode ter as duas informações</p>
<p>• Pagamento – Pode ter cadastrado mais de uma forma de
pagamento</p>
<p>• Entrega – Possui status e código de rastreio</p>
<p>Optei por criar 2 entidades: Pessoa Física e Pessoa Jurídica, para relacioná-las com a entidade Cliente, cada uma com seus atributos, e fazendo referência a entidade Cliente pelo id, de forma que só será acessado um cliente por vez e por tipo, se é PF ou PJ.</p>
<p>Criei uma entidade Pagamento, fazendo o relacionamento com Pedido de n:m, pois podem haver várias formas de pagamento para um pedido, e o relacionamento de Pagamento com Cliente de 1:n, pois um cliente é responsável por uma ou mais formas de pagamento.</p>
<p>Inicialmente para a Entrega, pensei em colocá-lo como um atributo de Pedido, porém percebi que isso tornaria mais dificultoso em um processo de manutenção e consulta, por exemplo. Então criei Entrega como uma entidade, pois deixa a abordagem mais organizada, permitindo adicionar novos atributos no futuro e tem maior facilidade de atualização. Entrega foi relacionada com Pedido, de 1:n, pois o pedido pode ter uma ou mais entregas.</p>
