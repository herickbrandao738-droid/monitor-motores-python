# monitor-motores-python

# **Relatório escrito do monitoramento realizado**

Nesse relatório será tratado quais foram os valores encontrados, situação dos motores, e quais providências devem ser tomadas.

Motor | Setor | Status
:--- | :---: | ---:
MTR-01 | Estamparia | Normal
MTR-02 | Usinagem | Crítico
MTR-03 | Bobinagem | Atenção
MTR-04 | Pintura | Normal

## Motores em situação Normal

Motor | Temp. | Corr. | Vib. | RPM
:--- | :---: | :---: | :---: | ---:
MTR-01 | 68.4 C | 14.2 A | 2.1 mm/s | 1750
MTR-04 | 61 C | 11.5 A | 1.8 mm/s | 1780

## Motores em situação de Atenção

Motor | Temp. | Corr. | Vib. | RPM
:--- | :---: | :---: | :---: | ---:
MTR-03 | 76.2 C | 17.8 A | 4.7 mm/s | 1520
---
**_RISCO_**: Vibracao elevada (4.7 mm/s)

## Motores em situação CRÍTICA

Motor | Temp. | Corr. | Vib. | RPM
:--- | :---: | :---: | :---: | ---:
MTR-02 | 84.7 C | 19.3 A | 5.2 mm/s | 1690
---
**_RISCO_**: Superaquecimento (84.7 C)

**_RISCO_**: Sobrecorrente (19.3 A)

**_RISCO_**: Vibracao elevada (5.2 mm/s)

## Medidas a serem tomadas

- [ ] MTR-03 / _Diminuir Vibração_
- [ ] MTR-04 / _Diminuir Temperatura_
- [ ] MTR-04 / _Diminuir Nível de Corrente_
- [ ] MTR-04 / _Diminuir Vibração_

# Explicação do Código

    Este código foi feito para poder realizar um diagnóstico dos motores da indústria, para que esse diagnóstico pudesse ser realizado, foram atribuidos valores a variáveis. Esses valores influeniam diretamente no número de alertas que a máquina possui, se ela está com 0 alertas, seu Status é NORMAL, se houver 1 alerta, o status é ATENCAO, e se houver mais do que isso, a Máquina está em situação crítica. O princípio é esse, mas para deixar o código esteticamente mais bonito, foram adicionados detalhes como uma tabela com os valores, data e horário da leitura, versão do Monitoramento e "---" para ser possível separar os elementos. 