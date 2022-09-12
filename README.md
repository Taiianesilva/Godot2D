
# Trabalho Prático: Jogo de Plataforma 2D usando Godot Engine

###  Prof. Edson M. Souza - 2022/2
Trabalho prático da disciplina de  JOGOS DIGITAIS, voltado ao desenvolvimento de um jogo de plataforma 2D usando Godot. 
- Coletar vários itens na cena - no mínimo 10
- Implementar nível de dificuldade para a coleta de itens
- Implementar danos ao jogador com base em um número de vidas inicial que, ao ser alcançado, finalize o jogo e mostre a pontuação obtida.

## Resultado Parcial
Visualize uma prévia do sistema em sua atual fase desenvolvimento através de imagens abaixo :)
<br>
## Configuração Inicial
Inicialmente, é feita a configuração da animação do personagem, tal como sua movimentação inicial nos eixos X e Y, conforme variáveis de velocidade, gravidade e força de pulo, além da função physics_process() do Godot Engine.

<img width="474" alt="image" src="https://user-images.githubusercontent.com/75912890/189549343-239e40d0-a4e0-4d13-a234-5e5d0f6753df.png">

## Tilemap, Layers e Colisões
Em sequência é criado um tilemap o qual é configurado conforme Assets baixados. São configuradas 4 camadas de jogo (Jogadores, Inimigos, Itens e Mundo) as quais são atribuidas aos objetos presentes no jogo. As colisões são ajustadas conforme as camadas e os tilemaps únicos. O resultado inicial é exibido abaixo.  

<img width="476" alt="image" src="https://user-images.githubusercontent.com/75912890/189704502-f965b978-afb3-4a8a-92b0-0b7c27034fbd.png">


