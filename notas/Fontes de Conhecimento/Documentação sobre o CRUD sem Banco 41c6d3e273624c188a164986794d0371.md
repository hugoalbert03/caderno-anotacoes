# Documentação sobre o CRUD sem Banco

```php
$cad = new Aluno($indice, $nome, $matricula, $turma, $turno, $curso);  
$arquivo = fopen("dados.txt", "a+");
echo $arquivo;
if($arquivo){
   echo "<tr>";
   
   foreach($cad as $valor){
       echo "<td>$dados</td>";
       fwrite($arquivo, $valor. PHP_EOL);
   }
   
   fclose();
   echo "</tr>";
}

```

Passo a passo:

1. Com iniciar com fopen
    1. Atribuir o fopen a uma variável.
    2. Dentro do fopen atribuir o arquivo e a decodificação de escrita
        
        ```php
        $arquivo = fopen("<Arquivo>.txt", "a+");
        ```
        
2. Adicionar a condição para validar a existência dos valores dentro do fopen
    
    ```php
    if($arquivo){
    
    }
    ```
    
3. Criar um foreach do valor e em seguida criar o fwrite para escrever os valores
    1. 
        
        ```php
        foreach($val as $dados){
        	fwrite($arquivo, $dados. PHP_EOL)
        }
        ```
        
    2.