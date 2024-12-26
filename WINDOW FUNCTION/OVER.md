<h1></h1> WINDOW ANALYTIC FUNCTION </h1>
<h4>Why do we need a Window Analytuc Function</h4>

If we want to find the employee with max salary then we can use with simple sql query:
Select max(salary) as max_salary from employee;
<b>If we want to find max salary in each department then we can do group by </b>
Select dept_name , max(salary) as max_salary from employee group by dept_name;

<h5>OVER</h5>
