# Attached & Detached
- docker logs - Utilizamos para ver os logs que estão acontecendo dentro de um Conteiner especifico
- docker run - Cria o conteiner novo e o inicia a partir de uma imagem
- docker start - Reinicia um conteiner especifico que esta parado
- docker build . -q - Cria a imagem com o nome já
- docker run - Roda sempre attached ou seja, o terminal sempre fica aberto e não pode fazer nenhuma execucao no mesmo
- docker run -d - Roda em segundo plano o conteiner ficando assim com o terminal livre (detached), pode usar o docker logs para verificar a saída.
- docker attach <nome> - Se conecta ao terminal verificando a saida em tempo real de um conteiner q estava detached