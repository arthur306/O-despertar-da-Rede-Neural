# Soluções FarmTech – Etapa 6 | Reconhecimento de objetos com YOLO

Atividade 1: treinar, validar e testar um modelo YOLO para identificar dois tipos de objetos, controle e copo, comparando 30 e 60 épocas de treinamento.

Estudante: Arthur Michelini Medeiros Lopes - RM: 570598

---

Como dar o pontapé inicial

A solução completa, com o passo a passo detalhado, o código utilizado, os resultados obtidos e as análises realizadas, está disponível no notebook do Google Colab:

[Acessar o notebook no Colab](https://colab.research.google.com/drive/1CYqCBQhn620tJ-JcJlNj9PViav2ZCEyC?usp=sharing)

O arquivo .ipynb também pode ser encontrado neste repositório.

> Este README serve apenas como um ponto de partida. A descrição detalhada de cada fase está no notebook, para evitar a repetição de conteúdo.

Visão geral da solução

A FarmTech Solutions necessita de um sistema de visão computacional capaz de identificar objetos em imagens. Para verificar a eficácia da abordagem, esta atividade utiliza dois objetos distintos e avalia o impacto do número de épocas no desempenho do modelo.

Fase - O que é feito - Onde encontrar 
1. Conjunto de dados : 40 imagens de cada objeto, rotuladas no Make Sense e divididas em conjuntos de treino, validação e teste - Notebook, seções 1 e 2 
2. Configuração : Arquivo data.yaml com caminhos e classes; biblioteca Ultralytics (YOLOv11n) - Seções 3 e 4 
3. Treinamento : Dois modelos com os mesmos parâmetros, alterando apenas o número de épocas (30 e 60) - Seção 5 
4. Teste  Avaliação;  em imagens inéditas e demonstrações visuais de predições - Seções 5 e 6 
5. Comparação : Análise de erro, tempo de treinamento, precisão, recall e mAP - Seções 7 e 8 

Conjunto de dados

Divisão - Imagens por objeto - Total
Treino (32 | 64 )
Validação ( 4 | 8 )
Teste ( 4 | 8 )

Classes: 0 = controle, 1 = copo. Formato das anotações: YOLO (classe, coordenadas x e y do centro, largura e altura, normalizadas).

Resultado resumido

O modelo treinado por 60 épocas demonstrou ser mais confiável na identificação da classe correta no conjunto de teste, embora tenha exigido aproximadamente o dobro do tempo de treinamento (cerca de 0,81 h contra 0,41 h, em CPU). Dado o tamanho reduzido do conjunto de dados, os resultados são meramente indicativos; detalhes completos e ressalvas podem ser encontrados na seção 8 do notebook.

Como replicar:

1. Acesse o notebook no Google Colab.
2. Conecte o Google Drive e organize o conjunto de dados na estrutura Fase 6/Dataset/images | labels/(train,val,test).
3. Execute as células na ordem apresentada. O notebook gerará o arquivo data.yaml, treinará os dois modelos e salvará os resultados em Fase 6/results.

Tecnologias utilizadas:

Python - Google Colab - Ultralytics YOLOv11n - Pandas - Make Sense (para anotação)

Vídeo explicativo:
(COLE_AQUI_O_LINK_DO_VIDEO)
