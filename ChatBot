//import java.io.InterruptedIOException;
import java.util.Arrays;
import java.util.Scanner;
import java.lang.Thread;

public class ChatBot {
    private final Scanner input = new Scanner(System.in);

    private String itemName;
    private int itemQuantity;
    private double itemPrice, amountDue;

    private final String[] choices = {
            "A. Fruits and Vegetables(Fresh Produce)",
            "B. Meat",
            "C. Dairy",
            "D. Frozen Food",
            "E. Canned Goods",
            "F. Bakery",
            "G. Snacks",
            "H. Drinks"
    };

    private final String[][] products = {
            {"Apples", "Mango", "Lettuce", "Carrots"}, //a
            {"Beef", "Pork", "Chicken", "Fish"}, //b
            {"Yogurt", "Milk", "Cheese", "Butter"}, //c
            {"Hotdogs", "Ice Cream (Magnum)", "Ham", "Burger"}, //d
            {"Sardines", "Beans", "Spam", "Corned Beef"}, //e
            {"Flour", "Baking Dough", "Bread", "Baking Powder"}, //f
            {"Piattos", "Nova", "Cheetos", "Breadpan"}, //g
            {"Beer", "Coke", "Orange Juice", "Wine"} //h
    };

    private final int[][] prices = {
            {50, 60, 35, 24}, //a
            {450, 390, 143, 200}, //b
            {32, 140, 62, 120}, //c
            {220, 640, 500, 320}, //d
            {30, 20, 160, 35}, //e
            {360, 246, 200, 90}, //f
            {22, 22, 54, 18}, //g
            {190, 90, 160, 3442} //h
    };

    /*public void setItemName(String newItemName) { this.itemName = newItemName; }
    public void setTotalCost(int quantity, double price) { this.itemQuantity = quantity; this.itemPrice = price; }
    public String getItemName() { return itemName; }
    public double getTotalCost() { return amountDue; }*/

    public void readInput() throws InterruptedException {
        System.out.println("Hi there. I'm CoinBot :) Can I have your name please? :)");
        String greeting = input.nextLine();

        Thread.sleep(2000);

        System.out.println("Hi " + greeting + "! CoinBot will be yor guide today! :)");

        Thread.sleep(1000);

        // print grocery sections by looping
        for (int i = 0; i < choices.length; i++) {
            // print the name of the grocery section
            System.out.println(choices[i]);

            // iterate over the products in the current section
            for (int j = 0; j < products[i].length; j++) {

                // print the price of the product
                System.out.print("\t" + prices[i][j]);

                // product name
                System.out.println("\t\t\t" + products[i][j]);
            }
            System.out.println(); // line space between section
        }

        Thread.sleep(2000);

        System.out.println("What type of section did you got your items from?");
        String chosenSection = input.nextLine();

        Thread.sleep(1000);

        System.out.print("Enter the quantity: ");
        itemQuantity = input.nextInt();

        Thread.sleep(2000);

        // inputting purchased items
        // for ( initialization ; condition ; iteration)
        for(int i = 0; i < itemQuantity; i++) {
            System.out.print("Enter item " + i + ": ");
            itemName = input.nextLine();

            System.out.println("Enter the price: ");
            itemPrice = input.nextDouble();

            amountDue = itemQuantity * itemPrice;

            Thread.sleep(1000);
        }

        Thread.sleep(2000);

    }

    public void writeOutput() {
        if (itemQuantity > 1) {
            System.out.println("You are purchasing " + itemQuantity + " " + itemName + "(s) at " + itemPrice + " each.");
            System.out.printf("Amount due is %.2f", amountDue);
        } else {
            System.out.println("You are purchasing " + itemQuantity + " " + itemName + " at " + itemPrice + " each.");
            System.out.printf("Amount due is %.2f", amountDue);
        }
    }
}
