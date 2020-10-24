1. Variavel pode receber qualquer tipo de dados, aparentemente. E com esse negocio de Panda, ao rodar o seguinte comando, o **conteudo das colunas** sera passado pra variavel notas.
    ```python
    notas = ["NU_NOTA_CN","NU_NOTA_CH","NU_NOTA_MT","NU_NOTA_LC","NU_NOTA_REDACAO"]
    ```

2. "hist" e abreviacao para histograma. 
   "bins" determina o numero de barras do grafico. 
   "figsize" especifica o tamanho do grafico de outpu (em cm?).
    ```python
    dados["NU_NOTA_REDACAO"].hist(bins = 55, figsize=(8, 6))
    ```

3. Ao receber mais de uma coluna, **hist()** cria mais de um grafico.
    ```python
    dados[notas].hist(bins = 55, figsize=(8, 6))
    ```

4. Talvez seria possivel ler o codigo acima como "pegue o conteudo das colunas" e depois "pegue a tabela anterior e gere um histograma"
   
5. Por alguma razao, nao e possivel usar variaveis que se cria anteriormente no notebook do Colab.

6. **value_counts()** Faz o programa buscar por quantas vezes os valores unicos de uma coluna se repetiram.
   
7. **.query("ALGO=1")** Fara o programa procurar e "retornar" (imagino) as colunas cuja condicao dentro do parenteses seja verdadeira.
   
8. Selecionar mais de uma coluna demanda passar uma lista para o comando, o que implica criar mais um par de colchetes. 
    ```python
    dados.query("NU_IDADE == 13")[["SG_UF_RESIDENCIA","NU_IDADE"]].value_counts()
    ```
9. Quando se usa **dados["QUALQUERCOISA"]**, ele procurara pelos valores da coluna para serem utilizados ou impressos, mas caso nao exista uma, o programa cria um novo. 
    
10. **sum()** serve (ou pode ser usado) para somar o valor de todos os itens de uma coluna.
    
11. Operacoes matematicas se aplicam a todos os itens, e os parenteses tambem parecem funcionar. O codigo a seguir pega as **quantidades de cada idade unica** presente na lista e a divide pela **soma do numero total de vezes que as idades apareceram na lista**, e mostra essas porcentagens de maneira **ordenada**. Note que foi necessario usar parenteses para separar a operacao matematica da ordenacao. 
    ```python
    (dados["NU_IDADE"].value_counts()/dados["NU_IDADE"].value_counts().sum()*100).sort_index()
    ```


