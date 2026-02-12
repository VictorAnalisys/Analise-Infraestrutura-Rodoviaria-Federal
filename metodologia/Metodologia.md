### Metodologia



1. ###### **Definição do Escopo Analítico**

O projeto foi delimitado à infraestrutura rodoviária federal concedida, considerando exclusivamente:

* Radares federais
* Praças de pedágio federais
* Extensão da malha rodoviária federal por UF

A delimitação do escopo foi uma decisão intencional para garantir:

* Coerência regulatória dos dados
* Comparabilidade entre estados
* Clareza na interpretação dos resultados

Evita-se, assim, a mistura de bases federais e estaduais, que possuem estruturas regulatórias distintas.



###### 

###### **2. Consolidação das Bases**

As bases de radares e pedágios foram integradas por meio de união (Union), e não relacionamento (Relationship).

Motivo da escolha:

* Ambas as bases representam pontos geográficos independentes.
* O objetivo era empilhar registros (infraestrutura total), e não cruzar informações linha a linha.
* O uso de Union evita multiplicações indevidas e conflitos de granularidade.



Foi criado um campo categórico:

***Tipo\_Ponto (Radar ou Pedágio)***

Essa variável permite análises segmentadas e comparativas dentro da mesma estrutura de dados.





###### **3. Construção do Indicador Absoluto**

Criou-se o indicador:

***Infraestrutura\_Total = Radares + Pedágios***

Esse indicador mede a presença absoluta de infraestrutura por estado.



Objetivo:

* Identificar concentração estrutural.
* Avaliar quais estados possuem maior volume operacionalmente relevante.

Limitação reconhecida:

* Estados maiores tendem a apresentar maior volume absoluto.
* O indicador isolado não controla o efeito do tamanho da malha.





###### **4. Construção do Indicador Proporcional**

Para evitar viés territorial, foi criado o indicador:

***Densidade de Infraestrutura por 100 km***



Fórmula:

Infraestrutura\_Total / Extensão\_km\_Federal \* 100



Justificativa da escala por 100 km:

* Mantém a proporcionalidade.
* Torna o indicador interpretável.
* Evita valores excessivamente pequenos.
* Facilita leitura executiva.

Objetivo do indicador proporcional:

* Medir intensidade estrutural.
* Avaliar fricção operacional relativa.
* Comparar estados de tamanhos diferentes de forma justa.



###### 

###### **5. Análise Bivariada (Volume vs Intensidade)**

Foi construído um gráfico de dispersão com:

* Eixo X → Infraestrutura Total (Volume)
* Eixo Y → Densidade por 100 km (Intensidade)

Linhas de referência com base na média nacional dividiram os estados em quatro perfis estratégicos:

1. Alta Infraestrutura + Alta Densidade
2. Alta Infraestrutura + Baixa Densidade
3. Baixa Infraestrutura + Alta Densidade
4. Baixa Infraestrutura + Baixa Densidade

Objetivo da classificação:

Identificar padrões estruturais e evitar análises simplistas baseadas apenas em ranking absoluto.

Essa abordagem permite:

* Detectar estados com infraestrutura diluída.
* Identificar corredores logísticos intensos.
* Avaliar potenciais níveis de fricção operacional.





###### **6. Interpretação Estratégica**

A análise não se limita à descrição dos dados.

Ela foi orientada por uma lógica operacional:

* Radares → Influenciam controle de velocidade e conformidade.
* Pedágios → Representam pontos fixos de custo e parada.

A combinação desses elementos foi interpretada como indicador de:

***Fricção Logística Potencial***

Estados com maior densidade estrutural podem exigir:

* Maior padronização operacional.
* Planejamento de tempo mais rigoroso.
* Monitoramento de desempenho.





###### **7. Limitações do Estudo**

* Não inclui rodovias estaduais.
* Não incorpora valores tarifários reais por praça.
* Não considera volume de tráfego ou fluxo de carga.

Essas limitações foram deliberadamente aceitas para manter consistência metodológica e foco no escopo federal.





###### **8. Direcionamento Futuro**

A estrutura analítica construída permite evolução natural para:

* Inclusão de tarifas reais por praça.
* Simulação de custo por rota.
* Análise de fricção logística estadual (ex.: São Paulo).
* Modelagem de risco operacional.



