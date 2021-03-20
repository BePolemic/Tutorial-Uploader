
![](images/image8.jpg)


# GUIA DO UPLOADER EFICIENTE

Um oferecimento de [t.me/PolemicKnowledge](t.me/PolemicKnowledge)

Versão v101

## Sumário

1. Preparando o Ambiente
    1. ffmpeg
    1. anaconda
1. Customização do Zimatise
1. Como Utilizar os Utilitários e Upar Vídeos de Maneira Eficiente
    1. ETAPA 1 - Preparando o ambiente
    1. ETAPA 2 - Gerar relatório de arquivos de vídeos
    1. ETAPA 3 - Como utilizar os utilitários-O segredo do Processo Automático e Upload eficiente
    1. ETAPA 4 - Agrupamento dos vídeos
    1. ETAPA 5 - Descrições dos vídeos e do Projeto
    2. ETAPA 6 - O Upload
2. Conclusão


## Importante

Nenhum dos softwares utilizados nesse tutorial possui relação direta como o objetivo deste tutorial.

O uso dos softwares em conjunto para qualquer objetivo, é por uma decisão individual de responsabilidade de cada usuário.

## ETAPA 1 - Preparando o ambiente

Para começar, é necessário instalar alguns programas que são dependências para que os utilitários funcionem, são eles o ffmpeg e o anaconda.

### 1.1 ffmpeg

O ffmpeg é uma "caixa de ferramenta" que pode ser utilizada via linha de comando por qualquer linguagem de programação para fazer dezenas de operações com arquivos áudio, vídeo e legendas, incluindo transformar vídeos (codecs, resolução, bitrate) e extrair quaisquer informações (metadados) sobre esses arquivos.

