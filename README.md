# CDI-Profitability
**Documentação do Código**

Este documento descreve o código em Python para calcular os retornos acumulados de um investimento com base em dados da taxa SELIC (Sistema Especial de Liquidação e de Custódia) fornecidos pelo Banco Central do Brasil. O código também identifica o intervalo de datas de maior retorno e plota o gráfico dos retornos acumulados ao longo do tempo.

**Tecnologias utilizadas:**
- **Python:** Linguagem de programação utilizada para escrever o código.
- **NumPy:** Biblioteca utilizada para trabalhar com arrays e realizar cálculos numéricos eficientes.
- **Matplotlib:** Biblioteca utilizada para a criação de gráficos e visualizações dos dados.
- **bcb:** Biblioteca desenvolvida por terceiros para acessar os dados do Banco Central do Brasil.

**Descrição do Código:**

1. **Importação de Bibliotecas:** O código inicia importando as bibliotecas necessárias para o funcionamento do programa.

2. **Função `checking_dates_and_frequency()`:** Essa função é responsável por solicitar ao usuário as informações sobre o investimento, incluindo o capital investido, a frequência desejada para os cálculos e as datas inicial e final para análise. Ela retorna essas informações para serem utilizadas posteriormente no código.

3. **Função `challenge(selic, capital, start_date, end_date, frequency)`:** Essa função é a principal do código e realiza o cálculo dos retornos acumulados do investimento com base nos dados da taxa SELIC. Os passos realizados nesta função são:
    - Filtrar os dados da taxa SELIC para o intervalo de datas fornecido pelo usuário.
    - Calcular os retornos acumulados diários com base na taxa SELIC.
    - Resample (agrupar) os dados para a frequência especificada pelo usuário (mensal, trimestral, etc.).
    - Calcular o valor acumulado do investimento ao longo do tempo e o lucro acumulado em relação ao capital inicial.
    - Imprimir os resultados dos cálculos.

4. **Função `question(selic)`:** Essa função realiza a análise dos retornos acumulados ao longo do tempo e identifica o intervalo de datas de maior retorno. Os passos realizados nesta função são:
    - Filtrar os dados da taxa SELIC para o período de interesse (data inicial: 01/01/2000 e data final: 31/03/2022).
    - Calcular os retornos acumulados diários com base na taxa SELIC.
    - Calcular os retornos acumulados para janelas de 500 dias.
    - Plotar o gráfico dos retornos acumulados ao longo do tempo.
    - Identificar o intervalo de datas de maior retorno.
    - Plotar o gráfico dos retornos acumulados para o intervalo de maior retorno.

5. **Execução do Código:** O código solicita ao usuário as informações sobre o investimento (capital, frequência e intervalo de datas), obtém os dados da taxa SELIC do Banco Central do Brasil e chama as funções `challenge(selic, capital, start_date, end_date, frequency)` e `question(selic)` para realizar os cálculos e análises necessárias.

O código permite ao usuário obter informações importantes sobre os retornos acumulados de um investimento com base em dados da taxa SELIC, além de visualizar graficamente a evolução desses retornos ao longo do tempo.

**Observações:**
- Certifique-se de ter instaladas as bibliotecas necessárias (NumPy, Matplotlib e bcb) antes de executar o código.
- O código assume que o usuário fornecerá datas válidas e que a API do BCB está funcionando corretamente para obter os dados da taxa SELIC.
- Verifique se o ambiente gráfico do seu sistema está configurado corretamente para plotar os gráficos do Matplotlib. Caso ocorram problemas de renderização gráfica, consulte a documentação do Matplotlib para solucionar problemas relacionados à configuração do ambiente gráfico.
- É importante lembrar que a biblioteca `bcb` foi desenvolvida por terceiros e pode estar sujeita a mudanças não previstas pelos desenvolvedores do código.

**Recomendações de Uso:**
- Utilize o código em um ambiente Python configurado corretamente e certifique-se de ter as dependências instaladas corretamente.
- Insira dados válidos ao executar o código, como um valor numérico para o capital investido, uma frequência válida (como "M" para mensal) e datas dentro do intervalo permitido (inicial maior que 01/01/1995 e final menor que a data atual).
