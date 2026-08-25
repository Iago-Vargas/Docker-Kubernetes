# Excluir Conteiners e Images

## Remocao Conteiners
- Quando rodamos o docker ps -a e verificamos que existem conteiners que nem utilizamos mais conseguimos excluir eles com:
  - docker rm {nome_conteiner}
- Caso queiramos excluir uma grande quantidade vamos fazer dai
  - docker rm {nome_conteiner_1} {nome_conteiner_2} {nome_conteiner_3} {nome_conteiner_Y} ....

## Remocao Images
> Para remover Images é necessario anteriormente ter excluido o conteiner, por mais que ele esteja parado sem usar a image precisa ser deletado para conseguir excluir a Image
- Para exclusão de images iremos fazer a listagem primeiro
  - docker images - Para imagens que foram criadas sem o <none>
  - docker images -a - Listamos TODAS images por mais que não possuam <none>
- Comando da exclusao seriam:
  - docker rmi <id> - Para remover uma por uma
  - docker image prune - Remove TODAS image, precisa de confirmacao
