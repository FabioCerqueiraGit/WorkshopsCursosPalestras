# Fórmulas DAX Power BI

## Acumulado de Vendas por dia, mês e ano

### CALCULA O TOTAL DE VENDAS ACUMULANDO POR DIA
Total Vendas YTD = 
CALCULATE(
     [TOTAL VENDAS];
     DATESYTD(DATA[DATA])
)

### CALCULA O TOTAL DE VENDAS MÊS PASSADO
Total Vendas LM =
CALCULATE(
     [Total Vendas];
     DATEADD(
         Data[Data];
         -1;
         MONTH
     )
 )   

### CALCULA O TOTAL DE VENDAS ANO PASSADO
Total Vendas LY =
CALCULATE(
     [Total Vendas];
     SAMEPERIODLASTYEAR(Data[Data])
 )   

### CALCULA A % DE CRESCIMENTOD DE VENDAS COMPARADO AO MÊS PASSADO 
MoM % = DIVIDE([Total Vendas]; [Total Vendas LM])

### CALCULA A % DE CRESCIMENTOD DE VENDAS COMPARADO AO ANO PASSADO 
YoY % = DIVIDE([Total Vendas]; [Total Vendas LY])
