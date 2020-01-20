# Scripts uteis

## Removendo arquivos do trackeamento do GIT

Para parar de trackear um arquivo especifico sem adicioná-lo ao gitignore:
``` shell
git update-index --assume-unchanged <arquivo>
```

Para trackear o arquivo de novo:
``` shell
git update-index --no-assume-unchanged <arquivo>
```

Para fazer o mesmo com pasta, basta usar a flag '-r'(recursive):
``` shell
git update-index -r --assume-unchanged <arquivo>
git update-index -r --no-assume-unchanged <arquivo>
```

----

## Resetando banco de dados de teste do Rails

Primeiramente, para criar o banco de dados de testes:
``` shell
bundle exec rake db:test:prepare
```

Para resetar o banco de testes:
``` shell
bundle exec rake db:reset RAILS_ENV=test
```

----

## Deletando branches do GIT:

Para deletar uma branch local:
``` shell
git branch -D <nome do branch>
```

Para deletar uma branch remota:
``` shell
git push -d <nome do remote> <nome do branch>
```

----
