Abba-Ismail
===========

Calculator
 
 //
//  main.c
//  Lesson
//
//  Created by AIJ on 10/1/14.
//  Copyright (c) 2014 Abba Ismail. All rights reserved.
//

#include <stdio.h>


void menu(){
        printf("***calculator\n");
        printf("1 for summation\n");
        printf("2 for division\n");
        printf("3 for subtraction\n");
        printf("4 for multiplication\n");
        printf("0 for Exit\n");
    
}


double summation(double x, double y){
    return x+y;
}

double division (double x, double y){
   // double result = 0;
    if (y == 0) {
        printf("Y cant be \'0\'!!");
        return 0;
    }else{
        return x/y;
    }
}

double subtraction (double x, double y){
    return x-y;
}

double multiplication (double x, double y){
    return x*y;
}

int main(int argc, const char * argv[]) {
    
    double number1,number2;
    int choice;
    
    printf("What operation would you like to do?\n\t1)Addition\n\t2)Division\n\t3)Subtraction\n\t4)Multiplication\n");
    printf("Enter your choice : ");
    scanf("%d" ,&choice);
    
    while (choice != 0) {
        if (choice == 1) {
            printf("enter first value : ");
            scanf("%lf",&number1);
            printf("enter second value : ");
            scanf("%lf",&number2);
            printf("The result is %lf\n", summation(number1, number2));
            menu();
            printf("enter your choice : ");
            scanf("%d" , &choice);
        }
       else if (choice == 2) {
            printf("enter first value : ");
            scanf("%lf",&number1);
            printf("enter second value : ");
            scanf("%lf",&number2);
            printf("The result is %.2lf\n",division(number1, number2));
            menu();
           printf("enter your choice : ");
            scanf("%d" , &choice);
        }
       else if (choice == 3) {
           printf("enter first value : ");
           scanf("%lf",&number1);
           printf("enter second value : ");
           scanf("%lf",&number2);
           printf("The result is %lf\n", subtraction(number1, number2));
           menu();
           printf("enter your choice : ");
           scanf("%d" , &choice);
       }
       else if (choice == 4) {
           printf("enter first value : ");
           scanf("%lf",&number1);
           printf("enter second value : ");
           scanf("%lf",&number2);
           printf("The result is %lf\n", multiplication(number1, number2));
           menu();
           printf("enter your choice : ");
           scanf("%d" , &choice);
           
    menu();
        printf("enter your choice : ");
        scanf("%d" , &choice);
    }else if(choice == 0) {
        printf("BYE Bro!!!!");
        
        return 0;
    }
    
}

    menu();

    return 0;
}
