# 7-Power-BI-Analise-Frete
Dashboard de Fretes solicitado pelo CEO

Após uma reunião com o CEO e o time diretivo sobre o assunto
Fretes, foi solicitado as seguintes analises e vizualizações:

### Cartões:

1. Total de Frete
2. Frete Acumulado (Ano Atual)
3. Frete Acumulado (Ano Anterior)
4. Taxa de Crescimento Acumulado (Ano Atual x Ano Anterior)
5. % de Desconto de Frete (Regra: Itens com preço igual ou superior a R$ 5.000, possuem 40% de
desconto no frete.)

### Análises Gráficas:

1. Uma Análise de Pareto 80-20 com o Total de Frete por Estado de
Compra.

2. Total de Frete Acumuladas mês a mês exibindo todos os anos na tela.

3. Uma análise que exiba o Total de Frete do Ano Atual x Ano Anterior
mês a mês em conjunto com a taxa de crescimento exibindo todos os
anos na tela.

### Segmentações:

1. Ano/Mês
2. ID Pedido
3. ID Vendedor

---

## Medidas DAX

  <br>

  <img src="https://github.com/user-attachments/assets/f17cb283-71b2-49e3-a265-c5da255024f3"/>
  </div>

  <br>


---

 ### Frete Acumulado

  <img src="https://github.com/user-attachments/assets/d05cb166-aae5-4131-8896-4d1f5e899fa2"/>
  </div>
  
  <br>
  <br>
  
  * Função **DATESYTD**: Retorna uma tabela de coluna única que contém uma coluna das datas do ano até a data, no contexto atual.

  <br>

 ### Frete Acumulado Ano Anterior

  <img src="https://github.com/user-attachments/assets/fdb1d881-6b22-4e24-a294-f966405e97fb"/>
  </div>
  
  <br>
  <br>
  
  * Função **DATEADD**: Retorna uma tabela de coluna única que contém uma coluna de datas, deslocada para frente ou para trás no tempo pelo número especificado de intervalos   começando nas datas do contexto atual.
  
  <br>
  
  ### Porcentagem de Desconto de Frete

  <br>

   *1º Criado uma coluna calculada par aplicar a regra de négocio solicitada pelo CEO.*

  ***Regra: Itens com preço igual ou superior a R$ 5.000, possuem 40% de
     desconto no frete.***

  <br>
 
  <img src="https://github.com/user-attachments/assets/6feb2292-b0dd-4de5-8805-35f1a2c15a34"/>
  </div>
  
  
  <br>
  <br>

  *2º Filtrado as vendas superiores a 5K utilizando a função **CALCULATE***

  <br>
  
  <img src="https://github.com/user-attachments/assets/19c09427-2332-4c50-9fe4-0b34f09db8f2"/>
  </div>
  
  <br>
  <br>

  *3º Função **SUMX** para somar linha a linha, executando a multiplicação para chegar no resultado solicitado.*

  <br>
  
  
  <img src="https://github.com/user-attachments/assets/033d0a8b-dd63-419d-a302-5a82be181c60"/>
  </div>

  <br>
  <br>
  
  *4º Por ultimo usamos a função **DIVIDE** para calcular a porcentagem.*

  <br>

  ### Pareto com o Total de Frete por Estado de Compra.

  <br>
 
  *1º Criando Ranking dos Estados com maior valor de frete.*

  <br>

<div align="center">
<img src="https://github.com/user-attachments/assets/6b90004a-a3ca-4abc-bb5b-d5c63a6c4c60" />
</div>

<br>

* Função **RANKX:** Cria um ranking em ordem crescente

* Função **ALLSELECTED:** Garante que a função RANKX considere todos os estados ao criar o ranking com base na somatória de frete.

<br>

*2º Criando Valores Acumulados de Frete.*

<br>

<div align="center">
<img src="https://github.com/user-attachments/assets/1c1eae96-412d-42a2-99da-2a8d10b4abbd" />
</div>

<br>

* Para que obtenhamos os valores acumulados, precisamos aninhar função **TOPN** como argumento de filtro da Função **CALCULATE**.

* Função **TOPN:** retorna os N valores desejados de uma tabela especificada e acumula valores.

* Função **ALLSELECTED:** Garante que a função **TOPN** considere o ranking dos estados ao criar o acumulado na somatória de frete.

<br>

*3º Criando Percentual (%) Acumulado de Frete.*

<br>

<div align="center">
<img src="https://github.com/user-attachments/assets/27f911ce-6c60-4828-8773-a6ccdbbf7051" />
</div>

<br>

* Função **ALLSELECTED:** Garante que a função **DIVIDE** considere o valor total do frete por estados ao criar o percentual acumulado.

<br>

### Visualização:

 <img src="https://github.com/user-attachments/assets/89589f43-433f-45de-b540-1b641455d756"/>
 </div>


    

    
