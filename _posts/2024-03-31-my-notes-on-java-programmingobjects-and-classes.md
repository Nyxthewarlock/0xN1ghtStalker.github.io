---
published: true
date: 2024-03-31
title: my notes on java programming,objects and classes
url: https://0xn1ghtstalker.github.io/
---
```
public class Account {
	private String name; // instance variable
	
	// method to set the name
public void setName(String name) {
	this.name = name;
}

public String getName() {
	return name;
}

}
```
this first file creates a public class named account and defines a method called setName which will be used later to set a name from user input as the name of an account via object instantiation

```

import java.util.Scanner;

import chap03.Account;
public class AccountTest {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		
		// instantate an object called myAccount 
		Account myAccount = new Account();
		// display initial value of name(null)
		System.out.printf("Initial name: %s%n", myAccount.getName());
		
		// prompt for and read name
		System.out.println("Please enter the name:");
		String theName = input.nextLine();
		myAccount.setName(theName);
		System.out.println();
		
		// display the name stored in object myAccount
		System.out.printf("name in object myAccount is:%n%s%n", myAccount.getName());

	}

}

```

this code then uses the account class we created earlier to instantiate an object called myAccount, reads the initial name stored in the object called myAccount which is null as we did not accept user input yet, uses the scanner util to take a name given by the user and store it in the object myAccount via input.nextLine(); then will display the name stored in the object myAccount via the printf method 

