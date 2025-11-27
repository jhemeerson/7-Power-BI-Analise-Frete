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

* Frete Acumulado

    <img src="https://github.com/user-attachments/assets/d05cb166-aae5-4131-8896-4d1f5e899fa2"/>
    </div>

    <br>

    *Função DATESYTD: Retorna uma tabela de coluna única que contém uma coluna das datas do ano até a data, no contexto atual.*

  <br>

* Frete Acumulado Ano Anterior

    <img src="https://github.com/user-attachments/assets/fdb1d881-6b22-4e24-a294-f966405e97fb"/>
    </div>

    <br>

    *Função DATEADD: Retorna uma tabela de coluna única que contém uma coluna de datas, deslocada para frente ou para trás no tempo pelo
    número especificado de intervalos começando nas datas do contexto atual.*

  <br>
