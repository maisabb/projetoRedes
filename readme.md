# Jogo de Damas em Rede 🛡️
Este é um projeto de um jogo de damas multiplayer em Python, usando Sockets TCP e Threads.
### 1. Pré-requisitos
Antes de rodar, você precisa ter o Python 3 e a biblioteca Pygame instalados.
Se você não tem o Pygame, instale-o usando o pip:
pip install pygame


### 2. Como Rodar a Aplicação (em localhost) 🔧
Para testar o jogo no seu próprio computador, você precisará abrir 3 (três) janelas de terminal ou prompt de comando.
A ordem é importante:
#### Passo 1: Rodar o Servidor (Terminal 1)
Na primeira janela de terminal, execute o server.py. Ele ficará "preso", esperando por conexões.
python server.py. O servidor irá mostrar quando os jogadores se conectarem.
#### Passo 2: Rodar o Jogador 1 (Terminal 2)
Na segunda janela de terminal, execute o client.py.
python client.py. Uma janela do Pygame irá abrir. Ela ficará esperando o segundo jogador.
#### Passo 3: Rodar o Jogador 2 (Terminal 3)
Na terceira janela de terminal, execute o client.py novamente.
python client.py. Uma segunda janela do Pygame irá abrir. Assim que este cliente se conectar ao servidor, o jogo começará em ambas as janelas.
### 3. Como Rodar em Computadores Diferentes (Rede Local) 🔧
Se você quiser jogar com um colega em outro computador na mesma rede (ex: mesmo Wi-Fi):
Encontre o IP do Servidor: No computador que vai rodar o server.py, descubra o seu "Endereço IPv4".
No Windows: abra o cmd e digite ipconfig.
No Mac/Linux: abra o terminal e digite ifconfig ou ip a.
(Ex: 192.168.1.10)
Altere o Código:
Em server.py: mude HOST = 'localhost' para HOST = '0.0.0.0' (isso faz o servidor aceitar conexões de fora).
Em client.py: mude HOST = 'localhost' para o IP do computador do servidor (ex: HOST = '192.168.1.10').
Execute:
O Jogador 1 (em seu computador) roda o server.py e depois o client.py.
O Jogador 2 (no outro computador) roda apenas o client.py (que deve estar com o código já alterado).
