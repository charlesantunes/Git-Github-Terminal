**Introdução ao Git e ao GitHub**

O Git segue os comandos simiar ao linux.

 

​                                   

 

 

   **Terminal do Windows**

cd = processeguir em uma pasta

dir = listar todas as pastas

mkdir = criar pasta

del = deleta os arquivos de dentro da pasta

rmdir " " /S /Q = deleta a pasta com tudo

cd .. = retroceder em uma pasta

cls = limpar cmd

cd / = volta para o inicio do diretore, no caso C:

tab = auto completa a palavra

echo hello > hello.txt = echo prepara a criação o arquivo hello que com o > confirma o arquivo e a extensão dele

 

**Terminal do Linux**

cd = prosseguir em uma pasta

cd / = volta para o início do diretore, no caso C:

cd .. = retroceder em uma pasta

ls ou control+L = listar todas as pastas

mkdir = criar pasta

rm -rf = deletar pasta

clear = limpar cmd

sudo su = permissão administrador

tab = auto completa a palavra

pwd = exibe o caminho atual que está 

ls -a = mostra arquivos ocultos

sha1 é a forma como o git incriptografa os dados.

​          

 

 

 

 

 

   Objetos internos responsavel pelo versionamento do git

​                                 

 

 

 

 

   

 

 

 

 

 

 

 

 



​                  

 

 

Classificado como sistemas distribuídos por que são arquivos compartilhados com vários usuários, pois se ocorrer de acontecer algo com o servidor, esses arquivos estarão divididos em copias com todos os usuários atual usando esse mesmo arquivo com diferentes criptografia(sha), caso a rede venha a cair em um lugar, a copia do arquivo pode estar com outro online. Por isso o Sistema distribuído e seguro.

 

 

**CHAVE SSH:**

Gerando a chave SSH no sialay (Git bash), segue os comandos:

\- ssh-keygen -t ed25519 -C charleswcantunes@gmail.com 

Enter , depois enter de novo, digita uma senha (eu usei a senha do meu facebook :/)

\- cd /c/Users/charl/.ssh/

\- cat id_ed25519.pub

Copiar todo o conteúdo da chave que aparecer, até mesmo o meu email.

ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHaUak5p/arLNxHDeKOTTR7xi4Rzdnl0f8oI+Z2R/Kt6 [charleswcantunes@gmail.com](mailto:charleswcantunes@gmail.com)

colar no site do Github, no local: perfil, settings, SSH and GPG key, New SSH key.

Adicionar um titulo para especificar o computador e depois em key, colar a chave SSH, confirma em Add SSH key.

Próximo passo é voltar para o Gitbash e digitar um comandos para inicializar o ssh-agent, esse tem o papel de gerenciar as chaves publicas e privadas.

\- eval $(ssh-agent -s)

Será informado um numero do Agent aleatório, vou exemplificar com um número “Agent pid 1382”.

Agora deve digitar um comando e adicionar a chave privado, a chave que não tem o .pub, ou seja, “id_ed25519”, segue o código:

-ssh-add id_ed25519

Vai solicitar a senha que foi feita na criação da chave, bem no início do processo, ou seja, a senha que coloquei sendo a mesma do facebook :/.

 

Testando o SSD clonando um repositório, com o comando

-git clone “colar o ssd do repositório a ser clonado”

  

 

 

 

Gerar um token de acesso no github e toda vez que for fazer um commit, coloca o seu usuário e a senha sera o token. Segue o caminho para configurar o Token: 

perfil, settings, developer settings, Personal access tokens. Na parte superior direita, clica em Generate new token. Preencher o nome do token e marcar ‘**repo’**, depois só confirmar no final da página em “**Generate token”**.

Obs: colocar o código gerado pelo token quando for fazer por exemplo um Git clone ou um commit, no lugar da senha pessoal(facebook), colocar o código do token.

 

 

 

 

git init = inicia o repositório

git add = mover arquivos

git commit = enviar arquivos

 

Obs: Na primeira vez que for usar os comando no Git, precisar configurar um nome e senha qualquer, estilo nickname, como na imagem abaixo:

 

Usando arquivos do tipo Markdown (.md)

 

Exemplos de comandos básicos do Markdown no final da página.

​    

   Working Directory = é a área onde os arquivos estão sendo preparados para entrar no repositório do git

