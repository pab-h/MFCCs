# MFCC de Sinais de Voz

Este repositório contém a implementação completa do cálculo dos **Coeficientes Cepstrais de Frequência Mel (MFCC)** aplicados a sinais de voz, desenvolvida como atividade prática da disciplina **Processamento Digital de Sinais (PDS)**.

O objetivo principal do trabalho é avaliar se os MFCC são capazes de **caracterizar e distinguir sinais de fala**, utilizando como exemplo dois áudios correspondentes às palavras **“sim”** e **“não”**.

## 🎯 Objetivos

- Implementar passo a passo o pipeline clássico de extração de MFCC;
- Analisar sinais de voz nos domínios do tempo e da frequência;
- Avaliar o impacto de cada etapa do processamento (pré-ênfase, janelamento, escala Mel, DCT);
- Verificar se os MFCC são eficazes para diferenciar sinais de fala distintos.

## 📂 Estrutura do Repositório

```

.
├── sim.wav                  # Áudio da palavra "sim"
├── nao.wav                  # Áudio da palavra "não"
├── MFCC_Voz.ipynb           # Notebook com a implementação completa
├── README.md                # Documentação do projeto

````

> ⚠️ O notebook deve ser executado com os arquivos `.wav` na mesma pasta.


## 🔍 Etapas Implementadas

O notebook executa automaticamente todas as etapas solicitadas no trabalho:

1. **Leitura e visualização dos sinais de áudio**
2. **Análise espectral via FFT**
3. **Filtro de pré-ênfase (α = 0,95)**  
4. **Remoção da média (componente DC)**
5. **Segmentação em frames de 10 ms**
6. **Aplicação da janela de Hamming**
7. **Cálculo da DFT e energia espectral**
8. **Aplicação de 40 filtros triangulares na escala Mel**
9. **Cálculo da energia e do log da energia Mel**
10. **Transformada Discreta do Cosseno (DCT)**
11. **Extração dos 16 primeiros MFCC**
12. **Concatenação dos MFCC de todos os frames**
13. **Análise comparativa dos sinais**

Cada etapa possui **comentários explicativos e gráficos**, permitindo fácil compreensão e correção.


## 📈 Resultados e Conclusão

Os resultados mostram que:

- A energia dos sinais de fala está majoritariamente concentrada nas baixas frequências;
- A escala Mel modela adequadamente a percepção auditiva humana;
- A DCT concentra a informação relevante nos primeiros coeficientes;
- Os vetores MFCC concatenados apresentam padrões distintos para os sinais “sim” e “não”.

📌 **Conclusão:**  
Os MFCC se mostraram uma ferramenta **eficiente e robusta** para a caracterização e distinção dos sinais de voz analisados.

## ▶️ Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/mfcc-sinais-de-voz.git
````

2. Instale as dependências:

```bash
pip install numpy scipy librosa matplotlib
```

3. Abra o notebook:

```bash
jupyter notebook MFCC_Voz.ipynb
```

4. Execute todas as células para gerar os gráficos e resultados.

