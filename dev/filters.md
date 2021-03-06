# Filters

Filtering for books, authors, tags and genres.

Building a new query.

```php
use App\Service\Search\Find;

$find = new Find($em, $term, $filter, $orderBy);
$find->setFields([]);
$find->setForcedFilters([]);
$find->find();
```

## Options

## Query

- term - string , Operator: like
- filter - array\<filter\>
- orderBy - array
  - book - array\<order\>
  - author - array\<order\>
- limit - integer
- offset - integer

## Filter

- genre - array\<integer\>, Operator: in
- lendOn - integer, Operators: eq, gte, gt, lte, lt, null
- branches - integer, Operator: eq
- releaseYear - integer, Operator: eq, gte, gt, lte, lt, null
- sold - bool, Operator: eq
- removed - bool, Operator: eq
- type - string, Operator: eq
- added - integer, Operator: eq, gte, gt, lte, lt, null

## Order

- field - string
- direction - string
