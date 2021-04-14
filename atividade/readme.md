Atividade avaliativa 01
================
Mateus Reis da Silva, Sheilla Santos da Rosa, Nilson </br>
Estat2020.1

------------------------------------------------------------------------

**Questão 01**

**“a”** </br>O erro de Astrobaldo em ter afirmado que a mala mais pesada
era de 23 Kg foi devido o mesmo não ter levado em consideração os
*limites inferiores e limites superiores* conhecidos também como
*bigodes* do grafico boxplot, pois os pesos das malas estão destribuidos
também nos *limites inferiores e superiores*, porém o erro de Astrobaldo
foi não levar em consideração os valores destribuidos dentre esses
limites.

***OS DADOS NUMERICOS ABAIXO SÃO REFERENTES AOS DADOS DO GRAFICO
BOXPLOT***

``` r
x <- c(5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29) 
```

**“b”** </br> Depois de realizar o cálculo da mediana com os valores
acima, chegou-se ao resultado disposto abaixo.

``` r
median(x)
```

    ## [1] 17

**“c”** </br> Para realizar o cálculo da diferença interquartilica entre
os quartis que representam 75% e 25%, pegou-se o conjunto de dados (X)
disposto acima, e observou-se o seguinte resultado.

``` r
quantile(x)
```

    ##   0%  25%  50%  75% 100% 
    ##    5   11   17   23   29

**“d”**

**Questão 02** </br> Nessa questão inicialmente colocou-se os dados da
média aritimetica das duas amostras de alunos, e observou-se que
alternativa correta após realizar o calculo é alternativa *d*

``` r
x <- c(6.40, 5.20)
```

``` r
median(x)
```

    ## [1] 5.8

**Questão 03**

**“a”** </br> Nesse procedimento foi criado um vetor (X) que tem como
função representar os dados correspondentes aos (Bat/min).

``` r
x <- c(68, 70, 72, 58, 90, 110, 68, 70, 72, 80, 80, 67, 90, 94, 100, 80, 75, 79, 84, 90)
```

**“b”** </br> Diante dos valores que representam os (Bat/min) acima, que
está representada pela varievel (X) foi possivél cálcular a mediana
desses dados, ao qual apresentou valor disposto abaixo.

***mediana*** </br> Para calcular a mediana utilizou-se como base os
dados representados pela váriavel (X), que representam os (BAT/min),
para calcular utilizou-se a função *median*, dessa forma possibilitando
o resultado disposto abaixo.

``` r
median(x)
```

    ## [1] 79.5

***média*** </br> No cálculo abaixo demostra como foi calculado a média
dos dados representados pela variável (X) que representam os (BAT/min),
para realizar esse cálculo utilizou-se a função *mean* e foi possível
obter o resultado abaixo.

``` r
mean(x)
```

    ## [1] 79.85

***Calculo dos quartiles*** </br> Pegando como base os dados da variável
(X) que representam os (BAT/min) foi possível analisar os seguintes
quatiles depois de usar a função *quantil*.

``` r
quantile(x)
```

    ##    0%   25%   50%   75%  100% 
    ##  58.0  70.0  79.5  90.0 110.0

***Calculo do Desvio padrão*** </br> No procedimento abaixo foi
calculado o desvio padrão do conjunto de dados (X) que representa
(BAT/min), utilizou-se a função *sd* e obteve o resultado abaixo.

``` r
sd(x)
```

    ## [1] 12.78681

**“c”** </br> De acordo com o Histograma não há diferença entre a média
e mediana desses dados analisados, pois o valor que representa a média é
de 79.85 e o valor que representa a mediana é de 79.5, dessa forma é
possível notar que os valores da média e mediana estão representados na
mesma coluna no histograma, a coluna que varia de 70 à 80. Diante disso
poe-se concluir que ambos os valores representam bem o histograma.

``` r
hist(x)
```

![](readme_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

**Questão 07**

``` r
dadosCo2 <- read_csv("dados/brutos/dados_co2.csv")
```

    ## 
    ## -- Column specification --------------------------------------------------------
    ## cols(
    ##   ano = col_double(),
    ##   jan = col_double(),
    ##   fev = col_double(),
    ##   mar = col_double(),
    ##   abr = col_double(),
    ##   mai = col_double(),
    ##   jun = col_double(),
    ##   jul = col_double(),
    ##   ago = col_double(),
    ##   set = col_double(),
    ##   out = col_double(),
    ##   nov = col_double(),
    ##   dez = col_double()
    ## )

``` r
dadosCo2
```

    ## # A tibble: 39 x 13
    ##      ano   jan   fev   mar   abr   mai   jun   jul   ago   set   out   nov   dez
    ##    <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl> <dbl>
    ##  1  1959  315.  316.  316.  318.  318.  318   316.  315.  314.  313.  315.  315.
    ##  2  1960  316.  317.  317.  319.  320.  319.  318.  316.  314   314.  315.  316.
    ##  3  1961  317.  318.  318.  319.  320.  320.  318.  317.  315.  315.  316.  317.
    ##  4  1962  318.  318.  320.  320.  321.  320.  319.  317.  316.  315.  317.  318.
    ##  5  1963  319.  319.  320.  321.  322.  321.  320.  318.  316.  316.  317.  318.
    ##  6  1964  319.  320.  321.  321.  322.  322.  320.  319.  317.  317.  318.  319.
    ##  7  1965  319.  320.  321.  322.  322   322.  321.  319.  318.  317.  319.  319.
    ##  8  1966  320.  321.  322.  324.  324.  324.  322.  320.  318.  318.  320.  321.
    ##  9  1967  322.  322.  323.  324.  325.  324.  322.  321.  319.  319.  321.  322.
    ## 10  1968  322.  323.  324.  325.  325.  325.  324.  322.  320.  320.  321.  323.
    ## # ... with 29 more rows

``` r
tabela_01 <- tribble(
  ~nome, ~altura, ~peso,
  "Ana", 155, 50,
  "Ludimilla", 158, 61,
  "Cristina", 162, 65,
  "Tereza", 168, 68,
  "Patrícia", 170, 69,
  "Mariana", 170, 65,
  "Ana Paula", 172, 82,
  "Dirce", 173, 79) 
tabela_01 %>% view()
```

**“c”** </br> Nessa alternativa para realizar os calculos, foi gerado um
vetor com a variavel (altura e peso), para facilitar os calculos de
média, mediana e desvio padrão.

``` r
altura <- c(155, 158, 162, 168, 170, 170, 172, 173)
```

Mediana

``` r
median(altura)
```

    ## [1] 169

Média

``` r
mean(altura)
```

    ## [1] 166

Desvio Padrão

``` r
sd(altura)
```

    ## [1] 6.78233

Para calcular a média, mediana e desvio padrão, dos pesos, foi
necessario gerar um veto com a variavel (peso).

``` r
peso <- c(50, 61, 65, 68, 69, 65, 82, 79)
```

meidana

``` r
median(peso)
```

    ## [1] 66.5

media

``` r
mean(peso)
```

    ## [1] 67.375

desvio padrão

``` r
sd(peso)
```

    ## [1] 10.04188
