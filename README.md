package com.company;

import java.util.ArrayList;
import java.util.Objects;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        ArrayList<Integer> testscores = new ArrayList<Integer>();
        Scanner input = new Scanner(System.in);
        int score;

        do {
            System.out.println("Test Score: ");
            score = input.nextInt();
            testscores.add(score);
        } while (score > -1);

        testscores.remove(testscores.size()-1);

        int totalscores = 0;
        for (int i = 0; i < testscores.size(); i++) {
            System.out.println(testscores.get(i));
            totalscores = totalscores + testscores.get(i);

        }
        System.out.println("Total Scores: " + totalscores);
        System.out.println("Average Scores: " + totalscores/ testscores.size());

    }
}
