# daily-Expenses-

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#101827">
<title>Daily Expenses</title>
<style>
*{box-sizing:border-box}
body{
 margin:0;padding:20px;
 background:#101827;color:white;
 font-family:Arial,sans-serif;
}
.container{max-width:500px;margin:auto}
h2{margin-top:10px}
.card{
 background:#1e293b;padding:20px;
 border-radius:16px;margin:15px 0;
}
.balance{font-size:32px;font-weight:bold;color:#4ade80}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.income{color:#4ade80}
.expense{color:#fb7185}
input,select,button{
 width:100%;padding:14px;margin:7px 0;
 border:0;border-radius:10px;font-size:16px;
}
input,select{background:#334155;color:white}
button{
 background:#2563eb;color:white;
 font-weight:bold;cursor:pointer;
}
.transaction{
 background:#1e293b;padding:13px;
 margin:9px 0;border-radius:12px;
 display:flex;justify-content:space-between;
 align-items:center;gap:10px;
}
.small{font-size:12px;color:#94a3b8}
.delete{background:#991b1b;width:auto;padding:8px}
</style>
</head>
<body>
<div class="container">
<h2>💰 Daily Expenses</h2>
<p class="small">Manage your money smartly</p>

<div class="card">
<p>Total Balance</p>
<div class="balance" id="balance">৳0</div>
<div class="grid">
<div>
<p class="small">Income</p>
<h3 class="income" id="income">৳0</h3>
</div>
<div>
<p class="small">Expense</p>
<h3 class="expense" id="expense">৳0</h3>
</div>
</div>
</div>

<div class="card">
<h3>Add Transaction</h3>
<select id="type">
<option value="expense">Expense</option>
<option value="income">Income</option>
</select>
<input id="amount" type="number" min="0.01" step="0.01" placeholder="Amount (৳)">
<select id="category">
<option>Food</option>
<option>Transport</option>
<option>Shopping</option>