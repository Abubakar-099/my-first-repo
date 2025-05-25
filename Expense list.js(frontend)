import React, { useEffect, useState } from 'react';
import axios from 'axios';

const ExpenseList = () => {
  const [expenses, setExpenses] = useState([]);

  useEffect(() => {
    axios.get('http://localhost:5000/api/expenses')
      .then(res => setExpenses(res.data))
      .catch(err => console.error(err));
  }, []);

  return (
    <div>
      <h2>All Expenses</h2>
      <ul>
        {expenses.map(exp => (
          <li key={exp._id}>
            {exp.title} - ${exp.amount}
          </li>
        ))}
      </ul>
    </div>
  );
};

export default ExpenseList;
