<H1> RANK </H1>
<B>Purpose</B>: Assigns a unique rank number to each row within a partition.<br>
<B>Behavior</B>: If there are ties (rows with the same values), RANK assigns the same rank to those rows, but skips the subsequent ranks.<br>
Example: <br>
<code style="color : blue">
  <p>
    SELECT column_name,
    RANK() OVER (ORDER BY column_name) AS rank
    FROM table_name;
  </p>
</code><BR>
<!DOCTYPE html>
<html>

<body>
  <table>
    <tr>
      <th>column_name</th>
      <th>rank</th>
    </tr>
    <tr>
      <td>A</td>
      <td>1</td>
    </tr>
    <tr>
      <td>A</td>
      <td>1</td>
    </tr>
    <tr>
      <td>B</td>
      <td>3</td>
    </tr>
    <tr>
      <td>C</td>
      <td>4</td>
    </tr>
  </table>
</body>
</html>
<BR>
<H1> DENSE_RANK </H1>
Purpose: Similar to RANK, but does not skip ranks when there are ties.<BR>
Behavior: Rows with the same values receive the same rank, and the next rank is consecutive.<BR>
Example:<BR>
<CODE> <P>
SELECT column_name,
       DENSE_RANK() OVER (ORDER BY column_name) AS dense_rank
FROM table_name;
</P></CODE><BR>
<!DOCTYPE html>
<html>
<body>
  <table>
    <tr>
      <th>column_name</th>
      <th>dense_rank</th>
    </tr>
    <tr>
      <td>A</td>
      <td>1</td>
    </tr>
    <tr>
      <td>A</td>
      <td>1</td>
    </tr>
    <tr>
      <td>B</td>
      <td>2</td>
    </tr>
    <tr>
      <td>C</td>
      <td>3</td>
    </tr>
  </table>
</body>
</html>