#### Para obter o ffmpeg:
- Baixe a partir deste [link direto]((https://www.gyan.dev/ffmpeg/builds/ffmpeg-git-full.7z)), que contém a versão completa e atualizada do programa. Ou siga os passos abaixo.
- Acesse [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html).
- No campo “get packages & executable files”, clique no botão que representa o Windows.
- Logo em seguida, escolha a opção `Windows builds from gyan.dev`
- Em seguida clique no link `https://www.gyan.dev/ffmpeg/builds/ffmpeg-git-full.7z`

#### Configurando o ffmpeg:
- Felizmente o ffmpeg não se instala, sendo uma aplicação portátil (portable). É necessário apenas o configurar para que seja possível o utilizar por terminal a partir de qualquer local ou pasta do PC.
- Escolha um diretório e crie uma pasta com o nome `ffmpeg`.
- O arquivo baixado deve ser extraído nesta pasta vazia que foi criada.
- Para o ffmpeg ser acessável via terminal a partir de qualquer local do seu sistema, busque o termo `variáveis de ambiente` na ferramenta de busca do windows e acesse  a aplicação `editar as variáveis de ambiente do sistema`.
- Na aplicação que será aberta, acesse a guia `Avançado` e clique no botão `Variáveis de Ambiente`.

![](images/image20.png)

- No form "Variáveis de Ambiente", clique no nome `Path` na coluna `Variável`. Em seguida clique no botão `Editar`.

![](images/image19.png)

- No form "Editar a variável de ambiente", clique no botão "Novo" e adicione o caminho da pasta `bin` que existe dentro da pasta criada para o ffmpeg.
- Caso se tenha criado a pasta na "unidade C", a pasta `bin` estará no caminho: `C:\ffmpeg\bin`

![](images/image22.png)

- Para evitar erros, logo após adicionar o novo caminho, selecione o novo caminho adicionado, em seguida clique no botão `Mover para Cima`.
- Esta ação dará ao path criado, maior prioridade em relação aos demais paths da lista.

![](images/image21.png)

- Parabéns. O ffmpeg foi configurado como variável de sistema!
- Para verificar se está tudo funcionando bem, basta abrir o cmd do Windows: (`[ctrl]+[r], cmd, [enter]`)
- Em seguida digite `ffmpeg` no terminal aberto e tecle `[Enter]`. O resultado deve ser similar a imagem abaixo.

![](images/image25.png)


### 1.2 anaconda
Anaconda é uma 'distribuição python' que funciona como pacote que instala a linguagem de programação Python, diversas libs de ciência de dados e outras coisas úteis.
Diferentemente de enfrentar o trabalho de instalar cada pedaço separado, a instação do Anaconda automatiza o serviço e poupa bastante tempo.

#### Para obter o anaconda:
* Acesse [https://www.anaconda.com/products/individual](https://www.anaconda.com/products/individual)
* Clique em download
* Baixe a versão apropriada para a sua arquitetura (64 ou 32 bits)
* Execute o .exe baixado.
* No form 'Advanced Options', marque `Add anaconda3 to my PATH environment variable`. Esta função automatiza a inclusão do Python no Path do windows, dispensando a repetição do trabalho executado no tópico anterior, com o ffmpeg.
* Clique em `Install`
* A instalação pode demorar alguns minutos, mas isso é normal.

![](images/image23.png)

## 2 Preparação os utilitários

Baixe os utilitários nos seguintes links:

1. Mass Video Join: [https://github.com/apenasrr/mass_videojoin](https://github.com/apenasrr/mass_videojoin)
2. Time Stamp Link Maker: [https://github.com/apenasrr/timestamp_link_maker](https://github.com/apenasrr/timestamp_link_maker)
3. Zipind: [https://github.com/apenasrr/zipind](https://www.google.com/url?q=https://github.com/apenasrr/zipind&sa=D&ust=1608417945410000&usg=AOvVaw22EBq1e5Hj2e1qtxo5p8lj)
4.  Telegram_filesender: [https://github.com/apenasrr/Telegram_filesender](https://github.com/apenasrr/Telegram_filesender)
5.  Zimatise: [https://github.com/apenasrr/zimatise](https://github.com/apenasrr/zimatise)

### Como baixar
- Clique no botão “Code” e, em seguida,
- Clique em “Download ZIP”.
- Repita o procedimento na página de cada utilitário

![](images/image27.png)

- Extraia todos os utilitários numa mesma pasta.
- Garanta de que as extensões de arquivo estão sendo exibidas, indo no menu “Exibir” e então marcando o checkbox “Extensões de nomes de arquivos”.

![](images/image26.png)

`ATENÇÃO: OS PASSOS A SEGUIR DEVEM SER REPETIDOS EM TODOS OS UTILITÁRIOS.`

### Atualizações de dependências
O python é uma linguagem de programação, onde durante a atividade de programação, vários 'atalhos' são pegos através do uso de scripts que foram criados por outras pessoas. Eses scripts são chamados de 'Libs' (bibliotecas).

Cada utilitário composto pelo Zimatise possui diversas libs requeridas, que precisamos baixar e atualizar.

Para facilitar o processo, tudo foi resumido à execução de 1 arquivo.
- Para cada pasta de utilitário, abra sua pasta e execute o arquivo `update_libs.bat`.

![](images/image30.png)

- Renomeie as pastas de cada utilitário, tirando o `“-master”` do nome cada uma. O resultado final deve ser esse:

![](images/image28.png)


```
CURIOSIDADE

O passo acima só foi necessário porque os utilitários foram baixados através do botão 'code' no site do github.
Se tivessem sido baixados por linha comando (git clone), as pastas apareceriam da forma desejada.
Para saber mais: https://docs.github.com/pt/github/creating-cloning-and-archiving-repositories/cloning-a-repository
```
### Customização do Zimatise
#### Aplicação de assinatura no sumário do canal
- Na pasta do utilitário timestamp_link_maker, os textos dos arquivos `“summary_bot.txt”` e `“summary_top.txt”` precisam ser alterados.

![](images/image29.png)

* No arquivo “summary_bot”, troque o texto que está lá por esse:

```
Bons estudos!

Não se esqueça de checar os nossos outros cursos:

@PolemicKnowledge
```
O resultado será como na imagem:

![](images/image31.png)

- No arquivo “summary_top”, troque o texto que está no arquivo por esse:

```
⚠ Atenção ⚠

Clique aqui para ver o Menu de navegação.
Utilize as # para navegar rapidamente entre os blocos de vídeos.


Materiais em #Materiais
```

- O resultado será como na imagem:

![](images/image32.png)

#### Seleção dos arquivos à serem compactados
Vídeos serão disponibilizados via streamming, mas demais arquivos serão compactados. Para gerar este efeito, é necessário informar ao Zimatise quais tipos de arquivos não deverão ser compactados.
- Acesse a pasta do utilitário `Zipind`
- Acesse a pasta `config`
- Abra o arquivo `ignore_extensions.txt`
- Na última linha do arquivo, adicione as extensões de vídeos que não deverão ser compactadas, tal como exemplo:
- `mp4,avi,webm,ts,vob,mov,mkv,wmv`

![](images/image32-1.jpg)

#### Definição de limites de tamanho e duração
O processo de agrupamento dos vídeos é guiado por alguns limites para que o projeto não seja consolidado num único vídeo de dezenas de horas e gigabytes. A definição de limites sugerida está em sintonia com uma boa experiência em se assistir vídeos por stream.
- Acesse a pasta do utilutário `mass_videojoin`
- Em seguida acesse a pasta `config` e abra o arquivo `config.txt`
- Na flag `size_per_file_mb`, defina como `'999'`
- Na flag `duration_limit`, defina como `'02:00:00.00'`
> Atenção: As aspas simples no início e final dos valores são necessárias.abra a pasta config A definição resume em agrupar os vídeos em grandes blocos com duração máxima de horas e/ou de tamanho máximo definido em megabytes.\

![](images/image32-2.jpg)

#### Ativação do Efeito de Transição nos vídeos
Esta função é opcional. Para desestimular a prática de cópia dos vídeos sem que haja citação a equipe que os processou, pequenos vídeos podem ser usados no início e final do bloco de vídeo, com também usado na forma de efeitos de transição, entre os diversos vídeos que foram agrupados.\
O Zimatise é inteligente para gerar novos vídeos de transição com resoluções diferentes na medida em que haja necessidade de os agrupar com vídeos cuja resolução seja diferente das encontradas até então.\
Para evitar grandes distorções no processo de adaptação de resolução, é recomendado que se crie 2 vídeos de transição com **alta definição**, mas possuindo uma relação de largura/altura (aspect ratio) de `16:9` e outra com `4:3`.
- Acesse a pasta do utilutário `mass_videojoin`
- Em seguida acesse a pasta `transition`. Crie caso ela não exista.
- Cole os vídeos de transição nessa pasta.
- Em seguida acesse o arquivo de configurações (`mass_videojoin\config\config.txt`) e defina a flag `activate_transition` como `'true'`.
- Caso não tenha interesse em usar o Efeito de Transição, defina a flag como `'false'`.

![](images/image32-3.jpg)

#### Padronização de Descrição do projeto
A descrição do projeto pode ser automaticamente gerada, com algumas variáveis padronizadas, como tamanho do projeto em megabytes, duração em horas e até o 'link de convite', caso seja posteriormente utilizado API do Telegram no utilitário `Telegram_filesender` para subir os arquivos.
- Acesse o arquivo `zimatise\header_template.txt`
- O preencha com o texto abaixo:

```
{project_name}

{project_name}

Tamanho: {file_size}
Duração: {duration}

Convite: {chat_invite_link}


Be @polemic
```

## 3 Como utilizar os utilitários - O segredo do Processo Automático e Upload eficiente

Agora que todas as ferramentas estão prontas, é hora de usá-las.

- Acesse a pasta do Zimatise e execute o arquivo “zimatise.bat”
- Será aberta um `terminal` com um menu simples

### 3.1 ETAPA 1 - Compactação de arquivos

- No menu de opções, escolha a primeira opção digitando `1` e confirmando ao teclar `[Enter]`

![](images/image33.png)

> `AVISO: Lembre-se de teclar [Enter] após digitar uma resposta em todas as etapas.`

> ATENÇÃO\
> Mova a pasta do curso para a raiz do seu HD.\
> Caso seu HD seja a unidade `C` e a pasta do curso se chame `meu_curso`, após a pasta ser movida, o caminho para ela será: `C:\meu_curso`.\
> Este processo é importante pois o arquivo compactado preserva a hierarquia das pastas, gerando um resultado  incoveniente caso o curso esteja submerso entre diversas pastas no seu PC.\
> Após a finalização do projeto, naturalmente o curso pode ser movido de volta para a pasta que o usuário achar conveniente.
- Informe o caminho da pasta raiz do curso.
- Para copiar o caminho, acesse a pasta pelo `Windows Explorer` e tecle `[ctrl]+[L], [ctrl]+[c]`
- Caso ao tentar no colar no terminal, o atalho `[ctrl]+[v]` não funcione, clique com o botão direito do mouse dentro do terminal, que o caminho será colado.

-  Na pergunta `The maximum size of each file will be... Ok?`, é informado o tamanho máximo por arquivo compactado que o script está configurado. Recomenda-se configurar como `1024`.
-  Caso não esteja com o tamanho recomendado, digite `n`, confirme e em seguida digite o tamanho máximo recomendado.
-  Na próxima vez que esta opção for utilizada, o último tamanho usado será lembrado.
-  Caso o tamanho recomendado já esteja configurado, confirme sem digitar nada adicional, teclando `[Enter]`.
-  O processo de compactação será como na próxima imagem:

![](images/image34.png)

### 3.2 ETAPA 2 - Gerar relatório de arquivos de vídeos

O processo dos vídeos se resume em agrupar os vídeos em grandes blocos com duração máxima de horas e/ou de tamanho máximo definido em megabytes.\
Para gerar esse efeito, os vídeos a serem agrupados preciam ter o mesmo perfil, com o mesmo **encode de áudio, vídeo** e mesma **resolução**.\
O processo de transformação dos perfis para serem iguais entre si, se chama `homogeneização de perfis`.\
Para fazer esta análise e dá as instruções de transformação, siga os passos:
- Ative a segunda opção digitando `2`
- Informe o caminho da pasta do curso novamente e aguarde o processo de listagem

![](images/image35.png)

- Após a conclusão do processo, o utilitário informará os perfis encontrados nos vídeos da pasta e escolherá o perfil mais popular para servir de modelo de conversão, onde os demais vídeos serão marcados para serem transformados para se igualar ao perfil popular.

![](images/image36.png)


```
AVANÇADO
Diminuindo o tempo necessário de reencode.
- Também é possível não aceitar o plano sugerido de conversão. Onde você pode mudar o plano de conversão de modo a diminuir o tempo total de reencode sem afetar a qualidade final do projeto.
- A mudança do plano do plano de reencode é realizada no relatório `video_details.xlsx` que foi criado na pasta do projeto.
- Através da mudança ou exclusão dos valores de resolução de alguma das linhas da coluna "video_resolution_to_change".

Onde está a pasta do projeto?
- A pasta do projeto foi criada na pasta do Zimatise, com o nome: `output_{nome_da_pasta_do_curso}`.

De que forma devo alterar o plano?
- Recomenda-se que o objetivo de adaptação seja homogeneizar os perfis apenas dentro de cada bloco de vídeo.
- É recomendado que um bloco de vídeo não contenha vídeo de módulos diferentes. E não é necessário que diferentes blocos de vídeos tenham perfis homogêneos para possibilitar o processo de agrupamento.
- Desta forma, basta que os vídeos de um mesmo módulo sejam homogêneos, não sendo necessário que todo o curso possua vídeos de mesmo perfil de encode/resolução, tal como será sugerido no plano automático de reencode.
```

> ATENÇÃO\
> Execute a próxima etapa mesmo que a etapa anterior aponte que não seja necessário fazer alguma alteração, pois nesta etapa também são geradas transformações importantes no relatório, essenciais para o continuar o projeto com sucesso.

### 3.3 ETAPA 3 - Reencode - Transformação de perfis

O próximo passo é reencodar os vídeos, para os vídeos que serão agrupados, fiquem com o mesmo perfil de encode/resolução.\
Este processo pode demorar entre 10% à 50% da duração total dos vídeos à serem transformados de acordo com o plano de reencode.\
Assim, se o plano de reencode contiver 10 horas de vídeos, o processo de reencode pode demorar entre 1 à 5 horas, dependendo da potência de seu processador.

- Selecione a terceira opção digitando `3` e aguarde a conclusão do processo.

![](images/image37.png)

- Após o final do processo de reencode, o resultado será similar ao da imagem a seguir:

![](images/image38.png)

### 3.4 ETAPA 4 - Agrupamento dos vídeos

- O agrupamento obedecerá 5 critérios:
  - Vídeos com perfil (resolução/codec), processado na etapa de reencode
  - Limites de tamanho de arquivo e duração máxima dos vídeos
  - E ajustes manuais pelo usuário realizados no relatório
- Selecionar a quarta opção digitando `4`
- Caso o limite de tamanho (em mb) informado seja o desejado, tecle `[Enter]`, caso não seja, digite `no`, tecle `[Enter]` e informe o tamanho máximo desejado para os blocos de vídeos agrupados.

#### Ajustes manuais
- Aparecerá a mensagem `"File [...] was updated with group column to gast join"`
- Neste momento é possível fazer ajustes manuais no plano de agrupamento, através do relatório `video_details.xlsx` presente na pasta do projeto dentro da pasta do `Zimatise`.
- Na coluna `group_encode`, é possível indicar que certos grupos de vídeos devem ficar em blocos diferentes, alterando sua numeração sequencial que fora agrupada. Recomenda-se ajustar para que vídeos de módulos diferentes fiquem em agrupamentos (numerações) diferentes.
- Como exemplo, a imagem abaixo demonstra um projeto cujo plano de agrupamento foi ajustado manualmente para que vídeos de módulos diferentes fiquem em blocos diferentes. Sendo os primeiros 4 vídeos num bloco. Do 5º ao 8º em outro boco. 9º ao 11º em outro bloco. E por fim, o último vídeo sozinho num bloco. As numerações dos grupos são sempre sequenciais.

![](images/image9-1.jpg)

#### De volta ao processo
Uma vez que o plano de agrupamento está como desejado...
- Aparecerá a mensagem: `Start hashtag index count with what value?`
- Neste momento, informe qual o início da numeração sequencial que os vídeos agrupados devem ser automaticamente gerados. Se trata do sufixo dos vídeos agrupados (`"-001.mp4", "-002.mp4"`)
- Caso deseje manter o padrão de `1`, tecle `[Enter]`
- O processo de agrupamento dos vídeos iniciará, com uma velocidade por volta de 700 vezes mais rápida que a duração dos vídeos.

![](images/image9.png)

### 3.5 ETAPA 5 - Descrições dos vídeos e do Projeto

Este é a etapa da geração planilha `descriptions.xlsx`, que contém as  descrições dos blocos de vídeos, com marcação temporal (timestamps) que servirá de menu de navegação para cada bloco.
Também será gerado o arquivo `header_project.txt`, contendo a descrição do Canal conforme modelo configurado.
Ambos arquivos serão salvos na pasta do projeto, dentro da pasta do utilitário Zimatise.
- Selecionar a quinta opção digitando `5`
- Aparecerá a mensagem: `Start hashtag index count with what value?`
- Escolha qual a numeração inicial das hashtags das descrições dos blocos de vídeos. Caso deseje começar com o padrão 1, apenas tecle `[Enter]`. Caso deseje outra numeração inicial, informe em número inteiro e tecle `[Enter]`
- Após a criação do arquivo `descriptions.xlsx`, aparecerá a mensagem: `TimeStamp and descriptions files created`.
- Tecle `[Enter]` para o arquivo `header_project.txt` ser gerado.

![](images/image10.png)

#### 3.5.1 ETAPA 5 – Ajustes das Descrições

- Acesse o relatório `descriptions.xlsx`
- Caso exista avisos na coluna `"warning"` indicando `"max size reached"`, significa que para o vídeo daquela linha, a descrição gerada ultrapassa o limite do Telegram de 1000 caracteres (contendo os espaços).

![](images/image11.png)

- Essas descrições precisam ser alteradas para evitar uma colagem incompleta no Telegram.
- Para alterar, clique duas vezes na célula da descrição com problemas
- Ela se expandirá e será possível copiar o texto e colá-lo em um editor de texto (para fechar a célula, basta apertar `Esc`), ou ainda alterar no próprio Excel.
- Nesse tutorial será utilizado o software "Microsoft Word" para corrigir as descrições com problemas.

![](images/image12.png)

- Usando a contagem de caracteres do Word é possível ver quantos caracteres existem no documento, e, por dedução, quantos deverão ser cortados:

![](images/image13.png)

- Uma função muito útil do Word para correção de textos é a de substituição, segue um exemplo de uso:

![](images/image14.png)

- Depois que a descrição estiver com 1000 caracteres ou menos, copie e a cole na célula do Excel de onde ela foi originalmente copiada.
- Também é importante corrigir erros de digitação e caracteres incompreensíveis em todas as descrições, ao invés de só alterar aquelas que estejam com tamanho acima do limite.

#### 3.6 ETAPA 6 – O Upload
Existem dois métodos para fazer o upload para o Telegram.
O método automatizado via Macro de Teclado e o método através da API do telegram.
Neste tutorial, ambos métodos serão abordados, mas é recomendado utilizar o método através da API do telegram, para ser mais eficiente no processo e minimizar riscos de erros manuais.

##### Upload via Macro de Teclado
- Crie um novo canal privado no Telegram
- O canal deve OBRIGATORIAMENTE ter o nome oficial do curso, uma foto da logo do curso (caso o curso seja da udemy, utilize a thumb do vídeo de apresentação. Caso não encontre nada, consulte o resto da equipe).
- Na descrição, cole o conteúdo do arquivo  `header_project.txt` gerad na pasta do projeto. O ajuste caso necessário.

![](images/image15.png)

- Nas configurações do canal, copie seu link de convite

![](images/image16.png)

- O Telegram dará a opção de adicionar pessoas no seu canal. Pule essa etapa ou adicione alguém da equipe que foi definido para ser seu orientador. (Converse com a equipe e defina isso de antemão)

![](images/image17.png)

- Clique no botão de "três pontos" no canto superior direito e clique em `“Gerenciar Canal”`.

![](images/image18.png)

- A descrição deve conter o link do canal. Coloque-o acima da assinatura com o prefixo “Convite: ”, ou algo de cunho similar (caso pretenda mudar, avise a algum membro superior a você).

###### Coleta manual de Metadados
Os metadados do cursos (tamanho e duração), normalmente já devem ter sido automaticamente gerado no arquivo `header_project.txt`. Assim, essa etapa do tutorial pode ser pulada.
Caso por algum motivo o arquivo não tenha sido automaticamente gerado, siga os passos abaixo para obter os metadados.
- Acesse a pasta com os vídeos agrupados do curso
- Esta pasta estará dentro da pasta do projeto, que por sua vez estará dentro da pasta do Zimatise.
- Selecione todos os vídeos, clique com o botão direito em um deles e clique no botão `“propriedades”`.

![](images/image1.png)

- Na nova janela que será aberta, na aba `“geral”`, copie o tamanho dos vídeos e coloque na descrição do canal, acima do link de convite.

![](images/image2.png)

- Na aba `“detalhes”` da mesma janela, copie a duração total dos vídeos e também coloque na descrição do canal. Esta informação estará no bloco chamado `“Vídeo”`, na linha `“Comprimento”`.
- A duração deve estar no formato “XXh XXmin XXseg”

![](images/image3.png)

- Após essas alterações, a descrição do canal deve parecer similar ao exemplo abaixo:

![](images/image4.png)

###### De volta ao upload
O upload pelo método via Macro de Teclado consiste em o script imitar comandos de teclado para que cada arquivo de vídeo seja jogado de forma sequencial no app do Telegram juntamente com sua descrição.
Para executar esse método, é necessário um pequeno preparo para funcionar adequadamente:
- Abra a pasta dos vídeos agrupados do curso a ser upado e selecione o primeiro arquivo de vídeo.

![](images/image5.png)

- Siga os passos abaixo nesta exata ordem:
1. Deixe a janela da pasta dos vídeos aberta
2. Depois abra a janela do Telegram
3. Depois abra a janela do Zimatise
- Faça isso utilizando o comando `alt + tab`, para evitar que a seleção do vídeo se perca.
- Caso tenha errado a ordem de ativação das janelas, repita o processo até conseguir ativar as 3 janelas na exata ordem descrita.
   > Atenção: Caso não faça desta forma, há grande risco da automação gerar erros.
- Na janela do zimatise, tecle `6` e confirme com `[Enter]`
- Nas opções que aparecerão tecle [enter] confirmando que será utilizado o arquivo `descriptions.xlsx` existente
- Aparecerá a mensagem: `"How do you intend to send the files?"`
- Tecle `1`, informando que será utilizado o método via Macro de Teclado, pelo app do Telegram.

![](images/image6.jpg)

- Neste momento não toque no teclado e aguarde a colagem dos vídeos no app do Telegram terminarQuando o processo automático terminar,
- Após o término do upload, faça manualmente o upload dos materiais, que se trata do arquivo `.rar` na pasta onde estão os vídeos agrupados.
- Poste-o com a descrição `#Materiais`.
- O envio do arquivo `.rar` pode ser feito antes ou depois do envio dos vídeos.

![](images/image7.png)

- Caso prefira fazer o upload manualmente, não utilizando a função via Macro de Teclado, apenas arraste os vídeos para a janela do Telegram ou use o clipe de papel no canto inferior esqueto do quadro do canal, copie e cole as descrições no relatório “descriptions.xlsx” e repita o processo para todos os blocos, na ordem correta.

##### Upload via API do telegram

(em construção)

# Conclusão

1. O resultado final do tutorial pode ser checado aqui: [https://t.me/joinchat/AAAAAFN6ZXVSxD6JKsbCkg](https://t.me/joinchat/AAAAAFN6ZXVSxD6JKsbCkg)
