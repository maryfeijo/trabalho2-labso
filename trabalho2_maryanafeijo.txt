Aluno: Maryana Feijo - 0050008500
Trabalho 2 de Laboratorio de Sistemas Operacionais
Professor: Alex Salgado
1o. Semestre de 2017   Turno: Noite
--------------------------------------------------
1-Faça um script shell que exiba o seguinte menu e execute as operações abaixo:

Trabalho 2 - Aluno:(Seunome e sobrenome)
[1] Listar conteúdo da pasta atual
[2] Ver conteúdo de um arquivo
[3] Testar se uma url está no ar
[0] Sair
Escolha uma opção: 


Observações: 
- O menu sempre será mostrado após a execução de uma das opções
- O programa só termina quando o usuário escolhe a opção 0-sair
- No item 2, você deve perguntar o nome do arquivo
- No item 3, você deve perguntar o nome da url

Dúvidas?

#!/bin/bash
x="teste"
menu ()
{
while true $x != "teste"
do
clear
echo "================================================"
echo "trabalho2 aluno: maryana feijo"
echo ""
echo "1)Listar conteúdo da pasta atual"
echo""
echo "2)Ver conteúdo de um arquivo"
echo ""
echo "3)Sair do programa"
echo""
echo "================================================"

echo "Digite a opção desejada:"
read x
echo "Opção informada ($x)"
echo "================================================"

case "$x" in


    1)
      for j in $( ls )
        do
                echo "$j"
        done

      sleep 5

echo "================================================"
;;
    2)
	echo "Qual o nome do arquivo ?"
	read arquivo
	find /home/maryana -iname $(echo "$arquivo") -exec cat {} \;
	
        sleep 5
echo "================================================"

;;
    3)
       echo "saindo..."
         sleep 2
         clear;
         exit;
echo"==============================================="
;;

*)
        echo "Opção inválida!"
esac
done

}
menu