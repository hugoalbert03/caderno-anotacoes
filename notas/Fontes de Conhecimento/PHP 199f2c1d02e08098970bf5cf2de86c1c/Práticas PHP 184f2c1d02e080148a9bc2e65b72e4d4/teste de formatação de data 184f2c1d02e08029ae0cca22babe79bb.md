# teste de formatação de data

Código

```php
<?php
    [[formatação]] de data
    $dtype = '01.08.2003';
    $dstart = DateTime::createFromFormat('d. m. Y', $dtype);
    echo "Start date: ". $dstart->format('Y-m-d'). "\n";
?>
```