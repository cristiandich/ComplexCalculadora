# ComplexCalculadora
Calculadora usando a classe complex

package Complex;
public class ComplexCalculator {

	@SuppressWarnings("hiding")
	public static <Complex> void main(String[] args) {
		
		Complex comp1 = null;
		Complex comp2 = null;
		Complex compR;//segundo operando complexo
		int op;//operação escolhida
		do
		{
			
			op = menu ();
			Complex.clearError();// limpa o erro da última operação
			compR = null;//limpa o resultado
			
			switch (op)
			{
			
			case 1 : comp1 = readComplex (); break;
			case 2 : comp2 = readComplex (); break;
			case 3 : if(comp1 != null) compR = comp1.add (comp2); break;
			case 3 : if(comp1 != null) compR = comp1.sub (comp2); break;
			case 3 : if(comp1 != null) compR = comp1.mul (comp2); break;
			case 3 : if(comp1 != null) compR = comp1.div (comp2); 
			
			}
			
			if (op >= 3 && op <= 6)//escrita do resultado complexo ou de uma mensagem de erro
			{
				if(Complex.getError () == Complex.ComplexError.ok)
					if(compR == null) printf("falta o primeiro operando\n", null);
					else printf("Resultado -> %s\n", compR.toString());
				else printf ("Erro -> %s\n", Complex.toString());
				//pausa para ver o resultado no monitor
				readChar ("Carregue em enter para continuar");
			}
	}while (op != 0);

}

	//definição de subprogramas

	private static void printf(String string, String string2) {
		// TODO Auto-generated method stub
		
	}



	private static void readChar(String string) {
		// TODO Auto-generated method stub
		
	}



	private static int menu() {
		// TODO Auto-generated method stub
		return 0;
	}



	private static Complex readComplex() {
		// TODO Auto-generated method stub
		return null;
	}

}
