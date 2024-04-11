import java.util.Scanner;

class ATM {
 private BankAccount acc;
 private int pin;
 
 public ATM(BankAccount ac, int pin)
 {
this.acc=ac;
this.pin=pin;
}
public void menu(){
System.out.println("ATM Machine Interface");
System.out.println("1)check Balance.\t  2) Deposite. \t 3) Withdraw. \t 4) Exit");
}
public boolean verifyPin(int entered_pin){
return this.pin == entered_pin;
}

public void bank_process() {
Scanner sc = new Scanner(System.in);
int entered_pin;
System.out.println(" enter your pin:");
entered_pin = sc.nextInt();
if(verifyPin(entered_pin)){
int opt = 0;
while (opt !=4)
{
menu();
 System.out.println("enter your choice :");
opt = sc.nextInt();
switch (opt)
{
case 1:
     System.out.println("The remaining Balance is :"+acc.getBalance());
      break;
case 2:
     System.out.println("Enter amount to deposite");
     double Amount_to_deposite = sc.nextDouble();
     acc.deposite_bal(Amount_to_deposite );
     break;
case 3:
     System.out.println("Enter amount to withdraw");
     double Amount_to_withdraw = sc.nextDouble();
     acc.withdraw_bal(Amount_to_withdraw);
     break;
case 4:
     System.out.println("Thankyou for using the ATM..visit again..");
     break;
   default:
        System.out.println("Invalid option.. Please try again");
      }
    }

}else{

 System.out.println("Incorrect pin");
 }
 sc.close();
 }
 }
 class BankAccount{
 
private double bal;
public BankAccount(double initial_Bal){
this.bal=initial_Bal;
}
public double getBalance(){
return bal;
}
public void deposite_bal (double amount){
 if(amount > 0){
 bal +=amount;
 System.out.println("the amount " + amount +"is deposited successfully");
 }}
 public void  withdraw_bal (double amount){
 if(amount > 0 && amount <=bal) {
 bal -=amount;
 System.out.println("the amount " + amount +"is withdraw successfully");
 }else {
 System.out.println("you do not have sufficient balance to withdraw.");
 }
 }
 }
 
 public class ATM_Machine{
 public static void main(String[] args) {
 {
BankAccount user_account = new BankAccount(1000.0);
int actual_pin = 1234;
ATM atm= new ATM(user_account, actual_pin);
atm.bank_process();
 }
 }
 }
