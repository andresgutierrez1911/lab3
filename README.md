import java.util.*;

public class Risk {

	
	public static void main(String[] args) {
		
		
		 {
		
		int defenderArmy, attackArmy;
		
		Scanner attacker = new Scanner (System.in);
		System.out.print("How many armies the attacker has?");
		attackArmy = attacker.nextInt();
	
		Scanner defender = new Scanner (System.in);
		System.out.print("How many armies the defender has?");
		defenderArmy = defender.nextInt();
		
		
		while(defenderArmy>=1 && attackArmy>=4) {
		Random first =  new Random();
		int d1a = 1 + first.nextInt(6);
		Random second =  new Random();
		int d2a = 1 + second.nextInt(6);
		Random third =  new Random();
		int d3a = 1 + third.nextInt(6);
		
		
		
		System.out.println("ATTACKER RAW ROLL:"+ d1a +" "+ d2a +" "+ d3a+"");
		
		Random firstd =  new Random();
		int d1d = 1 + firstd.nextInt(6);
		Random secondd =  new Random();
		int d2d = 1 + secondd.nextInt(6);
		
		
		System.out.println("DEFENDER RAW ROLL:"+ d1d +" "+ d2d +" ");
	
		int di1a=0,di2a=0,di3a=0;
	
		if(d1a>=d2a && d2a>=d3a) {
			di1a = d1a;
			di2a = d2a;
			di3a = d3a;			
			System.out.println("ATTACKER ORDERED ROLL: "+di1a+" " +di2a+" "+di3a);
		}
		
		else if(d1a>=d3a && d3a>=d2a) {
			di1a = d1a;
			di2a = d3a;
			di3a = d2a;			
			System.out.println("ATTACKER ORDERED ROLL: "+di1a+" " +di2a+" "+di3a);
		}
		
		else if(d2a>=d1a && d1a>=d3a) {
			di1a = d2a;
			di2a = d1a;
			di3a = d3a;			
			System.out.println("ATTACKER ORDERED ROLL: "+di1a+" " +di2a+" "+di3a);
		}
		else if(d2a>=d3a && d3a>=d1a) {
			di1a = d2a;
			di2a = d3a;
			di3a = d1a;			
			System.out.println("ATTACKER ORDERED ROLL: "+di1a+" " +di2a+" "+di3a);
		}
		else if(d3a>=d2a && d2a>=d1a) {
			di1a = d3a;
			di2a = d2a;
			di3a = d1a;			
			System.out.println("ATTACKER ORDERED ROLL: "+di1a+" " +di2a+" "+di3a);
		}
		else if(d3a>=d1a && d1a>=d2a) {
			di1a = d3a;
			di2a = d1a;
			di3a = d2a;			
			System.out.println("ATTACKER ORDERED ROLL: "+di1a+" " +di2a+" "+di3a);
		}
		
		int di1d = 0,di2d=0;
		
		
		
		if(d1d>=d2d) {
			di1d = d1d;
			di2d = d2d;
			System.out.println("DEFENDER ORDERED ROLL:"+di1d+" "+di2d);
		}
		else if(d2d>=d1d) {
			di1d = d2d;
			di2d = d1d;
			System.out.println("DEFENDER ORDERED ROLL:"+di1d+" "+di2d);
		}
		
		if(di1a>di1d && di2a>di2d) {
			System.out.println("Attacker wins!");
		}
		else if(di1a>di1d && di2a<=di2d) {
			System.out.println("Both sides lose one.");
		}
		else if(di1a<=di1d && di2a>di2d) {
			System.out.println("Both sides lose one.");
		}
		else {
			System.out.println("Defender wins!");
		}
		
		int fAttackerArmy, fDefenderArmy;

		if(di1a>di1d)
		{
			attackArmy = attackArmy;
			defenderArmy = defenderArmy - 1;
		}
		else {
			attackArmy = attackArmy - 1;
			defenderArmy = defenderArmy;
		}
		
		
	
		if(di2a>di2d)
		{
			attackArmy = attackArmy;
			defenderArmy = defenderArmy - 1;
		}
		else {
			attackArmy = attackArmy - 1;
			defenderArmy = defenderArmy;
		}
		

		
		System.out.println("ATTACKER ARMIES LEFT:" +attackArmy);
		System.out.println("DEFENDER ARMIES LEFT:" +defenderArmy);
		
		if (attackArmy<4) {
			System.out.println("Defender wins the battle!");
		}
		
		if(defenderArmy<=0) {
			System.out.println("Attacker wins the battle!");
		}
		System.out.println("==========================================");
		
		
		
		}
	}
}}

		
			
	
