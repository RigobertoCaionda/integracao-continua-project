# CI = Continuous Integration


# CI é o ato de preparar o código para o deploy, ou seja, antes do código ir para o deploy vocÊ precisar rodar os testes, ver se o código está a rodar, etc. Esse processo todo antes do deply chama-se CI e automatizar isso pode ser vantajoso porque validar isso na mão você pode esquecer de algum detalhe, com isso, você não esquece e caso o commit não passar no workflow criado, a pessoa não vai conseguir fazer o pull request.


# WorkFlow é a o processo de criar essas etapas de verificação para garantir que o código só passe se estiver tudo okay.

# Para criarmos o nosso workflow, na raiz do projeto devemos criar uma pasta chamada de .github e dentro dela criamos uma outra pasta chamada de workflows e dentro da pasta workflows criamos um arquivo chamado de ci.yaml e dentro desse arquivo colocamos as coisas que queremos.