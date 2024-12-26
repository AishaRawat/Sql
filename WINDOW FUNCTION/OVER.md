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


