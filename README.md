# Documentos da CPI da Pandemia

A [CPI da Pandemia](https://legis.senado.leg.br/comissoes/comissao?codcol=2441) recebeu milhares de documentos **públicos**, [todos disponibilizados no site do Senado Federal](https://legis.senado.leg.br/comissoes/docsRecCPI?codcol=2441).

Mas como clicar um por um leva tempo, automatizamos o **download** e **descompactação** de todos esses arquivos, facilitando assim não só o acesso, mas também buscas nos arquivos com ferramentas como Evernote, Spotlight, etc.

## Aviso importante

Algumas links para baixar os documentos públicos não funcionam pois o servidor do Senado parece instável. Mesmo com estratégias de repetir a tentativa em caso de erro, pode ser que nem todos os arquivos listados estejam, de fato, disponível.

Links que não puderem ser baixados são listados no arquivo `erros.txt`.

## Só quero baixar os arquivos

O resultado está disponibilizado nesse [diretório no Dropbox](https://www.dropbox.com/sh/ccl5u1bu8dkw2io/AADHkNe0pCiSv5MWiomKhA4ga?dl=0), e você pode baixar tudo com um clique.

Vou tentar manter esse diretório atualizado executando esse programa cerca de 3x semana.

## Sou _hacker_ e quero mais

Você também pode baixar tudo direto do Senado Federal, instalando esse pacote e digitando apenas um comando.

### Utilização com docker

Requer [Docker](https://docker.com):

```console
$ docker build -t docs-cpi-pandemia .
$ docker run -it -v $PWD/data:/docs-cpi-pandemia/data docs-cpi-pandemia
```

Os arquivos serão baixados em um diretório `data/` dentro da pasta onde você executou esse comando.

### Instalação sem docker

Requer [Go](https://golang.org/) 1.16.

```console
$ go run main.go
```

Existem opções que podem ser configuradas, as instruções e valores padrões podem ser vistos adicionando `--help` ao final do comando.
