# Run e Delecao
- Quando subimos um conteiner e queremos que o mesmo seja apagado logo em seguida para que não fique sujeira dele utilizamos o seguinte comando:
  - docker run -p <porta:porta> --rm <imagem>
- Caso precise ser um conteiner Dettached utilizamos:
  - docker run -p <porta:porta> -d --rm <imagem>
- Caso seja um interativo mudamos para:
  - docker run -p <porta:porta> -it --rm <imagem>