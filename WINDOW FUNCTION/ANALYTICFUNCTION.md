<H1>OVER</H1>
Now , let's see what happens when we use SQL Query with Over.<br><br>
Select e* , max(salary) over() as max_salary from employee e;<br>
<b>Output</b>
<table>
  <tr>
    <th>Empid</th>
    <th>Emp_name</th>
     <th>dept_name</th>
    <th>salary</th>
     <th>salary</th>
  </tr>
</table><br>

<b>When we use over(), it treats max as analytic function.</b>

Select e*, max(salary) over(partition by dept_name) as max_salary from employee e;<br>
<b>Partition</b> by will create different window for every department.
