# Java-Cash-

package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner changeowed = new Scanner(System.in);
        int centcount = 0;
        float dollars;
        do {
            System.out.println("How much change is owed?: ");
            dollars = changeowed.nextFloat();
        }while (dollars <= 0.00);


        int cents = Math.round(dollars * 100);


        while (cents >= 25)
        { centcount++;
            cents -= 25;
        }
        while (cents >= 10)
        { centcount++;
            cents -= 10;
        }
        while (cents >= 5)
        { centcount++;
            cents -= 5;
        }
        while (cents >= 1)
        { centcount++;
            cents -= 1;
        }


        System.out.println( "Coins required: " + centcount);

    }
}
