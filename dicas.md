# CI = Continuous Integration


# CI é o ato de preparar o código para o deploy, ou seja, antes do código ir para o deploy vocÊ precisar rodar os testes, ver se o código está a rodar, etc. Esse processo todo antes do deply chama-se CI e automatizar isso pode ser vantajoso porque validar isso na mão você pode esquecer de algum detalhe, com isso, você não esquece e caso o commit não passar no workflow criado, a pessoa não vai conseguir fazer o pull request.


# WorkFlow é a o processo de criar essas etapas de verificação para garantir que o código só passe se estiver tudo okay.

# Para criarmos o nosso workflow, na raiz do projeto devemos criar uma pasta chamada de .github e dentro dela criamos uma outra pasta chamada de workflows e dentro da pasta workflows criamos um arquivo chamado de ci.yaml e dentro desse arquivo colocamos as coisas que queremos.


# Depois de criado o arquivo ci.yaml com tudo que queremos e já termos comitado tudo no github, podemos clicar no repositório do git e clicar em actions e aí conseguiremos ver os nossos workflows, inclusive o workflow que criamos, é só clicarmos no workflow que criamos, vamos clicando nele para vermos o que ele executou.

# Depois de clicado no nome do workflow, vamos ver o commit que fizemos, é nesse commit onde roda o nosso workflow. Tanto é que você pode ver que o workflow passou no commit anterior, mas não passou no novo commit e inclusive você consegue ver qual step falhou no workflow.

# Quando abres o repositório, você consegue ver se o workflow passou ou não, se não passou fica um x ao lado do nome do teu commit. Caso alguma coisa não passar, você não consegue fazer o push.

# Para efetivamente barrar um merge ou um pull request (fazendo com que não passe), podemos primeiro deixar a nossa branch develop como padrão no repositório, para isso basta estar no repositório, clicar em settings e daí mudar o default branch. Depois de mudado a develop para a branch principal, vamos agora adicionar regras nessa branch develop assim: Clicamos em settings->Branch->Add classic branch protection rule, em branch name pattern coloca develop (Nome da branch a ser protegida), clicar em require status check to pass before merging, digitar o nome do teu job que deve rodar nessa branch e selecionar o job, selecionar também o Require branches to be up to date before merging, clicar em Lock branch para impedir usuários de fazerem push nessa branch, clicar em Do not allow bypassing the above settings para aplicar as regras aos administradores também, clicar em criar.

# Criar uma outra rule para o master, nesse caso branch pattern name coloca master e seleciona também o Require status checks to pass before merging e coloca o nome do teu job assim como feito na develop, também seleciona esse: Require branches to be up to date before merging, seleciona também o Lock branch e o Do not allow bypassing the above settings, ou seja, criamos basicamente a mesma coisa.