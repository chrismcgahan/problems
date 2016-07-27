# CSV to Array
## Convert CSV to Associative Array

This project should be completed in PHP. Provided are 2 files: *left.csv* and *right.csv*. The problem has 2 steps.

### Step 1

Parse each file and convert each row into an associative array. The first row of each file is a header row. Use the headers as the keys of the associative array.

```php
// first non-header row of left.csv
$row = array(
    'id'    => '8390',
    'name'  => 'Block',
    'color' => 'Red',
    'size'  => 'Large'
);
```
Note: the keys should be pulled from the header row, not hard-coded.

### Step 2

Once you've parsed both files, join the rows from each CSV file and merge them into a single associative array. The common column is *id*, so for every id you should have a single merged associative array. For example, row 1 from *left.csv* and row 5 from *right.csv* should be merged because they share an id. The result should look something like this:

```php
$merged = array(
    'id'       => '8390',
    'name'     => 'Block',
    'color'    => 'Red',
    'size'     => 'Large',
    'texture'  => 'Smooth',
    'quantity' => '10',
    'random'   => '20323'
);
```

### End Result

In the end you should have an array of associative arrays, each of which represent a pair of merged rows. For bonus points, sort the arrays by *name* and output in JSON format.
