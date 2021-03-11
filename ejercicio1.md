/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package pkg23221;
import javax.swing.JOptionPane;

/**
 *
 * @author Amanda Gómez
 */
public class Main {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        int valor1,valor2,valor3,sum,raiz,mul,sumtotal;
        
                try{
                    valor1=Integer.parseInt(JOptionPane.showInputDialog("Por favor ingrese el valor 1"));
                    
                    while(valor1!=-1)
                    {
                        valor2=Integer.parseInt(JOptionPane.showInputDialog("Por favor ingrese el valor 2")); 
                         valor3=Integer.parseInt(JOptionPane.showInputDialog("Por favor ingrese el valor 3"));
                         sum=valor1+valor2+valor3;
                         JOptionPane.showMessageDialog(null, "sumatoria es :\t  " + sum);
                                 raiz=(int) (Math.sqrt(sum));
                                  JOptionPane.showMessageDialog(null, "raiz es :\t  " + raiz);
                                 mul=sum*sum*sum*sum;
                                 JOptionPane.showMessageDialog(null, "multiplicacion es :\t  " + mul);
                                 sumtotal=sum+raiz+mul;
                                 JOptionPane.showMessageDialog(null, "sumatoria total es :\t  " + sumtotal);
                                        
                           valor1=Integer.parseInt(JOptionPane.showInputDialog("Por favor ingrese el valor 1"));      
                    }
                }
                catch(Exception e){
                     JOptionPane.showMessageDialog(null, "No ingrese letras o valores decimales");
                }
                 
    }
    
}