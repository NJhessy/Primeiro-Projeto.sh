# Primeiro-Projeto.sh
usado para fazer calculos, foi montado usando o bin bash no linux, para começar o uso é necessario por a numeração desejada e escolher a operação, entao será feito o calculo desejado.
#!/bin/bash

echo "Digite o primeiro número: "
read num1
echo "Digite o segundo número: "
read num2

echo "Escolha a operação(+,-,*,/): "
read operação

case $operação in
+) resultado=$(echo "$num1 + $num2" | bc);;
-) resultado=$(echo "$num1 - $num2" | bc);;
\*) resultado=$(echo "$num1 * $num2" | bc);;
/) resultado=$(echo "scale=2; $num1 / $num2" | bc);;
*) echo "Operção inválida"; exit 1;;
esac

echo "Resultado: $resultado"
