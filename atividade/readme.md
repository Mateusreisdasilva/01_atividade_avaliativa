Atividade avaliativa 01
================
Mateus Reis da Silva, Sheilla Santos da Rosa, Nilson dos santos Filho
</br>
Estat2020.1

------------------------------------------------------------------------

**Questão 01**

**(a)** </br> O erro de Astrobaldo em ter afirmado que a mala mais
pesada era de 23 Kg foi devido o mesmo não ter levado em consideração os
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

**(b)** </br> Depois de realizar o cálculo da mediana com os valores
acima, chegou-se ao resultado disposto abaixo.

``` r
median(x)
```

    ## [1] 17

**(c)** </br> Para realizar o cálculo da diferença interquartilica entre
os quartis que representam 75% e 25%, observou-se os valores que
correspondem ao peso das malas ques estão dispostos no gráfico boxplot e
observou-se que o valor que representa o primeiro quartil é 10 e o
terceiro quartil 23, dessa forma realizou a cauculo referente a
diferença interquartilica.

``` r
23 - 10
```

    ## [1] 13

Nesse calculo acima, podemos observar a distância interquartilica entre
o terceiro qurtil *75%* que é representada pelo valor *23* e o primeiro
quartil *25%* representado pelo valor *10*, para calcular essa distância
utilizou-se as operações básicas, no *R*, dessa forma possibilitando com
que calculasse a diferênca intequartilica.

**(d)** </b> Nessa questão é solicitado o calculo dos valores de malas
que pesam igual ou menos de 10 Kg, dessa forma levou-se em consideração
que as 240 malas dispostas na questão seja o total de malas que o
grafíco representa, dessa forma, os valores abaixo do grafico boxplot da
prova demonstra os pesos das malas, com isso se levarmos em consideração
os valores abaixo de 10 kg, pegou a diferença entre os quartis e
multiplicou por 1.5 *(Esse valor de 1.5 é referente aos valores
existentes entre o limite inferior do gráfico)* dessa forma foi possível
demonstra a quantidade de malas com o peso de 10 kg ou menos. Como
demonstrado no calculo abaixo.

``` r
1.5 * 12
```

    ## [1] 18

**Questão 02** </br> Nessa questão é solicitado a média aritimética dos
da nota dos 80 alunos, dessa forma, inicialmente colocou-se os dados da
média aritimetica das duas amostras de alunos, e observou-se que
alternativa correta após realizar o calculo é alternativa *d*

``` r
x <- c(6.40, 5.20)
```

``` r
mean(x)
```

    ## [1] 5.8

**Questão 03**

**(a)** </br> Nessa questão, inicialmente foi criado um vetor (X) que
tem como função representar os dados correspondentes aos (Bat/min), que
estão dispostos na questão.

Esse vetor tem como função principal representar os dados agrupados
correspondentes aos (Bat/min), o vetor está representado na sequencia
numeríca abaixo.

``` r
x <- c(68, 70, 72, 58, 90, 110, 68, 70, 72, 80, 80, 67, 90, 94, 100, 80, 75, 79, 84, 90)
```

**(b)** </br> Diante dos valores que representam os (Bat/min)
demonstrados na altrnativa **(a)** ao qual está representado pela
varievel (X) foi possivél cálcular a mediana, média, primeiro quartil,
terceiro quartil e o desvio padrão desses dados, ao qual apresentou
valores que estão dispostos abaixo.

**item-01\_mediana\_** </br> Para calcular a mediana utilizou-se como
base os dados representados pela váriavel (X), que representam os
(BAT/min), para realizar o calculo utilizou-se a função *median*, dessa
forma possibilitando o resultado disposto abaixo.

``` r
median(x)
```

    ## [1] 79.5

**item-02\_média\_** </br> No cálculo abaixo demostra como foi calculado
a média dos dados representados pela variável (X) que representam os
(BAT/min), para realizar esse cálculo utilizou-se a função *mean* e foi
possível obter o resultado reprentado abaixo.

``` r
mean(x)
```

    ## [1] 79.85

**item-03\_Calculo dos quartiles\_** </br> Pegando como base os dados da
variável (X) que representam os (BAT/min) foi possível analisar os
valores do *PRRIMEIRO QUARTIL E TERCEIRO QUARTIL* como solicitado na
atividade, depois de usar a função *quantil*, observou-se os valores
dispostos abaixo.

*Primeiro quartil*

``` r
quantile(x,c(0.25))
```

    ## 25% 
    ##  70

*Terceiro quartil*

``` r
quantile(x,c(0.75))
```

    ## 75% 
    ##  90

