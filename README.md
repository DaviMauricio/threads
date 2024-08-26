# threads
Atividade pratica threads em java
Primeira Parte
Considere um contexto em que produtores de soja precisam ter controle sobre suas
colheitas. Para isso, cada produtor deve fornecer as seguintes informações:
- Código do produtor;
- Produção p/ colheita (quantidade média de sacas);
- Intervalo entre as colheitas (esse tempo será utilizado no método sleep);
- Quantidade total de sacas de soja produzidas considerando as colheitas já
realizadas.
Crie uma classe para os produtores que implementem a interface Runnable.
- No construtor dessa classe, a quantidade total de sacas já produzidas deve iniciar com
0.
- O método run deve ser implementado de forma que sejam realizadas 10 colheitas, onde
a variável da quantidade total de sacas de soja produzidas deve ser incrementada de
acordo com a produção por colheita.
- Informe a quantidade total já produzida e o código do produtor para cada
colheita realizada;

- Entre cada colheita deve haver um intervalo de acordo com o estabelecido na variável
“intervalo entre as colheita”.
No main do programa instancie dois produtores, crie threads para cada um deles e utilize o
método start() para inicializar cada thread.
Execute o programa testando algumas situações, como sugerido a seguir:
- Instancie dois produtores com as seguintes entradas:
1)1° produtor: código 111, “intervalo entre as colheitas”: 1, Produção p/ colheita: 10;
2)2° produtor: código 222, “intervalo entre as colheitas”: 10, Produção p/ colheita: 20;

______________________________
Segunda Parte
Agora considere que os produtores, não apenas realizam o controle de sua produção,
mas também armazenam sua produção em armazéns compartilhados com outros produtores.
Altere o programa de forma que seja criada a classe Armazém (que possui apenas os
indicadores de capacidade máxima e estoque).
Essa classe também deve possuir o método que permita armazenar as sacas provenientes dos
produtores no armazém, que deve ser estabelecida da seguinte forma:

- Somar na variável do estoque a produção p/ colheita do produtor - Verificando
antes se há espaço no armazém
- Se houver espaço, atualize o estoque e exiba o estoque atual do
armazém;
- Se não houver espaço no armazém deve ser exibida uma mensagem
informando.

*Já na classe do produtor, altere de forma que em seu construtor seja estabelecido o armazém
ao qual o produtor envia a soja.
No run do produtor deve ser invocado o método armazenar, passando a produção p/ colheita.
Após isso, teste o programa com algumas situações, como sugerido a seguir:
- Instancie um armazém com a seguinte entrada: estoque = 0, capacidade máxima = 150
- Instancie dois produtores com as seguintes entradas e execute o sistema:
1)1° produtor: código 111, “intervalo entre as colheitas”: 1, Produção p/ colheita: 10,

instância do armazém;

2)2° produtor: código 222, “intervalo entre as colheitas”: 1, Produção p/ colheita: 20,

instância do armazém;
- Altere a prioridade do segundo produtor para 9 (utilize o setPriority), execute o sistema e
observe as saídas;
- Por fim, altere o “intervalo entre as colheitas” do segundo produtor para 10, execute o
sistema e observe as saídas.
============================
Considere a segunda parte da atividade para responder as questões a seguir.
01- Quais problemas podem ser observados nas interações do armazém com os
produtores?
02 - O que pode ser feito para a resolução desses problemas?
03 - Quais métodos da classe Thread podem ser utilizados na resolução desses
problemas (justifique) ?
