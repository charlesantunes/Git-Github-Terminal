## 📚 INTRODUÇÃO AO GIT E GITHUB

🌟 Esse repositório se da um desafio do Tech Lead da Dio Venilton Falvo Jr e tambem minha contribuição de aprendizado que estou iniciando ao longo dos meus estudos.

🔖 Me segue no Github: https://github.com/charlesantunes 👨🏻‍💻
🔖 Conecta lá no meu Linkedin: https://www.linkedin.com/in/charles-antunes-49b00057/ 💻

🔖Site para consultar as sintaxes básicas de Markdown: https://www.markdownguide.org/basic-syntax/**

Nesse resumo básico, os créditos são para as aulas de configuração do Desenvolvedor Web do instrutor Otávio Reis  da comunidade **Digital Innovation One**.

- O GitHub utiliza a linguagem Markdown para estilizar e formatar seus textos. 

- As linguagens principais para funcionalidades de GitHub são: C, C++, C#, Go, Java, JavaScript, PHP, Python, Ruby, Scala e TypeScript.

- O Git segue os comandos similar ao Sistema Operacional do Linux.

 

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) **Nesse guia pessoal, vou ensinar comandos iniciais de uso do Git e GitHub:**

Comandos básicos para:

- Mudar de pastas

- Listar as Pastas

- Criar pastas e arquivos

- Deletar pastas e arquivos

  

[📚 ](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**Segue alguns comandos básicos do Windows:**

 

·[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) **Terminal do Windows** 💻

`cd` = processeguir em uma pasta

`dir` = listar todas as pastas

`mkdir` = criar pasta

`del` = deleta os arquivos de dentro da pasta

`rmdir "nome da pasta s/ aspas" /S /Q` = deleta a pasta com tudo

`cd ..` = retroceder em uma pasta

`cls` = limpar cmd

`cd /` = volta para tela inicial do terminal, no meu caso C:

`tab` = auto completa a palavra

`echo hello > hello.txt` = echo prepara a criação o arquivo hello que com o > confirma o arquivo e a extensão dele

 

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**Terminal do Linux (usado no Git)** 💻

`cd` = prosseguir em uma pasta

`cd /` = volta para tela inicial do terminal, no meu caso C:

`cd ..` = retroceder em uma pasta

`ls` ou control + L = listar todas as pastas

`mkdir` = criar pasta

`rm -rf` = deletar pasta

`clear` = limpar cmd

`sudo su` = permissão administrador

`tab` = auto completa a palavra

`pwd` = exibe o caminho atual que está 

`ls -a` = mostra arquivos ocultos

 

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) **Conhecendo a criptografia sha-1 que é usado no git e github**

A sigla SHA significa Secure Hash Algorithm (Algoritmo de Hash seguro) é um conjunto de funções hash de dispersão criptográfica projetada pela Agência de Segurança Nacional dos Estados Unidos.

Essa encriptação gera um conto de caracteres identificador de 40 dígitos. O sha-1 é uma forma curta de representar o arquivo.

Sem dúvida alguma essa criptografia e uma das mais seguras do mundo, dessa forma foi usada pelo Git e GitHub.

 

