Atividade avaliativa 01
================
Mateus Reis da Silva, Sheilla, Nilson </br>
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

**“b”** </br>O peso mediano das malas é 17.

**“c”** </br>A distâcia interquaerilica é de 13.

**“d”**

**Questão 02** </br>A alternativa correta após realizar o calculo é a
alternativa *d- 5.80*

**Questão 03**

**“a”**

``` r
x <- c(68, 70, 72, 58, 90, 110, 68, 70, 72, 80, 80, 67, 90, 94, 100, 80, 75, 79, 84, 90)
```

**“b”**

``` r
median(x)
```

    ## [1] 79.5

***Calculo da mediana***= 79.5

``` r
median(x)
```

    ## [1] 79.5

***Calculo da média***= 79.85

***Calculo dos quartiles***Primeiro Quartil (25%)= 70.0 </br> Segundo
Quartil (50%)= 79.5 </br> Terceiro Quartil (75%)= 90

***Calculo do Desvio padrão***= 12.78681

**“c”** </br>De acordo com o Histograma não há diferença, pois os
valores que representam a média e mediana estão na mesma coluna de
representação do histograma, o que leva a notar que não há diferenças.

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
  "sheilla", 1.50, 65,
  "icaro", 1.55, 70
)
tabela_01 %>% view()
```
