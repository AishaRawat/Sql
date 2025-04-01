<H1> RANK </H1>
<B>Purpose</B>: Assigns a unique rank number to each row within a partition.<br>
<B>Behavior</B>: If there are ties (rows with the same values), RANK assigns the same rank to those rows, but skips the subsequent ranks.<br>
Example: <br>
<body text="blue" > <p> SELECT column_name,
       RANK() OVER (ORDER BY column_name) AS rank
FROM table_name;
</p> </body>
