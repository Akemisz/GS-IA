# GS IA
## Descrição do problema

Os recifes de coral são ecossistemas vitais para a saúde dos oceanos e a biodiversidade marinha, e enfrentam ameaças significativas, com destaque para o fenômeno do branqueamento em larga escala. O branqueamento ocorre quando os corais perdem suas algas simbióticas devido a estresses ambientais como aumento da temperatura da água e poluição, enfraquecendo os corais e impactando negativamente todo o ecossistema marinho. Além disso, a perda de corais afeta diretamente comunidades humanas que dependem dos oceanos para alimentação, emprego e proteção contra desastres naturais. É essencial implementar medidas eficazes para proteger e preservar os recifes de coral e os ecossistemas marinhos em geral.

## Solução Proposta

A solução proposta é uma plataforma de monitoramento de recifes de coral que permite aos usuários fazer upload de fotos de corais, fornecendo informações como localização, nome do observador, país e profissão. Esses dados são armazenados em um banco de dados centralizado, enquanto as imagens são analisadas por algoritmos de inteligência artificial para determinar se os corais estão saudáveis ou apresentam sinais de branqueamento. A plataforma facilita o monitoramento colaborativo dos recifes de coral em tempo real e promove a interação entre a comunidade e as empresas de conservação, contribuindo para a proteção e preservação desses importantes ecossistemas marinhos.

## Classificação de Imagens com Redes Neurais Convolucionais (CNNs)

## Carregamento e Pré-processamento dos dados:

### IMAGENS DE CORAIS

- As imagens do conjunto de dados são carregadas usando o TensorFlow's ImageDataGenerator, que permite carregar imagens diretamente do disco em lotes. Essas mesmas imagens são redimensionadas para um tamanho comum de (224, 224) e normalizadas para o intervalo [0, 1], e divididas em conjuntos de treinamento e validação usando train_test_split.

### CONSTRUÇÃO DO MODELO CNN

- Um modelo de Rede Neural Convolucional (CNN) é construído usando a API funcional do Keras. O modelo possui várias camadas convolucionais e de pooling, seguidas por camadas totalmente conectadas. É utilizado em seguida um modelo pré-treinado, VGG19, como base para extração de características. Logo em seguida são adicionadas camadas de aumento de dados para aplicar transformações aleatórias durante o treinamento, como rotação, zoom e flip horizontal. Já as camadas densas são adicionadas para classificar as imagens em suas respectivas classes.

### TREINAMENTO E AVALIAÇÃO

- O modelo foi compilado com uma função de perda de entropia cruzada categórica e otimizador Adam. Utilizando o método fit() do Keras, com EarlyStopping, ModelCheckpoint e ReduceLROnPlateau como callbacks para monitorar e ajustar o treinamento. A performance do modelo é avaliada usando dados de validação e o conjunto de teste separado, e as métricas de acurácia e perda são registradas ao longo do treinamento e exibidas em gráficos para análise.

### Resultados obtidos:

- O modelo CNN treinado demonstrou um bom desempenho na tarefa de classificação de imagens de corais.
A acurácia do modelo alcançou 72% no conjunto de teste.

- Os gráficos de treinamento e validação mostraram uma boa convergência do modelo, com a perda diminuindo e a acurácia aumentando ao longo das épocas.

- As previsões do modelo foram consistentes e precisas, comprovadas pela avaliação do conjunto de teste e observações visuais das imagens classificadas.

### Conclusão dos resultados

## Video Pitch e funcionalidades do codigo
link do video
















