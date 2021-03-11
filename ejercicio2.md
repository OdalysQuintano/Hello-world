/*

 
 */
package odalystest;

import javax.swing.JOptionPane;

/**
 *
 * @author Hewlett-Packard
 */
public class Odalystest {
   public static float varA,varB, ecuacion;
  
   public static int select = -1; //opción elegida del usuario
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
        //Mientras la opción elegida sea 0, preguntamos al usuario
		while(select != 0){
			//Try catch para evitar que el programa termine si hay un error
			try{
				String lectura = JOptionPane.showInputDialog(null,"********\n Elige una opción:\n1.- Calcular con la Ecuaciones" +
						"\n 0.- Salir\n**********");
				//Recoger una variable por consola
				select = Integer.parseInt(lectura); 
		
				//Switch case en Java
				switch(select){
				case 1: 
                                    pedirdatosvariables();
					JOptionPane.showMessageDialog(null, "\n EL RESULTADO DE LA ECUACION ES: " + calcularecuacion()) ;
				case 0: 
					JOptionPane.showMessageDialog(null,"Adios!");
					break;
				default:
					JOptionPane.showMessageDialog(null,"Número no reconocido");break;
				}
					
				
					
			}catch(Exception e){
				JOptionPane.showMessageDialog(null,"Uoop! Error!");
			}
		}
	}
    public static void pedirdatosvariables(){
        varA = Float.parseFloat(JOptionPane.showInputDialog(null,"Digite el Valor de la variable A: "));
         varB = Float.parseFloat(JOptionPane.showInputDialog(null,"Digite el Valor de la variable B: "));
    }
    public static float calcularecuacion(){
        ecuacion=(((varA*varA)+(2*varA*varB)+(varB*varB))/((varA*varA*varA)+(3*(varA*varA)varB)+(3*varA(varB*varB))+(varB*varB*varB)));
        return ecuacion;
    }

}