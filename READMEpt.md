# Project 201

## Geral

Este projeto prevê a probabilidade de vitória na próxima partida de Valorant **com base no mapa**, utilizando:
- **Padrões Temporais** → Aprende com sequências de vitórias/derrotas com base em tendências de desempenho.
- **Características** → Avalia e prevê com base no mapa, agente, eliminações, mortes e assistências, e prevê a probabilidade de vitória e o KDA esperado.
- **Combinação Híbrida** → Calcula a média das probabilidades de ambos os modelos para uma recomendação mais realista.

## Operação

### Requisitos
- Python 3.9+ (recomendado).
- Conhecimento básico da linha de comando/terminal.
- Arquivo de informações
## Funcionamiento

- ## Instalação no Windows
1. Baixe e instale o Python da Microsoft Store (https://apps.microsoft.com/detail/9PNRBTZXMB4Z?hl=neutral&gl=CL&ocid=pdpshare)
2. Abra o Prompt de Comando (CMD) e digite:
```bash
pip install pandas numpy scikit-learn xgboost torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
```
3. Após a conclusão, coloque os 3 arquivos em uma pasta e navegue pelo Prompt de Comando até a pasta do projeto:
```bash
cd %pasta%
```
## Instalação no Linux/Mac
1. Baixe e instale o Python do site do macOS (https://www.python.org/downloads/macos/)
2. Abra o Prompt de Comando (CMD) e digite:
```bash
pip install pandas numpy scikit-learn xgboost torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
``` Nota: Se isso não funcionar, entre em um ambiente virtual:
```bash
python -m venv .venv
source .venv/bin/activate
```
3. Depois de concluído, coloque os 3 arquivos em uma pasta e acesse a pasta do projeto:
```bash
cd %pasta%
```
## Para exportar seus dados de jogo para um arquivo CSV
1. Acesse [tracker.gg/valorant](https://tracker.gg/valorant) e encontre seu perfil.

2. Baixe e carregue quantos jogos quiser (recomendado: pelo menos 100)
3. Baixe a página clicando com o botão direito em qualquer espaço em branco na página
4. Abra o arquivo .htm, copie tudo com Ctrl+A e cole em um arquivo .txt, usando seu ID da Riot como nome do arquivo (exemplo: astato#86.txt)
5. Coloque o arquivo yourID.txt dentro da pasta com todo o projeto
6. Execute launch.py ​​no CMD/terminal:
```bash
python launch.py
```
#### Somente no Linux/Mac
Observação: Se isso não funcionar, entre em um ambiente virtual:
```bash
python -m venv .venv
source .venv/bin/activate
```
7. Selecione a opção 2, usando o mesmo ID do arquivo yourID.txt anterior.

8. Agora você tem um arquivo .csv com o mesmo nome de antes, ID.csv

## Usando no Windows:
1. Abra o CMD e vá para a pasta do seu projeto.

2. Execute o launch.py:
```bash
python launch.py
```
3. Escolha a opção 1 e insira o mesmo ID do arquivo .csv anterior (seu ID da Riot).

4. Escolha o mapa digitando o nome dele!
## Usando no Linux/Mac:
1. Abra o CMD e navegue até a pasta do seu projeto.

2. Execute o launch.py:
```bash
python launch.py
```
Observação: Se isso não funcionar, entre no ambiente virtual:
```bash
python -m venv .venv
source .venv/bin/activate
```
3. Escolha a opção 1 e insira o mesmo ID do arquivo .csv (seu ID da Riot).
4. Escolha o mapa digitando o nome dele!

## Saída
Previsões finais para a próxima partida (todos os agentes jogados neste mapa):
Map: Ascent
  - Jett | Win Probability 0.72 | Expected KDA 2.10
  - Reyna | Win Probability 0.65 | Expected KDA 1.95
  - Killjoy | Win Probability 0.60 | Expected KDA 1.80
## Considerações
1. O modelo prevê partidas com base nas partidas carregadas do arquivo .csv. Recomenda-se atualizar o arquivo .csv a cada partida jogada para obter melhores resultados. Por enquanto, você precisa sobrescrever o arquivo .csv manualmente, adicionando uma nova linha no formato mostrado.
2. O modelo NÃO é 100% perfeito, pois é uma versão alfa. Com base em minhas pesquisas, estimo que ele tenha uma taxa de precisão de 65% a 80%.
3. Se o modelo prever todas as derrotas, recomendo testar um novo agente que você ainda não tenha usado nesse mapa.

## Projeções Futuras Conhecidas
1. Interface do Usuário
2. Aprendizado com a partida atual
3. Atualização automática do arquivo CSV
4. Uso da GPU
## Atenciosamente
Agradecimentos especiais a Revit e Magiñho por serem os participantes dos testes.
amassando regularmente na área
