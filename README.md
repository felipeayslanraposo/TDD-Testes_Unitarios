# TDD-Testes_Unitarios

### Projeto descrição
Projeto tem o objetivo de construir um sistema utilizando a estrutura de TDD, desenvolvendo primeiro os testes com falha e depois criar a lógica para que os testes passem com sucesso.

Neste projeto foi criado um sistema simples de calculadora, efetuando as operações básicas de Somar, Subtrair, Multiplicar e Dividir.

Abaixo uma demonstração de uma parte de código onde é feito um teste de somatória, veja que estou utilizando a TAG [Theory] onde é possível incluir vários testes sem a necessidade de duplicação de códigos.

~~~csharp
[Theory]
        [InlineData(1, 2, 3)]
        [InlineData(4, 5, 9)]
        public void TestSomar(int val1, int val2, int resultado)
        {
            Calculadora calc = construirClasse();

            int resultadoCalculadora = calc.somar(val1, val2);

            Assert.Equal(resultado, resultadoCalculadora);
~~~