**item-04\_Calculo do Desvio padrão\_** </br> No procedimento abaixo foi
calculado o desvio padrão do conjunto de dados (X) que representa
(BAT/min), para realizar essse procedimento utilizou-se a função *sd*
que representa o desvio padrão, e obteve o resultado abaixo.

``` r
sd(x)
```

    ## [1] 12.78681

**(c)** </br> De acordo com o Histograma a diferença entre a média e
mediana desses dados são pequenas, pois o valor que representa a média é
de 79.85 *item-02* e o valor que representa a mediana é de 79.5
*item-01*, dessa forma é possível notar que os valores da média e
mediana estão representados na mesma coluna no histograma, a coluna que
tem a distância entre os valores 70 à 80. Diante disso pode-se tirar a
analogia de que ambos os valores representam bem o histograma, uma vez
que as diferenças entre os valores são pequenos.

``` r
hist(x)
```

![](readme_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

**Questão 04** </br> Importação e analise do conjunto de dados.

``` r
dados_csv <- read_csv("dados/brutos/frango_dieta.csv")
```

    ## 
    ## -- Column specification --------------------------------------------------------
    ## cols(
    ##   peso = col_double(),
    ##   tempo = col_double(),
    ##   frango = col_double(),
    ##   dieta = col_double()
    ## )

``` r
dados_csv %>% view()
```

``` r
dados_csv
```

    ## # A tibble: 578 x 4
    ##     peso tempo frango dieta
    ##    <dbl> <dbl>  <dbl> <dbl>
    ##  1    42     0      1     1
    ##  2    51     2      1     1
    ##  3    59     4      1     1
    ##  4    64     6      1     1
    ##  5    76     8      1     1
    ##  6    93    10      1     1
    ##  7   106    12      1     1
    ##  8   125    14      1     1
    ##  9   149    16      1     1
    ## 10   171    18      1     1
    ## # ... with 568 more rows

**(a)** </br> De acordo com os dados dispostos no datasset os valores
estão agrupados de maneira tidy, pois a organização de dados estão de
forma que favorecem com que computadores consigam ler e agrupar melhor
esses dados, nota-se também que esses dados estão apresentados de forma
que as variavéis estão organizadas em colunas vesticais e as observações
dos dados em horizontais, o que por lógica siginifica uma representação
de dados organizados de maneira tidy.

**(b)** </br> A média total que representa os valores dos pesos dos
frangos, está calculada no procedimento abaixo.

Média dos pesos de frangos.

``` r
dados_csv$peso %>% mean()
```

    ## [1] 121.8183

**(c)** </br> No procedimento a seguir, calculou-se a desvio padrão que
representam a variável peso.

Desvio Padrão da variável peso de frangos.

``` r
dados_csv$peso %>% sd()
```

    ## [1] 71.07196

**(d)** </br> Podemos classificar as variáveis envolvidas no datasset
como *quantitativas continuas* pois alguns valores dispostos nas
variáveis podem ser classificados de forma numerica de qualquer valor,
isso quer dizer que pode ter valores que contem virgulas ou pontos.
Existe dados também que são classificados como *quantitativas
discretas*, ou seja, que tem valores apenas inteiros.

**Questão 05**

O código abaixo tem como função gerar um histograma para analíse.

``` r
#---------------------------------------------------------
N <- 1000
x <- rnbinom(N, 4, .5)
hist(
x,
xlim = c(min(x), max(x)),
probability = T,
nclass = max(x) - min(x) + 1,
col = 'lightblue', xlab = ' ', ylab = ' ', axes = F,
main = 'Positive Skewed'
)
lines(density(x, bw = 1), col = 'red', lwd = 3)
```

![](readme_files/figure-gfm/unnamed-chunk-18-1.png)<!-- -->

``` r
#---------------------------------------------------------
```

De acordo com o analíse do histograma, a medida de tendência central que
mais se encaixa nos parametros de escolha para analíse desse grafico é a
*mediana*, pois a média ela é muito sensível a valores extremos, o que
acomete em deslocalizações extremas para representações grafica. Já a
mediana por ser o valor de observação intermediaria ela sofre
deslocamento de menores proporções, em relação aos valores extremos.
Dessa forma concui-se que a média é mais sensível a valores extremos, e
podem vim acometer o resultado final, do outro lado temos a mediana que
se apresenta de maneira mais relevante para essas medidas, uma vez que,
a mesma não sofre grandes ossilações de valores quando leva-se em
consideração os valores extremos.

**Questão 06** </br> Como solicitado na questão, importou-se o conjunto
de dados *dados\_co2.csv* e em seguida

``` r
dados_co2 <- read_csv("dados/brutos/dados_co2.csv")
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
dados_co2 %>% view()
```

**(a)** </br> Após importar o datasset modificou- se a variáveis
envolvidas, classificando as mesmas de maneira correta, que ficassem de
forma organizada para melhor leitura de dados, as modificações estão
dispostas abaixo.

``` r
dados_co2 %>%
  pivot_longer(
    !ano,
    names_to = "mes",
    values_to =  "ppm"
  )
```

    ## # A tibble: 468 x 3
    ##      ano mes     ppm
    ##    <dbl> <chr> <dbl>
    ##  1  1959 jan    315.
    ##  2  1959 fev    316.
    ##  3  1959 mar    316.
    ##  4  1959 abr    318.
    ##  5  1959 mai    318.
    ##  6  1959 jun    318 
    ##  7  1959 jul    316.
    ##  8  1959 ago    315.
    ##  9  1959 set    314.
    ## 10  1959 out    313.
    ## # ... with 458 more rows

``` r
dados_co2 %>% view()
```

**(b)** </br> Depois de importar o datasset e realizar análise percebeu
que os dados não estão agrupados de forma tidy, pois as variáveis
envolvidas estavão organizadas de maneira orizontal e os dados de forma
vertical, organização essa que não condiz com a forma de agrupaento de
dados e variáveis de acordo com a forma tidy.

**(c)** </br>

``` r
dados_co2 %>% 
  pivot_longer(
    !ano,
    names_to = "altura",
    values_to = "ppm"
  )
```

    ## # A tibble: 468 x 3
    ##      ano altura   ppm
    ##    <dbl> <chr>  <dbl>
    ##  1  1959 jan     315.
    ##  2  1959 fev     316.
    ##  3  1959 mar     316.
    ##  4  1959 abr     318.
    ##  5  1959 mai     318.
    ##  6  1959 jun     318 
    ##  7  1959 jul     316.
    ##  8  1959 ago     315.
    ##  9  1959 set     314.
    ## 10  1959 out     313.
    ## # ... with 458 more rows

**(d)**

**(e)**

**Questão 07**

**(a)** </br> Nessa alternativa, foi criada uma tibble que representa a
tabela disposta na atividade, como solicitado a tibble correspondente se
encontra abaixo.

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
```

**(b)** </br> Nessa alternativa foi solicitado para classificar as
variáveis envolvidas na tibble, as variáveis *peso e altura* são
variáveis *Quantitativas continua*, ou seja, que podem ser medidas em
valores quebrados, que contenham pontos ou virgulas.

**(c)** </br> Nessa alternativa para realizar os calculos, foi gerado um
vetor com a variavel (altura e peso), para facilitar os calculos de
média, mediana e desvio padrão.

Vetor criado com a variável (altura).

``` r
altura <- c(155, 158, 162, 168, 170, 170, 172, 173)
```

Nesse procedimento abaixo, colculou-se a Mediana com a variável altura.

``` r
median(altura)
```

    ## [1] 169

Utilizando os valores da variável altura nesse procedimentou,
calculou-se a Média.

``` r
mean(altura)
```

    ## [1] 166

Nesse procedimento, calculou-se o Desvio Padrão dos dados dispostos na
variável altura.

``` r
sd(altura)
```

    ## [1] 6.78233

Para calcular a média, mediana e desvio padrão, dos pesos, foi
necessario gerar um novo vetor com a variavel (peso), com intuito que os
calculos fiquem de maneira organizada.

``` r
peso <- c(50, 61, 65, 68, 69, 65, 82, 79)
```

Calculo da mediana dos dados dispostos no vetor acima, que tem como
variavel (peso).

``` r
median(peso)
```

    ## [1] 66.5

Nesse procedimento, calculou-se a média do agrupamento de dados da
variável peso.

``` r
mean(peso)
```

    ## [1] 67.375

Desvio padrão, esse procedimento foi realizado com os dados dispostos no
agrupamento de números da variável altura.

``` r
sd(peso)
```

    ## [1] 10.04188

**(d)** </br> Para gerar o gráfico plot, foi necessario utilizar os
dados que correspondem a peso e altura, disposto na tabela 01, dessa
forma o seguinte dado foi gerado.

``` r
plot(tabela_01$peso, tabela_01$altura)
```

![](readme_files/figure-gfm/unnamed-chunk-31-1.png)<!-- -->

Pode-se observar nesse gráfico que há uma relação entre peso e altura,
pois visualmente ao observarmos o crecimento dos valores que indicam
peso podemos observar também um aumento nos valores da altura, sendo
assim podemos dizer que quanto maior o peso maior será a altura, com
isso forma podemos afirmar que há relações entre essas variáveis.
