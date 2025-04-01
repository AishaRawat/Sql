<h1></h1> WINDOW ANALYTIC FUNCTION </h1>
<h4>Why do we need a Window Analytic Function</h4>

If we want to find the employee with max salary then we can use with simple sql query:<br>
Select max(salary) as max_salary from employee;<br>
<b>If we want to find max salary in each department then we can do group by </b><br>
Select dept_name , max(salary) as max_salary from employee group by dept_name;<br>
<table>
  <tr>
    <th>dept_name</th>
    <th>max_salary</th>
  </tr>
  <tr>
    <td>finance</td>
    <td>$1000</td>
  </tr>
    <tr>
    <td>Admin</td>
    <td>$3000</td>
  </tr>
    <tr>
    <td>HR</td>
    <td>$2000</td>
  </tr>
</table><BR>

But What if our requirement changes and we want to display dept_name with salary and with other employee details also .<br>
It is not possible with the aggregate function. Though we can use CTEs or <B>WITH</B> Clause but window function would be the most optimistic approach in this.

Note : Below are given reasons of using window functions:  
1. Unlike aggregate functions, window functions don't collapse rows into a single result. This means you can retain the original data structure while adding new calculated columns.<br>
2.hey can be more efficient than subqueries or joins for certain types of calculations, as they are optimized for performance in many SQL databases.<br>
3.They enable more sophisticated data analysis, such as calculating cumulative sums, finding the nth value in a partition, or identifying trends over time.<br>
4.They allow you to perform complex calculations across rows related to the current row without needing to group data. This is useful for tasks like running totals, moving averages, and ranking.<br>