[📚 ](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**Objetos internos responsáveis pelo versionamento do git**

- BLOBS

- TREES

- COMMITS

  

 [📚 ](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**CHAVES SSH E TOKENS** 💻

Inicialmente será configurada as duas chaves de segurança para versionamento dos arquivos entre o Git e o GitHub



[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) **CHAVE SSH:** 💻

Gerando a chave SSH no terminal do Git bash, segue os comandos:

`ssh-keygen -t ed25519 -C charleswcantunes@gmail.com`

Click no enter , depois enter de novo, digitar uma senha (eu usei uma senha que vou usar outras vezes “charufnOodwDbc”)

`cd /c/Users/charl/.ssh/`

`cat id_ed25519.pub`

Copiar todo o conteúdo da chave que aparecer, vai junto o email.

ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHaUak5p/arLNxHDeKOTTR7xi4Rzdnl0f8oI+Z2R/Kt6 [charleswcantunes@gmail.com](mailto:charleswcantunes@gmail.com)

colar no site do Github, no local: perfil, settings, SSH and GPG key, New SSH key.

Adicionar um título para especificar o computador e depois em key, colar a chave SSH, confirma em Add SSH key.

Próximo passo é voltar para o Gitbash e digitar um comandos para inicializar o ssh-agent, esse tem o papel de gerenciar as chaves publicas e privadas.

`eval $(ssh-agent -s)`

Será informado um numero do Agent aleatório, vou exemplificar com um número “Agent pid 1382”.

Agora deve digitar um comando e adicionar a chave privado, a chave que não tem o .pub, ou seja, “id_ed25519”, segue o código:

`ssh-add id_ed25519`

Vai solicitar a senha que foi feita na criação da chave, bem no início do processo, ou seja, a senha que coloquei sendo a mesma do facebook :/.

 

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) **Testando o SSD clonando um repositório, com o comando:** 💻

`git clone` “colar o ssd do repositório a ser clonado”

[imagem do git clone](https://drive.google.com/file/d/1_gISxtZYlinv2oxA_JZQPruUNvaTqIyM/view?usp=sharing) 

charl@DESKTOP-M51ETFE MINGW64 ~
$ `cd c:`

charl@DESKTOP-M51ETFE MINGW64 /c
$ `mkdir workspace`

 charl@DESKTOP-M51ETFE MINGW64 /c
$ `cd workspace/`

charl@DESKTOP-M51ETFE MINGW64 /c/workspace
$ `mkdir ssh-test`

charl@DESKTOP-M51ETFE MINGW64 /c/workspace
$ `git clone git@github.com:charlesantunes/projeto-web`

[segue a imagem dos comandos acima](https://drive.google.com/file/d/1BIKWED0-foNw66xTKbw6YdTmwMqaRTtg/view?usp=sharing)

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**Token de acesso: **

Gerar um token de acesso no GitHub e toda vez que for fazer um commit, coloca o seu usuário e a senha sera o token. Segue o caminho para configurar o Token: 

perfil, settings, developer settings, Personal access tokens. Na parte superior direita, clica em Generate new token. Preencher o nome do token e marcar ‘**repo’**, depois só confirmar no final da página em “**Generate token”**.

Obs: colocar o código gerado pelo token quando for fazer por exemplo um git clone ou um commit, no lugar da senha pessoal (charufnOodwDbc), colocar o código do token.

 

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**INICIANDO O GIT** 💻

Agora vamos iniciar usando o Git Bash, será usados os comandos abaixo: 

`git init` = inicia o repositório

`git add` = mover arquivos

`git commit` = enviar arquivos

 

Obs: Na primeira vez que for usar os comando no Git, precisar configurar um nome e senha qualquer, estilo nickname, como na imagem abaixo: 💻

`$ git config --global user.email "charleswcantunes@gmail.com"`

`$ git config --global user.name charlesantunes`

  

[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) **Ciclo de vida dos arquivos**

 O ciclo de vida dos arquivos no Git são divididos em 3 estágios:

:panda_face: [segue a imagem](https://drive.google.com/file/d/1d9DdpDWPRd8dtGXc7isXIg7ZF55MMdnB/view?usp=sharing)

 Unmodified = quando o Git tem um arquivo dentro do repositório, mas não sofreu alteração

Modified = quando o Git tem um arquivo dentro do repositório e realiza alguma alteração nele

Staged = Quando o arquivo está preparado para fazer um commit e retornar o ciclo para o Untracked

 

[📚 ](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**Existem status dos arquivos que são:**

Untracked = Quando o Git não tem ciência da existência desse arquivo

Tracked = é o ciclo realizado entre o Unmodified, Modified e Staged

 

[📚 ](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)**Realizando o primeiro commit**: 💻

o commit envia o arquivo para um repositório local.

 charl@DESKTOP-M51ETFE MINGW64 ~

`$ git add *`

`$ git commit -m "commit inicial"`

 

 [📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação) Nos comandos abaixo, foi criado uma pasta chamada receitas e depois o arquivo lasanha.md será movido para a pasta receitas. 💻

`git status = verifica o status dos arquivos se foram modificados.`

`mv “nome do arquivo e extensão” ./”pasta local do arquivo”/ = mover um arquivo para outra pasta`

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1BfcNDuPbBopYmCTydggwwEnqIXVI96ve/view?usp=sharing):arrow_heading_up:



[📚](https://github.com/arthurspk/guiadevbrasil#-sites-para-estudar-programação)  Nos comandos abaixo, será feito um retorno para a pasta livro-receita e listar os arquivos, verificando a nova pasta receitas, em seguida verificar os status dos arquivos e observando que o git identifica como deletado o arquivo lasanha.md que na verdade ele foi movido para outra pasta. Isso ocorro porque a pasta criada receitas não foi realizado o commit e dessa forma o git ainda não reconhece o arquivo.

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1DAgXHR8028TdTdsEO_y6nnO8riBPoN_6/view?usp=sharing):arrow_heading_up:

 

Na imagem abaixo, o arquivo lasanha.md e a pasta receita, seram preparados(stage) para fazer commit quando quiser. Depois feito um git status para verificar que os não foram feito commit e recomenda o comando do commit, logo em seguida ele exibe os arquivos para fazer o commit.

Obs: sera informado que pode ser desfeita a preparação dos arquivos e voltarem para estado de unstage.

  :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1joyjDMu01QnCnPb-dpySWQxPU5bG_D30/view?usp=sharing):arrow_heading_up:



No comando abaixo, será feito o commit e uma mensagem para identificar o motivo do commit, em seguida um git status para identificar que não há mais arquivos ou pastas para fazer commit.

  :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1aCiWl_ZzUbaaLYAps3MO2rfpFPka8q7l/view?usp=sharing):arrow_heading_up:

  

Segue exemplos de criação de arquivos e manipulação, sera adicionado manualmente pelo windows algumas informações no README.md

:panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1T-2nuN8t7fyS42ZTP76n-D5DVC-Utamr/view?usp=sharing):arrow_heading_up:



`git add` “nome do arquivo” = prepara um arquivo em específico para fazer o commit

`git add *`= prepara todos os arquivos da pasta para o commit

`git add.` = prepara todas os arquivos e modificações para commit.

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1yx7C61YNcOk4BX0MrC-cq5DLp1IggSrt/view?usp=sharing):arrow_heading_up:

 