Staging Area = é a área onde os arquivos estão sendo manipulados pelo Unmodified, Modified e Staged, dentro do repositório do git e preparado para enviar para o github.

Local Repository

 

 

Untracked = Quando o git não tem ciência da existência desse arquivo

Unmodified = quando o git tem um arquivo dentro do repositório, mas não sofreu alteração

Modified = quando o git tem um arquivo dentro do repositório e realiza alguma alteração nele

Staged = Quando o arquivo está preparado para fazer um commit e retornar o ciclo para o Untracked

Tracked = é o ciclo realizado entre o Unmodified, Modified e Staged

 

**Realizando o primeiro commit, segue imagem:**

 

 

 

Nos comando abaixo, foram criada uma pasta chamada receitas e depois o arquivo lasanha.md será movido para a pasta receitas.

\- git status = verifica o status dos arquivos se foram modificados.

\- mv “nome do arquivo e extensão” ./”pasta local do arquivo”/ = mover um arquivo para outra pasta

 

  

 

 

 

 

 

Nos comandos abaixo, será feito um retorno para a pasta livro-receita e listar os arquivos, verificando a nova pasta receitas, em seguida verificar os status dos arquivos e observando que o git identifica como deletado o arquivo lasanha.md que na verdade ele foi movido para outra pasta. Isso ocorro porque a pasta criada receitas não foi realizado o commit e dessa forma o git ainda não reconhece o arquivo.

  

 

Na imagem abaixo, o arquivo lasanha.md e a pasta receita, seram preparados(stage) para fazer commit quando quiser. Depois feito um git status para verificar que os não foram feito commit e recomenda o comando do commit, logo em seguida ele exibe os arquivos para fazer o commit.

Obs: sera informado que pode ser desfeita a preparação dos arquivos e voltarem para estado de unstage.

  

 

 

 

 

 

 

 

No comando abaixo, será feito o commit e uma mensagem para identificar o motivo do commit, em seguida um git status para identificar que não há mais arquivos ou pastas para fazer commit.

  

 

Segue exemplos de criação de arquivos e manipulação

  



 

# **Guia básico de Markdown**

