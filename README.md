## Este é meu Primeiro código em C#
----
 > *Estou iniciando na linguagem e nesses primeiros dias já estou amando, vejo do Python/SQL e sempre tive um pouco de avesão a linguagem C, porém esse contato com C# mudou totalmente o meu pensamento, estou considerando uma linguagem bem completa, espero um dia me tornar um expecialista.*
 
 >*Este código é o meu primeiro desenvolvimento na linguagem, apliquei noções basicas de lógica de programação, Tenho exelentes ideias de aplicações para desevolver em C# e em breve postarei coisas cada vez mais avançadas aqui.*
 ----
 * Mapa do Código
 
 ~~~c#
using System;

namespace HelloWorld
{
    class Program 
    {

        static void Main(string[] args)
        {
            //Declarando as variaveis
            int Idx;
            float peso;
            float altura;
            float imc;
            string opc;
            string[] alternativa = new string[9]
            {
                "S","s","SIM","sim","siM","sIm","sIM","SIm","Sim"
            };

            // Inicio do loop, faço a verificação após execução do while
            try
            {
                do
                {
                    //Entrada de dados pelo usuário
                    Console.Write("Informe o seu peso: ");
                    peso = float.Parse(Console.ReadLine() + "\n");

                    Console.Write("Informe sua altua: ");
                    altura = float.Parse(Console.ReadLine() + "\n");

                    imc = peso / (altura * 2);

                    // Chama a função com a lógica da tabela IMC
                    MostraImc(imc);

                    //Se a resposta for igual a Sim, executa o programa novamente
                    Console.Write("\n\nDeseja calcular novamente? :");
                    opc = Console.ReadLine();

                    // percorre o array até encontrar a posição correta
                    for (Idx = 0; alternativa[Idx] != opc; Idx++) { }

                    // Limpra o console
                    Console.Clear();

                } while (alternativa[Idx] == opc);
            }
            catch (Exception) { Console.WriteLine("Finalizado!"); }
        }

        static void MostraImc(float i)
        {
            string texto;
            texto = "Seu IMC é" + " " + i + " ";

            if (i <= 18.5)
            {
                Console.WriteLine(texto + "Você está abaixo do peso");
            }
            else if (i >= 18.6 && i <= 24.9)
            {
                Console.WriteLine(texto + "Você está no peso ideal");
            }
            else if (i >= 25 && i <= 29.9)
            {
                Console.WriteLine(texto + "Você está levemente acima do peso");
            }
            else if (i >= 30 && i <= 34.9)
            {
                Console.WriteLine(texto + "Você está na Obesidade");
            }
        }
    }
}
 ~~~