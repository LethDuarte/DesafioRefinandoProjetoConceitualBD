# DesafioRefinandoProjetoConceitualBD

Desafio de projeto realizado durante o 'Bootcamp Database Experience', oferecido pela plataforma Digital Innovation One (DIO), em Agosto/2022. O desafio propõe que se refine um projeto conceitual de banco de dados, realizado com o modelo diagrama entidade-relacionamento, de acordo com as informações repassadas.

#### Explicando Soluções
No esboço do desafio, foram repassadas as seguintes informações:

1. Cliente PJ e PF: Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
2. Pagamento: Pode ter cadastrado mais de uma forma de pagamento;
3. Entrega: Possui status e código de rastreio.

Como soluções, apliquei a seguinte lógica:

1. Como cliente pessoa jurídica e pessoa física possuem poucas informações em comum (predominantemente, apenas o endereço), optei por criar entidades distintas que os representassem separadamente. Acredito que a empresa teria interesse em manter essas informações em tabelas distintas.
2. Como o pagamento possui algumas informações associadas a ele e se relaciona tanto com pedido quanto com cliente, criei uma entidade separada para representá-lo. Cada cliente pode fazer mais de um pagamento (sendo o número de pagamentos igual ao número de pedidos), mas uma pagamento deve se relacionar com apenas um cliente. Da mesma forma, um pagamento pode se relacionar com apenas um pedido.

3. Não encontrei atributos e relações suficientes para que a entrega se torne uma entidade; por isso, as informações sobre a entrega foram aglutinadas como atributos do pedido.