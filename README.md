Download Link: https://assignmentchef.com/product/solved-b561-assignment-2-practice-working-with-sql
<br>



In this assignment, you will practice working with SQL as discussed in lectures SQL Part 1, SQL Part 2, and Views.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> Your solutions, containing the PostgreSQL statements for solving the problems, should be submitted to IUCanvas in the required format. (See previous announcement.) It is strongly recommended that you include comments in this file to elaborate on your solutions.

In this assignment, we will use the following relation schemas about students and books.

Student(<em><u>Sid</u>,Sname</em>)

Major(<em>Sid,Major</em>)

Book(<em><u>BookNo</u>,Title,Price</em>)

Cites(<em>BookNo,CitedBookNo</em>) Buys(<em>Sid,BookNo</em>)

The relation Major stores students and their majors. A student can have multiple majors but we also allow that a student has no major. major. A tuple (<em>b,c</em>) in the relation Cites indicates that the book with book number <em>b </em>cites the book with book number <em>c</em>. Note that a book may cite multiple other books. Also, a book does not have to cited.

The primary keys of the relations are the underlined attributes and we assume the following foreign keys:

<table width="0">

 <tbody>

  <tr>

   <td width="144">Attribute in Relation</td>

   <td width="226">References Primary Key of Relation</td>

  </tr>

  <tr>

   <td width="144">Sid in Major</td>

   <td width="226">Sid in Student</td>

  </tr>

  <tr>

   <td width="144">BookNo in Cites</td>

   <td width="226">BookNo in Book</td>

  </tr>

  <tr>

   <td width="144">CitedBookNo in Cites</td>

   <td width="226">BookNo in Book</td>

  </tr>

  <tr>

   <td width="144">Sid in Buys</td>

   <td width="226">Sid in Student</td>

  </tr>

  <tr>

   <td width="144">BookNo in Buys</td>

   <td width="226">BookNo in Book</td>

  </tr>

 </tbody>

</table>

Furthermore, assume the following domains for the attributes:

<table width="0">

 <tbody>

  <tr>

   <td width="94">Attribute</td>

   <td width="79">Domain</td>

  </tr>

  <tr>

   <td width="94">Sid</td>

   <td width="79">INTEGER</td>

  </tr>

  <tr>

   <td width="94">Sname</td>

   <td width="79">TEXT</td>

  </tr>

  <tr>

   <td width="94">Major</td>

   <td width="79">TEXT</td>

  </tr>

  <tr>

   <td width="94">BookNo</td>

   <td width="79">INTEGER</td>

  </tr>

  <tr>

   <td width="94">Title</td>

   <td width="79">TEXT</td>

  </tr>

  <tr>

   <td width="94">Price</td>

   <td width="79">INTEGER</td>

  </tr>

  <tr>

   <td width="94">CitedBookNo</td>

   <td width="79">INTEGER</td>

  </tr>

 </tbody>

</table>

To do this assignment, you will have to create the above relations, including the primary and foreign keys. For data, use the data.sql file provided with this assignment.

Formulate the following queries in SQL. In these queries, unless otherwise specified, you can not use views (including temporary and parameterized views).

<ol>

 <li>Find the sid and name of each student who majors in CS and who boughta book that cost more than $10.

  <ul>

   <li>Formulate this query in SQL without using subqueries and set predicates.</li>

   <li>Formulate this query in SQL by only using the IN or NOT IN set predicates.</li>

   <li>Formulate this query in SQL by only using the SOME or ALL set predicates.</li>

   <li>Formulate this query in SQL by only using the EXISTS or NOT EXISTS set predicates.</li>

  </ul></li>

 <li>Find the bookno, title, and price of each book that was not bought by anyMath student.

  <ul>

   <li>Formulate this query in SQL without using subqueries and set predicates.</li>

   <li>Formulate this query in SQL by only using the IN or NOT IN set predicates.</li>

   <li>Formulate this query in SQL by only using the SOME or ALL set predicates.</li>

   <li>Formulate this query in SQL by only using the EXISTS or NOT EXISTS set predicates.</li>

  </ul></li>

 <li>Find the bookno, title, and price of each book that cites at least two booksthat cost less than $60.

  <ul>

   <li>Formulate this query in SQL without using subqueries and set predicates.</li>

   <li>Formulate this query in SQL by only using the IN or NOT IN set predicates.</li>

   <li>Formulate this query in SQL by only using the EXISTS or NOT EXISTS set predicates.</li>

  </ul></li>

</ol>

<a href="#_ftnref1" name="_ftn1">[1]</a> <strong>Restrictions on SQL code</strong>: You can use views but you can not use the GROUP BY clause and aggregate functions. You can also not use the INNER JOIN (or other joins) operators.

Solutions with SQL statements that do not obey these requirements will not receive credit.