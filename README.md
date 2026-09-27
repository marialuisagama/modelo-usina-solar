# Modelo de Viabilidade de uma Usina Solar

Projeção de fluxo de caixa, valuation e análise de sensibilidade de uma usina solar de 10 MW, com capex de R$ 35 milhões e 25 anos de operação. O objetivo é responder se o projeto vale a pena e quais premissas mais influenciam essa decisão.

## Principais resultados

| Métrica | Valor |
|---|---|
| VPL | −R$ 3,39 milhões |
| TIR | 13,03% a.a. |
| Taxa de desconto (nominal) | 14,40% a.a. |

Nas premissas atuais, o projeto não deve ser aprovado: a TIR fica 1,37 p.p. abaixo da taxa exigida. O projeto é rentável, mas não o suficiente para remunerar o risco que carrega.

<img width="1169" height="680" alt="image" src="https://github.com/user-attachments/assets/72d7985b-4777-4cd3-afe7-110e50eed88b" />

O projeto está próximo do ponto de viabilidade: uma variação de cerca de 10% no capex, na taxa de desconto, na tarifa ou no fator de capacidade leva o VPL a zero. O custo de O&M tem baixa elasticidade e altera pouco o resultado. Dessa forma, o projeto se torna viável com capex de até R$ 31,6 milhões ou tarifa inicial de pelo menos R$ 218/MWh, mantidas as demais premissas.

## Metodologia

1. **Projeção do fluxo de caixa:** geração diminui com a degradação das placas, tarifa e custo de O&M sobem com a inflação (IPCA).
2. **Taxa de desconto:** NTN-B de longo prazo (custo de oportunidade sem risco) + prêmio de risco do projeto, convertida para taxa nominal para manter consistência com os fluxos.
3. **Valuation:** cálculo de VPL, TIR e payback descontado, com verificação cruzada entre o cálculo manual e a biblioteca numpy-financial.
4. **Análise de sensibilidade:** variação de −20% a +20% em cada premissa, para medir o impacto de cada uma no VPL.

## Premissas

Meramente ilustrativas, baseadas em médias e estimativas de mercado.

| Premissa | Valor |
|---|---|
| Capacidade instalada | 10 MW |
| Fator de capacidade | 25% |
| Degradação das placas | 0,5% a.a. |
| Tarifa inicial | R$ 200/MWh |
| IPCA | 4% a.a. |
| Custo de O&M (ano 1) | R$ 600 mil/ano |
| Capex | R$ 35 milhões |
| Vida útil | 25 anos |
| Juro real livre de risco | 7% a.a. (referência: Tesouro IPCA+ 2050, set/2026) |
| Prêmio de risco | 3% a.a. (ilustrativo) |

## Limitações

- Não considera impostos nem estrutura de financiamento (projeto 100% financiado com capital próprio).
- IPCA constante ao longo dos 25 anos.
- Prêmio de risco definido de forma ilustrativa.
- Não considera custos de conexão à rede nem valor residual da usina.

## Próximos passos

- Calibrar as premissas com dados públicos (geração real de usinas solares pelo ONS e preços de leilões de energia pela ANEEL).
- Importar as premissas de uma planilha externa.
- Incluir estrutura de financiamento com dívida.

## Ferramentas

Python · pandas · NumPy · numpy-financial · matplotlib · Google Colab

## Autora

Maria Luisa Gama · [LinkedIn](https://www.linkedin.com/in/maria-luisa-gama-2619ba309)
