# atm-project
Java101_24 this program does ATM function with switch case
https://www.patika.dev/tr

import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    
	    String userName, password ;
	    int balance=4500, counter=3, transaction, cash, deposit;
	    Scanner input=new Scanner(System.in);

	    while(counter>0){
	        System.out.print("Username : ");
	        userName=input.nextLine();
	        System.out.print("Password : ");
	        password=input.nextLine();
	        
	        if(userName.equals("code123") && password.equals("dev123")){
	            
	            System.out.println("Welcome to the CodeBank");
	            do{
	                
	            System.out.println("Please choose a transaction\n1-Balance Inquiry\n2-Withdraw cash\n3-Deposit cash\n4-Quit");
	            transaction=input.nextInt();
	            switch(transaction){
	                case 1:
	                    System.out.println("Your Balance : "+balance);
	                    break;
	                case 2:
	                    System.out.println("Cash amount : ");
	                    cash=input.nextInt();
	                    if(balance<cash){
	                        System.out.println("Your balance is not enough");
	                    }
	                    else{
	                        balance-=cash;
	                        System.out.println("Your new balance : "+balance);
	                    }
	                    break;
	                case 3:
	                    System.out.println("Deposit amount : ");
	                    deposit=input.nextInt();
	                    balance+=deposit;
	                    System.out.println("Your new balance : "+balance);
	                    break;
	                    }
	    
	                    
	                    }while(transaction!=4);
	                    System.out.println("Thanks for your bank preference");
	                    break;
	        }
	        else
	        {
	        counter--;
	        System.out.println("Incorrect username or password, please try again");
	            if(counter==0){
	                System.out.println("Your bank card got blocked\nPlease contact your customer service assistant");
	            }
	            else{
	                System.out.println("Your remaining attempt is "+counter);
	            }
	        
	        
	        
	        } 
	    }
	  
	  	    
	}
}
