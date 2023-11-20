3. Create a Java class named MortgageCalculator with the following requirements:

    Define the following variables:

        loanAmount: Represents the loan amount.
        loanTermInYears: Represents the loan term in years.
        loanType: Represents the type of loan.

    Determine the annual interest rates for different loan types:

            Fixed:
                30 years: 7.5%
                15 years: 6.9%

            FHA:
                30 years: 7.24%
                15 years: 6.62%

            VA:
                30 years: 6.75%
                15 years: 5.99%

    Write a program to calculate the monthly mortgage payment using the following formula:

        monthlyInterestRate = annualInterestRate / 100 / 12
        numberOfPayments = loanTermInYears * 12
        monthlyPayment = (loanAmount * monthlyInterestRate) / (1 - Math.pow(1 + monthlyInterestRate, -numberOfPayments))


    Display the output in the following format:

            Example 1:
                loanAmount = $500,000
                loanTermInYears = 30
                loanType = "Fixed"

            Output:
                Your monthly mortgage payment for a 30 Yr. Fixed loan is: $3,496.00


    Ensure that the program accurately calculates the monthly mortgage payment based on the
    specified loan amount, term, and type.
