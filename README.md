##ASFF-Net: Attention-based Spatial Feature Fusion Network ✈️🧠

Este repositório contém o código-fonte, artigo científico e apresentação do projeto ASFF-Net, desenvolvido para a previsão da Vida Útil Restante (RUL - Remaining Useful Life) de motores turbofan da NASA.

📌 Visão Geral do Projeto

A manutenção preditiva aeroespacial enfrenta um desafio crítico: as métricas tradicionais de erro (como o MSE) penalizam de forma simétrica previsões precoces e tardias. No mundo real, prever que um motor vai falhar mais tarde do que a realidade resulta em falhas catastróficas.

A ASFF-Net aborda este problema introduzindo três inovações principais:

Atenção Espacial Dinâmica: Pondera automaticamente os sensores mais críticos com base no contexto temporal da janela.

Fusão de Rotas Paralelas (LSTM + CNN 1D): Combina a memória de longo prazo da LSTM com a deteção de anomalias abruptas da CNN.

Função de Perda Assimétrica: Uma métrica orientada ao risco que penaliza severamente superestimações, forçando o modelo a adotar um comportamento conservador e seguro.

📊 Dataset

O modelo foi treinado e avaliado no conjunto de dados CMAPSS (FD001) da NASA.

Aviso: Devido ao tamanho do dataset, os dados brutos não estão incluídos neste repositório.
Pode descarregar os dados originais através deste link no Kaggle: NASA CMAPSS Turbofan Engine Degradation

📁 Estrutura do Repositório

/codigo: Scripts em Python para pré-processamento, EDA, arquitetura da rede, treino e avaliação.

/artigo: Código LaTeX e PDF final do artigo científico (5 páginas, estilo NeurIPS).

/apresentacao: Ficheiro PowerPoint e o script Python utilizado para gerar os slides iniciais.

🚀 Como Executar

Clone este repositório:

git clone [https://github.com/SEU-USUARIO/ASFF-Net.git](https://github.com/SEU-USUARIO/ASFF-Net.git)


Instale as dependências necessárias:

pip install pandas numpy matplotlib scikit-learn tensorflow python-pptx


Descarregue o dataset do Kaggle e coloque-o na pasta local. Atualize a variável caminho_arquivo no ficheiro modelo_asff_net.py.

Execute o script principal:

python codigo/modelo_asff_net.py


📈 Principais Resultados

No conjunto de teste oficial da NASA (FD001):

MAE: 12.45 ciclos

RMSE: 15.97 ciclos

Score NASA: 36.756 (Viés conservador de segurança)

✍️ Autores

Ryan Gabriel Elesbão - Universidade Federal de Uberlândia (UFU)
