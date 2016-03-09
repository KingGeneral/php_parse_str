# php_parse_str
Do the same as parse_str without max_input_vars limitation


## Example usage

$queryString = 'abc=3&var[key]=4&array[]=5&array[]=6&array2[key][]=5&array2[key][]=6&array2[key2]=10';
ParseStr::parse($queryString, $data);

var_dump($data);

> array(4) {
>   ["abc"]=>
>   string(1) "3"
>   ["var"]=>
>   array(1) {
>     ["key"]=>
>     string(1) "4"
>   }
>   ["array"]=>
>   array(2) {
>     [0]=>
>     string(1) "5"
>     [1]=>
>     string(1) "6"
>   }
>   ["array2"]=>
>   array(2) {
>     ["key"]=>
>     array(2) {
>       [0]=>
>       string(1) "5"
>       [1]=>
>       string(1) "6"
>     }
>     ["key2"]=>
>     string(2) "10"
>   }
> }
