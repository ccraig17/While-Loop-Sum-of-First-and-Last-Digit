# While-Loop-Sum-of-First-and-Last-Digit
Understanding how to calculate the the Sum of the First and Last Digit of any Number using a While-Loop.

public class FirstAndLastDigitSum {
    public static int sumFirstAndLastDigit(int number) {
        if (number < 0) {
            return -1;
        }
        int lastNumber = 0; // the last digit of the number is stored in the variable "lastNumber"
        int sum = 0; // the total of the first and last digit is stored in "sum."

        while (number != 0) { // the while-Loop is always "True" and therefore will ALWAYs til number = zero.
            if (number >= 1 && number <= 9) { //the if-statement is for numbers btn 1-9. (
                lastNumber = number % 10;  // this line assigns ONLY the remainder of the number when divided by 10.
                sum = number + lastNumber; // the total is now placed in the variable "sum."
            } else {                      // for number greater than >= 10
                lastNumber = number % 10;  //declared variable outside the "while-loop." (lastNumber)
                while (number >= 10) {
                    number /= 10;  // this is the same as number = number/10. returning ONLY the number w/o a remainder.
                  // the NEW "number" is then returned to the "while-loop" to determine IF the condition is True/False.
                  // the "while-Loop" now reads: "while new number >=10" is true, continue again til "while new number >= 10" is false.
                  // the "while-loop" will then exit and collect the new number and lastDigit
                }
                sum = (new)number + lastNumber;  // the new values of (new)number or number and lastNumber are place in the Variable "sum."
            }
            return sum;  // since the Method expects are "return" value; sum is placed in the return for the "while-Loop."
        }
       return sum;  // this sum is used to "return sum" for the Method called.
    }
}
