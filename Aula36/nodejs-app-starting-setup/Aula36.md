# Nome em Conteiners e Image

## Nomear Conteiners
- Para nomearmos um conteiner utilizamos o comando --name <nome>, ficando assim para executar com um nome:
  - docker run -p <porta:porta> -d --name <nome> <image> : Nesse exemplo preferi colocar porta e colocar dettached

## Nomear Image
- Para nomearmos uma image fazemos um processo um pouco diferente, na sua criacao iremos rodar o seguinte:
  - docker build -t <nome:tag> .
  - Na image normalmente colocamos o seu nome ao lado esquerdo sendo por exemplo NewIO e em Tag a versão tipo 1.01.03