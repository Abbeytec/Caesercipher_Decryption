# Caesercipher_Decryption
package Caeserprogram;
//Name:              ABIODUN TAOFEEK TIAMIYU
//Student's Number:         21910091
//Course Code:                IT526
//Course Title:     Operating System And Network Security
import java.util.*;
public class Caesercipher_Decryption {
	public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("SOLUTION PROGRAM : ");
        System.out.println("ABIODUN TAOFEEK TIAMIYU : ");
        System.out.println("STUDENT NUMBER: 21910091 : ");
        System.out.println("OPERATING SYSTEM AND NETWORK SECURITY : ");
        System.out.println("ASSIGNMENT 2 : ");
        System.out.println(" Input the ciphertext message : ");
        String ciphertext = sc.nextLine();
        System.out.println(" Enter the shift value : ");
        int shift = sc.nextInt();
        String decryptMessage = "";
        for(int i=0; i < ciphertext.length();i++)  

        {
            // Shift one character at a time
            char alphabet = ciphertext.charAt(i);
            // if alphabet lies between a and z 
            if(alphabet >= 'a' && alphabet <= 'z')
            {
                // shift alphabet
                alphabet = (char) (alphabet - shift);
            
                // shift alphabet lesser than 'a'
                if(alphabet < 'a') {
                    //re-shift to starting position 
                    alphabet = (char) (alphabet-'a'+'z'+1);
                }
                decryptMessage = decryptMessage + alphabet;
            }    
                // if alphabet lies between A and Z
            else if(alphabet >= 'A' && alphabet <= 'Z')
            {
             // shift alphabet
                alphabet = (char) (alphabet - shift);
                
                //shift alphabet lesser than 'A'
                if (alphabet < 'A') {
                    // re-shift to starting position 
                    alphabet = (char) (alphabet-'A'+'Z'+1);
                }
                decryptMessage = decryptMessage + alphabet;            
            }
            else 
            {
             decryptMessage = decryptMessage + alphabet;            
            } 
        }
        System.out.println(" decrypt message : " + decryptMessage);
    }
}

