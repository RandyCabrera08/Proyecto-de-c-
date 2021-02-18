using System;
using System.Collections.Generic;
using System.Text;

namespace  Cajero_Automatico
{
    class Program
    {
        static void Main(string[] args)
        {
           
            //Cajero automatico
            //Entrega el dinero solicitado en la cantidad minima de billetes

            int CantidadDinero;
            int Billetes200;
            int Billetes100;
            int Billetes50;
            int Billetes20;
            int Billetes10;
            int Monedas5;
            int Monedas2;
            int Monedas1;
            int Residuo;
            int Resultado;

            Console.WriteLine("Ingrese la Cantidad de Dinero que desea retirar");
            CantidadDinero = int.Parse(Console.ReadLine());
            // Procesamineto
            
            
            Billetes200 = CantidadDinero / 200;
            Residuo = CantidadDinero % 200;

            Billetes100 = Residuo / 100;
            Residuo=Residuo%100;

            Billetes50 = Residuo / 50;
            Residuo = Residuo % 50;

            Billetes20 = Residuo / 20;
            Residuo = Residuo % 20;

            Billetes10 = Residuo / 10;
            Residuo = Residuo % 10;

            Monedas5 = Residuo / 5;
            Residuo=Residuo%5;

            Monedas2 = Residuo / 2;
            Residuo = Residuo % 2;

            Monedas1 = Residuo / 1;
            Residuo = Residuo % 1;

                  
            //Cantifad minima de billetes
            Resultado = Billetes200 + Billetes100 + Billetes50 + Billetes20 + Billetes10 + Monedas5 + Monedas2 + Monedas1;


            //Mostrar resultados
            Console.Clear();
            Console.WriteLine("Dinero Solicitado  : {0}", CantidadDinero);
            Console.WriteLine("Billetes de 200    : {0}",Billetes200 );
            Console.WriteLine("Billetes de 100    : {0}", Billetes100);
            Console.WriteLine("Billetes de 50     : {0}", Billetes50);
            Console.WriteLine("Billetes de 20     : {0}", Billetes20);
            Console.WriteLine("Billetes de 10     : {0}", Billetes10);
            Console.WriteLine("Monedas de 5       : {0}",Monedas5 );
            Console.WriteLine("Monedas de 2       : {0}", Monedas2);
            Console.WriteLine("Monedas de 1       : {0}", Monedas1);
            Console.WriteLine("La cantidad Mimima de");
            Console.WriteLine("Billetes y monedas es:{0}", Resultado);       
          
            
             Console.WriteLine("");
            Console.ReadLine();
        }
    }
}# Proyecto-de-c-
