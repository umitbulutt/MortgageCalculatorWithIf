package week03_review;

import java. text.DecimalFormat;

public class MorgageCalculatorWithIf {
    public static void main(String[] args) {

        int loanAmount  =1_000_000;
        int loanTermInYears = 30;
        String loanType = "VA";

        double  annualInterestRateFor30Years_Fixed = 9.8,
                annualInterestRateFor15Years_Fixed = 6.9,
                annualInterestRateFor30Years_FHA = 7.24,
                annualInterestRateFor15Years_FHA = 6.62,
                annualInterestRateFor30Years_VA = 6.75,
                annualInterestRateFor15Years_VA = 5.99;


        double annualInterestRate = 0;

        if(loanType != "Fixed" && loanType !="FHA" && loanType != "VA"){
            System.err.println("Please choose the correct loan type.");
            System.exit(1);
        }
            if(loanType == "Fixed"){
                if(loanTermInYears == 30){
                    annualInterestRate = annualInterestRateFor30Years_Fixed;

                }else if(loanTermInYears == 15 ){
                    annualInterestRate = annualInterestRateFor15Years_Fixed;

                }
            }else if (loanType == "FHA"){
                if(loanTermInYears == 30 ){
                    annualInterestRate = annualInterestRateFor30Years_FHA;
                }else if(loanTermInYears == 15 ){
                    annualInterestRate = annualInterestRateFor15Years_FHA;

                }
            }else if (loanType == "VA"){

                if (loanTermInYears == 30){
                    annualInterestRate = annualInterestRateFor30Years_VA;
                }else if (loanTermInYears == 15){
                    annualInterestRate = annualInterestRateFor15Years_VA;
                }


            }


            double monthlyInterestRate  = annualInterestRate /100/12;
            int numberOfPayments  = loanTermInYears * 12;
            double monthlyPayment = (loanAmount * monthlyInterestRate) / (1 - Math.pow(1 + monthlyInterestRate, -numberOfPayments));


        DecimalFormat df = new DecimalFormat("0.0000000");


        System.out.println("Your monthly mortgage payment for a  " + loanTermInYears + " Yr. "
                + loanType + " loan is: " + df.format((monthlyPayment )   ));


        }



        }




