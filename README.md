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
            int Billetes1000;
            int Billetes500;
            int Billetes200;
            int Billetes100;
          
            int Residuo;
            int Resultado;

            Console.WriteLine("Ingrese la Cantidad de Dinero que desea retirar");
            CantidadDinero = int.Parse(Console.ReadLine());
            // Procesamineto
            
            
            Billetes1000 = CantidadDinero / 1000;
            Residuo = CantidadDinero % 1000;

            Billetes500 = Residuo / 500;
            Residuo=Residuo% 500;

            Billetes200 = Residuo / 200;
            Residuo = Residuo % 200;

            Billetes100 = Residuo / 100;
            Residuo = Residuo % 100;

           
                  
            //Cantifad minima de billetes
            Resultado = Billetes1000 + Billetes500 + Billetes200 + Billetes100 ;


            //Mostrar resultados
            Console.Clear();
            Console.WriteLine("Dinero Solicitado  : {0}", CantidadDinero);
            Console.WriteLine("Billetes de 1000   : {0}",Billetes1000 );
            Console.WriteLine("Billetes de 500   : {0}", Billetes500);
            Console.WriteLine("Billetes de 200    : {0}", Billetes200);
            Console.WriteLine("Billetes de 100    : {0}", Billetes100);
            Console.WriteLine("La cantidad Mimima de");
            Console.WriteLine("Billetes y monedas es:{0}", Resultado);       
          
            
             Console.WriteLine("");
            Console.ReadLine();
        }
    }
}

