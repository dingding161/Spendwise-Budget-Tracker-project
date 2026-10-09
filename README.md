# Spendwise-Budget-Tracker-project

/*
  SpendWise - JavaScript Foundation
*/

// 1. Store application data
let budget = 0;
let expenses = 0;
let remainingBalance = 0;

// 2. Create a reusable calculation function
function calculateBalance(budget, expenses) {
    return budget - expenses;
}

// 3. Collect user input
let budgetInput = prompt("Enter your total budget:");

let expensesInput = prompt("Enter your total expenses:");

// 4. Convert the input into numbers
budget = Number(budgetInput);
expenses = Number(expensesInput);

// 5. Check the input and perform calculations
if (
    budgetInput !== null &&
    expensesInput !== null &&
    budgetInput.trim() !== "" &&
    expensesInput.trim() !== "" &&
    Number.isFinite(budget) &&
    Number.isFinite(expenses) &&
    budget >= 0 &&
    expenses >= 0
) {
    remainingBalance = calculateBalance(budget, expenses);

    // 6. Display clearly labeled results
    console.log("===== SpendWise Budget Report =====");
    console.log("Total Budget: KES " + budget.toFixed(2));
    console.log("Total Expenses: KES " + expenses.toFixed(2));
    console.log("Remaining Balance: KES " + remainingBalance.toFixed(2));

    if (remainingBalance < 0) {
        console.log("Status: You have exceeded your budget.");
    } else {
        console.log("Status: You are within your budget.");
    }
} else {
    console.log("Invalid input. Please enter valid, non-negative numbers.");
}

<script src="script.js"></script>


    <!-- Keep your existing SpendWise content above -->

    <script src="script.js"></script>
</body>
</html>