**Markdown Syntax** é uma sintaxe usada para padronizar e facilitar formatação de texto na web, utilizada em aplicativos como [Slack](https://slack.com/) e [GitHub](https://github.com/). Textos estilizados com **Markdown** são, na maioria dos casos, apenas texto com caracteres não-alfabéticos, como `#`, `\*` e `![]()`, usados para a configuração de títulos, listas, itálico, negrito e inserção de imagens.

O Markdown funciona como um conversor de texto para HTML: os caracteres não-alfabéticos são traduzidos como `<b>`, `<i>` e `<a href>`, etc. Já os textos sem formatação entram como parágrafo simples `<p>`.

## **Lista de comandos em Markdown**

Veja abaixo uma lista dos comandos em markdown e alguns exemplos de seu uso:

### **Titulação**

```
# Título <h1>
## Título <h2>
### Título <h3>
#### Título <h4>
##### Título <h5>
###### Título <h6>
```

### **Exemplos de titulação**

# **Título 1**

## **Título 2**

### **Título 3**

#### **Título 4**

##### Título 5

###### Título 6

### **Ênfase**

Para adicionar ênfase ao conteúdo que será escrito, usa-se o asterisco `*` ou traço-baixo (*underline*) `_`:

- **Negrito**: adicione dois asteriscos ****texto**** ou dois     traços-baixos __**texto**__     no início e no fim do conteúdo.
- **Itálico**: adicione apenas um asterisco **texto** ou um traço-baixo _*texto*_ no início e no fim do     conteúdo.

Este é um exemplo de um texto que possui uma ênfase em ****negrito\****, e outro em _*itálico*_.

### **Links**

Existem duas formas de inserir link em Markdown, através de um **link direto** ou usando um **texto-âncora**:

·     **Texto-âncora**: utilize os caracteres `[]()`, adicionando entre chaves o texto que você quer que apareça, e entre os parênteses, o endereço de destino, no formato `[exemplo](https://exemplo.com/)`.

·     **Link direto**: envolva o endereço da web em chaves `<>`. O endereço ficará visível e será clicável pelo usuário. O endereço em forma de link direto tem o formato `<https://exemplo.com/>`.

Este é um [link em formato de texto](https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown), e este é um link direto https://pipz.com/.

### **Listas de itens**

Para listas não ordenadas, utilize um asterisco `*` na frente to item da lista:

```
* Item 1
* Item 2
* Item 3
```

Para listas ordenadas, utilize o número do item seguido de ponto `.` :

```
1. Item 1
2. Item 2
3. Item 3
```

As listas acima serão exibidas dessa maneira, respectivamente:

- Item 1
- Item 2
- Item 3

1. Item 1
2. Item 2
3. Item 3

### **Imagens**

O código para inserir uma imagem no conteúdo é semelhante ao código de inserir links-âncora, adicionando um ponto de exclamação `!` no início do código, como no exemplo abaixo:

```
![Alt ou título da imagem](URL da imagem)
```

Esta é uma linha com uma imagem personalizada   .

Imagens grandes podem estar em linhas individuais, para serem exibidas em maior tamanho.

### **Citação (Quote)**

Para transformar um texto em uma citação ou comentário, semelhante ao código HTML `<blockquote>`, utilize o sinal `>` no início da linha que será formatada:

```
>Este é um *blockquote*. O sinal usado abre e fecha este código no HTML. 
>Para adicionar mais uma linha à citação, basta teclar Enter para um novo
>código sinal. Isso gerará um novo parágrafo dentro do *blockquote*.
>Códigos de **negrito**, _itálico_ e <https://links.com> funcionam aqui.
```

Como aparece no HTML:

Este é um *blockquote*. O sinal usado abre e fecha este código no HTML. Para adicionar mais uma linha à citação, basta teclar Enter para um novo código sinal. Isso gerará um novo parágrafo dentro do *blockquote*. Códigos de **negrito**, *itálico* e [https://links.com](https://links.com/) funcionam aqui.

### **Código (Code Highlight)**

Há dois modos de adicionar trechos de código ao Markdown:

- **Código em linha** (*inline*):     adicione um acento grave `ˋ` no início e no final do código.
- **Múltiplas linhas de código**: envolva as linhas de código com três acentos     graves `ˋˋˋ` ou três tils `~~~`.

```
 Esta é uma linha que contém um ˋcódigoˋ.
 
ˋˋˋ
Esta é uma linha de código
 ˋˋˋ
```

Para especificar que tipo de linguagem está sendo apresentada no bloco de códigos adicionando o nome da linguagem de programação após o `ˋˋˋ` ou `~~~`, por exemplo `~~~javascript` ou `~~~ruby`. Veja nos exemplos abaixo:

```
~~~javascript
Esta é uma linha de código em Javascript.
~~~
 
~~~php
Esta é uma linha de código em PHP.
~~~
 
~~~html
Esta é uma linha de código em HTML.
~~~
```

JAVASCRIPT

PHP

HTML

```
Esta é uma linha de código em Javascript.
```

Aqui está a lista de [linguagens suportadas](http://pygments.org/languages/) pelo Pygments, usada em nosso **Learning Center**.

### **Tabela**

Escolha os títulos das colunas e use `|` para delimitar as colunas. Depois, utilize hífen `-` na segunda linha para indicar que acima estão os títulos das colunas, usando novamente o `|` para delimitar colunas. Veja um exemplo abaixo:

```
Exemplo   | Valor do exemplo
--------- | ------
Exemplo 1 | R$ 10
Exemplo 2 | R$ 8
Exemplo 3 | R$ 7
Exemplo 4 | R$ 8
```

Como aparece no **Learning Center**:

| Exemplo   | Valor do exemplo |
| --------- | ---------------- |
| Exemplo 1 | R$ 10            |
| Exemplo 2 | R$ 8             |
| Exemplo 3 | R$ 7             |
| Exemplo 4 | R$ 8             |

Para especificar o tipo de alinhamento que deseja ter nas tabelas, utilize `:` ao lado do campo horizontal de hífens `---`, na segunda linha da sua tabela. Veja abaixo:

- **Alinhado a esquerda**: usar `:` no lado esquerdo (alinhamento padrão);
- **Alinhado a direita**: usar `:` no lado direito;
- **Centralizado**: usar `:` dos dois lados.

Veja no exemplo:

```
Alinhado a esquerda | Centralizado | Alinhado a direita
:--------- | :------: | -------:
Valor | Valor | Valor
```

| Alinhado   a esquerda | Centralizado | Alinhado a direita |
| --------------------- | ------------ | ------------------ |
| Valor                 | Valor        | Valor              |

 

 