📚 **GitHub**

Será Feita uma verificação da conta de usuário para que seja feito o mesmo usuário do git e o github, dessa forma evitar problemas futuros

`git config --list` = verificar qual o usuário registrado no git

:panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1uwdKfbaArdITQCLyknEzqGUrRjrbGi3d/view?usp=sharing):arrow_heading_up:

Se precisar alterar o e-mail e usuário da conta do git, segue abaixo os códigos:

`git config –global –unset user.email`

`git config –global –unset user.name`



Verifique que o user.email e user.name, sumiram, agora os próximos códigos serão os mesmo do inicio da aula de cadastro.vou repetir o código:

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1eUcEBUQ6pbSXK-fK88_oCJJBqW8qlnwu/view?usp=sharing):arrow_heading_up:



`git config –global user.email “charleswcantunes@gmail.com”`

`git config –global user.name “charlesantunes”`



📚 Criando um repositório:

Tela com o local para criar repositório

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1DfMjcF89bfROi_--L5WAw3d5Oyofxybt/view?usp=sharing):arrow_heading_up:

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1Q2pz3WRfg5bo67Dp4C3MKFOjWbi-nKM5/view?usp=sharing):arrow_heading_up:



Criei o nome do meu repositorio e não marquei o README, porque o mesmo já foi criado no git.

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1AGJHO15yGVQoBzja0W5S8Oeue7Hu2gD-/view?usp=sharing):arrow_heading_up:



Copiando o endereço do repositório.

:panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1VaU_UTLPDfkf1C8L0o9omNUeygE6B_x1/view?usp=sharing):arrow_heading_up:



Comandos a seguir serve para apontar o endereço do GitHub ao Git e deixar preparado para fazer o push

`git remote add origin https://github.com/charlesantunes/Git-GitHub-via-comando.git`

`git remote -v` = verifica o que esta apontado na pasta

 :panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1hXDoVH8BUzz7JVdRVmSdEtY-KAIrURkH/view?usp=sharing):arrow_heading_up:

 

Obs: Algumas alterações que fiz antes de iniciar o git push.

Na tela abaixo eu excluir uma pasta depois informei ao git essa alteração, usei antes dessa tela um git add *.

:panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/18lD8sxKdCtck2j4wjEmAQEBISE_JSjxF/view?usp=sharing):arrow_heading_up:



📚 Agora sim! Git preparado para fazer push (enviar do git para github ou contrário)

`git push origin master`

:panda_face: [imagem dos códigos de cima](https://drive.google.com/file/d/1yy1T6n8N8HIfGQTA4GLjq9PzkHXDU5zo/view?usp=sharing):arrow_heading_up:
