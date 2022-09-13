
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

## Tilemap, Layers, Colisões, Animações e Raycast
Em sequência é criado um tilemap o qual é configurado conforme Assets baixados. São configuradas 4 camadas de jogo (Jogadores, Inimigos, Itens e Mundo) as quais são atribuidas aos objetos presentes no jogo. As colisões são ajustadas conforme as camadas e os tilemaps únicos.
Foram feitos ajustes no processo de animação do jogador, tal como em seu formato de pulo. São criadas animações associadas ao movimento de corrida do jogador, tal como de pulo e recebimento de ataque. Ademais, é feita a configuração de alternância entre as animações através da alteração do arquivo de Scripts do player. Por fim, são incluídos raycasts no personagem para controlar a colisão do mesmo com o chão, de modo que o pulo só possa ocorrer caso o jogador esteja em alguma superfície, não "pulando infinitamente". Os resultados são expostos em sequência.

<img width="476" alt="image" src="https://user-images.githubusercontent.com/75912890/189704502-f965b978-afb3-4a8a-92b0-0b7c27034fbd.png">

## Câmera 2D e Limites
Para o contexto de jogo, é desejado que a câmera acompanhe o jogador com suavidade, mostrando partes do cenário que estão próximas do mesmo e deixado de lado áreas fora do limite da tela de jogo. Para tanto, cria-se um elemento "Câmera 2D" na aba do jogador; a mesma terá a opção "current" ativada, além das ferramentas de "smoothing". Os resultados, juntamente com um remanejamento do mapa.

<img width="943" alt="image" src="https://user-images.githubusercontent.com/75912890/189755220-c0f18434-ba99-44e1-a7a4-1d257fd6d9dc.png">


## Parallax Background
São diferentes camadas do plano de fundo do jogo, utilizando os Assets Seasonal Tilesets e os nós "Parallax Background" e "Parallax Layers" da Engine Godot. Os diferentes elementos do conjunto de assets foram organizados como texturas de diferentes "Parallax Layers" e então ordenados conforme sua posição. O ajuste à tela foi feito através de configurações de escala e espelhamento, tal como movimentação manual.

<img width="531" alt="image" src="https://user-images.githubusercontent.com/75912890/189769665-a664b985-a74e-4441-bd84-ae3f0a033179.png">

## Falling Platforms
Aumento de dificuldade, foram criadas neste itens plataformas as quais "caem" após terem contato com o jogador. Tal função foi implementada através de uma verificação de colisão em adição a um timer e uma verificação de fim de animação. Após alguns segundos, a plataforma caída é restaurada à sua posição e animação originais

<img width="571" alt="image" src="https://user-images.githubusercontent.com/75912890/189978294-2a4e94fe-2a89-4673-b541-5c03b9f4acdd.png">
