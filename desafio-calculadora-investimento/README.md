# Calculadora de Investimento — calculaInvest.xlsx

Aplicação em planilha Excel que simula investimentos mensais em **FIIs (Fundos de Investimento Imobiliário)**, projetando o patrimônio acumulado, os dividendos mensais e sugerindo a alocação da carteira conforme o perfil do investidor.

## Como funciona

Basta preencher as células de configuração na aba **Calculadora**. Todos os cálculos são automáticos, baseados em **intervalos nomeados** (`Salario`, `SugestInvest`, `Aporte`, `Anos`, `Taxa`, etc.) e nas funções financeiras do Excel.

## Funcionalidades

### 1. Configurações
| Campo | Descrição |
|---|---|
| **Salário** | Renda mensal do usuário (ex.: R$ 2.309) |
| **Rendimento Carteira** | Rendimento estimado da carteira (ex.: 1%) |
| **Sugestão de investimento (30%)** | Calcula automaticamente 30% do salário como valor sugerido para aportar |

### 2. Investimento Mensal
- **Quanto investir por mês?** — usa a sugestão de 30% do salário.
- **Por quantos anos?** — horizonte de tempo do investimento (ex.: 6 anos).
- **Taxa de rendimento mensal?** — taxa média esperada ao mês (ex.: 1,079%).
- **Patrimônio acumulado?** — calculado com a função financeira `FV` (Valor Futuro):
  ```
  =FV(Taxa; Anos*12; -Aporte)
  ```
- **Dividendos mensais?** — patrimônio acumulado × taxa mensal de rendimento.

### 3. Cenários
Tabela de projeção do patrimônio acumulado e dos dividendos correspondentes para os prazos de **2, 5, 10, 15, 20, 25, 30 e 35 anos**, permitindo visualizar o efeito dos juros compostos no longo prazo.

### 4. Alocação por Perfil de Investidor
A partir de um menu suspenso (validação de dados) com os perfis **Conservador**, **Moderado** ou **Agressivo**, a planilha divide o aporte mensal entre os 6 tipos de FIIs usando `PROCV` (`VLOOKUP`):

- Papel (CRIs / recebíveis)
- Tijolo (imóveis físicos)
- Híbridos
- FOFs (fundos de fundos)
- Desenvolvimento
- Hotelarias

## Estrutura das Abas

### `Calculadora`
Painel principal da aplicação, com as seções: Configurações, Investimento Mensal, Cenários e alocação da carteira por perfil.

### `Tb_Apoio`
Tabela de apoio (lookup) com a matriz de distribuição percentual por perfil × tipo de FII:

| Perfil | Papel | Tijolo | Híbridos | FOFs | Desenvolvimento | Hotelarias |
|---|---|---|---|---|---|---|
| Conservador | 30% | 50% | 10% | 10% | 0% | 0% |
| Moderado | 32% | 35% | 8% | 5% | 10% | 10% |
| Agressivo | 50% | 10% | 5% | 5% | 20% | 10% |

## Requisitos

- Microsoft Excel (ou software compatível com `.xlsx`, como LibreOffice Calc / Google Sheets)

## Como usar

1. Abra o arquivo `calculaInvest.xlsx`.
2. Na aba **Calculadora**, informe seu salário, os anos de investimento e a taxa de rendimento mensal.
3. Selecione seu perfil de investidor no menu suspenso.
4. Analise o patrimônio projetado, os dividendos mensais e a sugestão de alocação por tipo de FII.
