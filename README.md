﻿## Este é meu Primeiro código em C#
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
            float peso;
            float altura;
            float imc;
            string texto;
            string opc;

            // Inicio do loop, faço a verificação após execução do while
            do
            {
                //Entrada de dados pelo usuário
                Console.Write("Informe o seu peso: ");
                peso = float.Parse(Console.ReadLine() + "\n");

                Console.Write("Informe sua altua: ");
                altura = float.Parse(Console.ReadLine() + "\n");

                imc = peso / (altura * 2);
                texto = "Seu IMC é" + " " + imc + " ";

                // Condicionais para informar a métrica do IMC
                if (imc <= 18.5)
                {
                    Console.WriteLine(texto + "Você está abaixo do peso");
                }
                else if (imc >= 18.6 && imc <= 24.9)
                {
                    Console.WriteLine(texto + "Você está no peso ideal");
                }
                else if (imc >= 25 && imc <= 29.9)
                {
                    Console.WriteLine(texto + "Você está levemente acima do peso");
                }
                else if (imc >= 30 && imc <= 34.9)
                {
                    Console.WriteLine(texto + "Você está na Obesidade");
                }

                //Se a resposta for igual a Sim, executa o programa novamente
                Console.Write("\n\nDeseja calcular novamente? :");
                opc = Console.ReadLine();

                // Limpra o console
                Console.Clear();

            } while (opc == "Sim" || opc == "SIM" || opc == "sim");
        }
    }
}
 ~~~