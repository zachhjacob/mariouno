package com.byaj;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner mario = new Scanner(System.in);
        int height;
        do {
            System.out.println("How tall do you want the tower? Enter # between 1 and 8: ");
            while (!mario.hasNextInt()) {
                System.out.println("Invalid response, try again ");
                mario.next();
            }

            height = mario.nextInt();

        }
        while (height <= 1 || height > 9);
        System.out.println("Height: " + height);
        System.out.println("Stored: " + height);

        for (int row = 0; row < height; row++) {
            for (int col = 0; col < height - row; col++) {
                System.out.print(" ");
            }
            for (int hash = 0; hash <= row; hash++) {
                System.out.print("#");
            }
            System.out.println("");
        }
    }
}
