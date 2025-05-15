# Avaliação de algorítmos para determinação das rotas mais curtas em grafos urbanos

## Autores: 
### • Lucas Garcia Costa   

### • Maurício Matheus Araújo Silva Galvão  



Link para o vídeo explicativo: https://drive.google.com/drive/u/0/folders/1ghKkB1SeIr4uw_xilaxyV2jw2oH9XzuS

Nesta atividade foi utilizado como cenário o roteamento para serviços de emergência, onde foi avaliado o tempo de resposta de ambulâncias saindo do Hospital Walfredo Gurgel para diferentes bairros, os quais foram:

• Alecrim;  

• Felipe Camarão; 

• Pajuçara.  

Para determinar a rota mais curta para esses três bairros, foram utilizados e comparados o desempenho e eficiência de três algorítmos diferentes, sendo eles:  

• Dijkstra (O(n²));  

• Dijkstra com heap; 

• OSMNx.


O código foi feito em Python com a utilização das seguintes bibliotecas: `OSMNx`, `Codecarbon`, `Matplotlib.pyplot`, `Networkx` e `Folium`.    

Primeiramente criamos um grafo da cidade de Nata/RN, assim obtendo as coordenadas do ponto de origem, que foi o Hospital Walfredo Gurgel e posteriormente dos três bairros referenciados como destinos. Com isso pudemos aplicar os três algorítmos separadamente analisando as suas pegadas de carbono com ajuda da biblioteca `Codecarbon`, o que nos deu uma visão bem detalhada dos custos energéticos e ambientais da execução de cada um deles. Após esse processo, conseguimos visualizar quais foram as rotas mais curtas encontradas para cada caso:

## Sendo: OSMNx (vermelho), Dijkstra padrão (amarelo) Dijkstra com heap (ciano):  

### Rota mais curta do hospital para o Alecrim: 

![image](https://github.com/user-attachments/assets/0c0ff773-17e7-43c7-b3eb-ad1aeca42b1c)  


### Rota mais curta do hospital para Felipe Camarão:  

![image](https://github.com/user-attachments/assets/356ec6e8-9397-420e-a155-e2d3bd8b936c)  



### Rota mais curta do hospital para Pajuçara:  

![image](https://github.com/user-attachments/assets/639c195f-2c74-4520-ba1b-6c9090d70b6d)    


### Tabela de comparação entre os algorítmos:  

![image](https://github.com/user-attachments/assets/a0667a88-0b77-47ad-ae6d-90805dbb3e52)


Analisando os resultados podemos perceber que só temos dois caminhos e um deles é o Dijkstra. Isso se dá ao fato de que a rota escolhida pelo Dijkstra com e sem heap foram a mesma, porque ambos são o mesmo algorítmo, apenas diferem na estrutura usada para escolher o nó com o menor custo. O outro caminho é o OSMNx, nos mostrando em todas as imagens que a rota escolhida por ele é levemente mais extensa que a escolhida pelo Dijkstra. Uma explicação possível para isso é que o OSMNx usa `NetworkX`, que depende fortemente da estrutura e integridade dos dados do grafo, o que pode afetar a qualidade do caminho escolhido.  

Foi possível observar que como esperado a eficiência computacional do Dijkstra com heap é bem maior que a sem heap, isso se dá pelo motivo de que o com heap usa uma fila de prioridade (heap) para escolher rapidamente o próximo nó mais próximo, enquanto a versão sem heap não faz isso e itera todos os nós a cada passo, deixando extremamente mais pesado em grafos maiores.








