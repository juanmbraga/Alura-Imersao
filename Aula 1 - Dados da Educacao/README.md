# Aula 1
## Recursos uteis que mandaram no Discord
Cheatsheet sobre pandas: https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

Documentação Pandas: https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html

## Perguntas sobre os dados durante a primeira aula
•	(Treineiro) Será que quem e treineiro tem maiores chances de aumentar a nota?

•	(Treineiro) Quem faz o Enem como treineiro tem maiores chances de aprovação (como o dado de aprovação não esta presente, determinar uma média de nota mínima para aprovações seria interessante) (requereria um estudo temporal com os dados de anos anteriores para checar se a pessoa já fez antes, e se sim, quantas vezes...)

•	(Inglês e espanhol) será que os alunos que escolhem espanhol tiram mais ou menos pontos que aqueles que escolheram inglês, na prova de linguagens? 

* Ouvi sobre casos de pessoas que já que não falavam ou sabiam muito sobre nenhuma das duas línguas, escolheu espanhol na impressão de ser mais próximo da língua portuguesa. Seria isso verdade? Seria isso algo possível de ser medido com os dados disponíveis? 
* 
## Questões e comentários sobre Colab
•	Como será que o gráfico de boxplot(?) ficaria caso os dados estivessem igualmente distribuídos?

•	Para alguém que só programou em C pela primeira vez, que e considerada mais tipada e difícil, a estrutura sintática de Python (ou seja, lá o que for que esse Colab usa) está até que bem críptica

•	Talvez se na aula eles tivessem explicado melhor como as funções pudessem ser usadas, ao invés de apenas mostrar alguns exemplos. Para mim que só sei um pouco de programação e estou apenas terminando minhas aulas sobre estruturas de dados em C, e, portanto, tenho um certo conhecimento de logica de programação, confesso estar um pouco perdido sobre como esse negócio de panda manuseia listas inteiras. Saberia como trabalhar com itens e criar loops para calcular a porcentagem, mas como isso acontece em Python?? Kkk

•	Como tive provas no início da semana, estou vendo a primeira aula já no quarto dia... será que consigo terminar?

•	A pesquisar: o que é panda e no que difere de uma linguagem (Python ou C)?

•	Fato: os relatórios de erro de Python não ajudam muito alguém ignorante como eu :/

•	Achei um Cheatsheet que mandaram no Discord: https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf

## Desafios
### Desafio 1: Proporção dos inscritos por idade.
### Desafio 2: Descobrir de quais estados são os inscritos com 13 anos.
Os 4 alunos de 13 anos que se inscreveram no Enem sao dos estados de SP, MT, BA e AP.
```python
Code:	dados.query("NU_IDADE == 13")[["SG_UF_RESIDENCIA", "NU_IDADE"]].value_counts()  
Results:
SG_UF_RESIDENCIA  NU_IDADE
SP                13          1
MT                13          1
BA                13          1
AP                13          1
dtype: int64
```

### Desafio 3: Adicionar título no gráfico
### Desafio 4: Plotar os Histogramas das idades dos do treineiro e não treineiros.
### Desafio 5: Comparar as distribuições das provas em inglês espanhol
### Desafio 6: Explorar a documentações e visualizações com matplotlib ou pandas e gerar novas visualizações.
