# Paint
Este  trabalho  tem  como  objetivo  complementar  os  conhecimentos  teóricos  na  disciplina  de Computação Gráfica com o desenvolvimento de uma aplicação de desenho gráfico assistido, como o Paint Brush.

### Vídeo exemplificando
https://www.youtube.com/watch?v=YJTuOonM_xQ&lc=UgzJgsu0fuT_3gFg7614AaABAg

### Instalar
```
git clone https://github.com/lrr68/Paint
cd Paint
```

### Executar
```
javac Paint.java
java Paint
```

### Uso das ferramentas
O programa dispõe dos seguintes recursos:
+ Plotagem de pontos soltos
+ Plotagem de retas com o algoritmo DDA e com o algoritmo de Bresenham
+ Plotagem de retângulos
+ Plotagem de circunferências
+ Translação
+ Rotação
+ Escala
+ Reflexões nos eixos X, Y e XY
+ Recortes com Cohen-Sutherland e Liang-Barsky
+ Preenchimento Boundary Fill (Faltam melhorias na implementação) 
+ Curvas Interpoladas
+ Curvas de Hermite
+ Curvas de Bezier

Para selecionar uma ferramenta, clique no botão que a representa.

As seções a seguir descrevem o uso de cada uma dessas ferramentas.

#### Plotagem de pontos soltos
Selecione a ferramenta de caneta. Cada clique no canvas vai colorir o pixel clicado com a cor selecionada.

#### Plotagem de retas DDA e Bresenham
Selecione a ferramenta DDA ou Bresenham.
As duas ferramentas têm a mesma mecânica, o primeiro clique no canvas seleciona o primeiro ponto da reta, o segundo ponto
seleciona o segundo. Logo após clicar no segundo ponto a reta será desenhada.
```  
 ----------------
p1              p2
```  
#### Plotagem de retângulos
Selecione a ferramenta retângulo.
O primeiro clique no canvas marca um dos cantos do retângulo (p1). O segundo clique marca o canto oposto do retângulo (p3).
Esses dois pontos são os pontos que fazem parte da diagonal do retângulo. 
Logo após o clique no segundo ponto o retângulo será plotado.
```         
             p3 
 +-----------+  
 |           |  
 +-----------+  
p1
```
#### Plotagem de circunferências
Selecione a ferramenta de Circunferência.
O primeiro clique no canvas marca um ponto da circunferência. O segundo clique marca o ponto oposto na circunferência.
Note que os pontos clicados são o diâmetro da circunferência.

#### Transformações (Translação, Rotação e Escala)
Essas três ferramentas tem mecânica igual.
Clique no botão da ferramenta e uma caixa de diálogo aparecerá para o usuário digitar os parâmetros.
No caso da rotação o parâmetro é o ângulo da rotação.
No caso da translação e escala os parâmetros representam o vetor de transformação
Após entrar com os parâmetros a transformação é aplicada à todos os objetos no canvas

#### Reflexões
As 3 reflexões funcionam da mesma maneira.
Ao clicar no botão da reflexão todo o canvas será refletido no eixo correspondente (X, Y ou XY).
```
      Reflexão eixo X
             |   
+--------+   |   +--------+
|        |   |   |        | 
|        |   |   |        | 
|        |   |   |        | 
+--------+   |   +--------+ 
             |

      Reflexão eixo y
                 
        +--------+    
        |        |   
        |        |  
        |        |  
        +--------+  
   ---------------------
        +--------+    
        |        |   
        |        |  
        |        |  
        +--------+  

      Reflexão eixo XY
                 
+--------+   |   
|        |   |    
|        |   |    
|        |   |    
+--------+   |   
------------------------------
             |    +--------+ 
             |    |        |
             |    |        |
             |    |        |
             |    +--------+ 
             |
```  

#### Recortes
Tanto o recorte Cohen-Sutherland como o Liang-Barsky têm a mesma mecânica.
Selecione o recorte desejado.
A forma de seleção da área é exatamente a mesma da seleção dos pontos do retângulo.
O primeiro clique é p1 e o segundo clique é p3, o ponto oposto pela diagonal à p1.
Tudo dentro dessa área será plotado, tudo que estiver fora não será plotado.
Esses métodos não apagam os objetos, eles apenas ficam escondidos. Selecionar a janela
inteira mostra todos os objetos.
```  
       ^     p3  
 +-----------+  
 |   /   \   |  
 |  /     \  |  
 | /       \ |  
 +-----------+  
p1              
```  
#### Preenchimento
Selecione a ferramenta de preenchimento.
Um clique na tela e começa a preencher a área a qual o ponto clicado pertence.

#### Curvas Interpoladas
Selecione a ferramenta de curvas interpoaldas.
O primeiro clique na tela indica o começo da curva, o segundo indica o final. Estes pontos serão fixos.
Estes dois cliques formarão uma linha entre os dois pontos. Após isso, o próximo clique deverá ser a direçãol do primeiro ponto de controle.
E o último, deverá ser a direção do segundo ponto de controle.
Os dois últimos cliques poderão ser alterados, formando curvas diferentes.

#### Curvas de Hermite
Selecione a ferramenta de curvas de Hermite.
O primeiro clique na tela indica o começo da curva, o segundo indica o final. Estes pontos serão fixos.
Estes dois cliques formarão uma linha entre os dois pontos. Após isso, o próximo clique deverá ser a direção do primeiro ponto de controle.
E o último, deverá ser a direção oposta do segundo ponto de controle.
Os dois últimos cliques poderão ser alterados, formando curvas diferentes.

#### Curvas de Bezier
Selecione a ferramenta de curvas de Bezier.
O primeiro clique na tela indica o começo da curva, o segundo indica o final. Estes pontos serão fixos.
Estes dois cliques formarão uma linha entre os dois pontos. Após isso, o próximo clique deverá ser a direçãol do primeiro ponto de controle.
E o último, deverá ser a direção do segundo ponto de controle.
Os dois últimos cliques poderão ser alterados, formando curvas diferentes.


### Alunos

+ [Laura N. de Andrade](https://github.com/lauranandrade)
+ [Lucca A. M. Santos](https://github.com/lrr68)
+ [Pedro Achilles Carvalho](https://github.com/PedroAchilles)
+ [Richard V. R. Mariano](https://github.com/richvrm)