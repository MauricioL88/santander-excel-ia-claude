# Desafio Calculadora de Imposto de Renda

Projeto do desafio da DIO (Digital Innovation One) para cálculo e organização de informações para declaração de Imposto de Renda.

## Arquivo: `Informa_Leao.xlsx`

Planilha Excel com 4 abas para organização de dados financeiros e pessoais:

### Aba 1: TITULAR
Dados pessoais do contribuinte:
- Nome, CPF, data de nascimento, título de eleitor
- Dados do cônjuge
- Endereço completo (rua, CEP)
- Contato (telefone, celular, email)
- Informações sobre alterações e dependência do cônjuge
- Status de residente no exterior

### Aba 2: INFORMES
Informes de rendimentos bancários com:
- Cadastro de até 3 bancos
- Código do banco (lista com +150 opções)
- Valor atual de cada conta
- Anexo de comprovantes (PDF)
- **Fórmula**: `SUM(D11,D17,D23)` para totalizar os valores
- **Total**: R$ 1.751.500,00

Bancos cadastrados:
| Banco | Valor |
|-------|-------|
| 748 - Banco Cooperativo SICREDI S.A. | R$ 1.725.000,00 |
| 237 - Banco Bradesco S.A. | R$ 1.500,00 |
| 033 - Banco Santander (Brasil) S.A. | R$ 25.000,00 |

### Aba 3: NOTAS
Registro de notas bancárias ou extratos de holerites:
| Data | Categoria | Valor |
|------|-----------|-------|
| (data) | HOLERITE | R$ 3.500,00 |
| (data) | CNPJ | R$ 10.000,00 |

### Aba 4: TABELA (oculta)
Lista de referência com todos os bancos autorizados pela CNSFN (001 a 757).

## Recursos da Planilha
- **3 imagens** (PNG) - possivelmente logos ou ilustrações
- **2 gráficos** - para visualização dos dados financeiros
- **1 tabela** - lista de referência de bancos
- **Fórmulas** - cálculo automático de totais

## Objetivo
Auxiliar na organização e preparação de dados para a declaração anual do Imposto de Renda, facilitando:
- Cadastro de dados pessoais
- Registro de informes de rendimentos de múltiplos bancos
- Controle de entradas e notas fiscais
- Geração automática de totais
