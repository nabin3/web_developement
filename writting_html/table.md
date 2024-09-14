* The <table> element is used to create a table. The contents of the table are written out row by row.

* You indicate the start of each row using the opening <tr> tag. <td> are put inside <tr>

* Each cell of a table is represented using a <td> element. (The td stands for table data.)

* The <th> element is used just like the <td> element but its purpose is to represent the heading for either a column or a row.

* Sometimes you may need the entries in a table to stretch across more than one column. The colspan attribute can be used on a <th> or <td> element and indicates how many columns that cell should run across.
```bash
<td colspan="2">Geography</td>
```

* You may also need entries in a table to stretch down across more than one row.
The rowspan attribute can be used on a <th> or <td> element to indicate how many rows a cell should span down the table. ```<td rowspan="2">Movie</td>```

* The headings of the table should sit inside the <thead> element.

* The body should sit inside the <tbody> element.

* The footer belongs inside the <tfoot> element.
