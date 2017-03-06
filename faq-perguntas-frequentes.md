# Perguntas Frequentes

## O que é o EAM?
 
O EAM (Emparelhamento ao modelo) é um software de pesquisa do comportamento de escolha concebido para funcionar em um contexto de  ensino individualizado e testes de aprendizagem e desempenho na pesquisa de controle de estímulos. Ele permite o planejamento de tentativas discretas com alternativas dispostas na tela de um monitor em posições programadas. Para programar uma sessão com uma sequência de tentativas o software lê um Arquivo de Sessão no qual os valores das variáveis são dispostos em sequência de acordo com desenhos experimentais ou planejamentos de ensino. O software registra e fornece um relatório de sessão com os valores por tentativa das variáveis fornecidas no Arquivo de Sessão e as escolhas feitas pelo indivíduo.

## O que é um Arquivo de Sessão?
 
Um Arquivo de Sessão é um arquivo de configuração. Sua extensão é *.txt. Ao editar um arquivo de sessão, é possível dizer que você está programando uma sessão experimental ou planejando uma sessão de ensino. Esses arquivos possuem uma linguagem própria que o software lê e executa (por exemplo, dado o nome de um arquivo ".jpg"  e uma posição na tela o software carrega esse arquivo e mostra na tela a figura correspondente na posição lida. O Arquivo de Sessão tem uma estrutura característica, com variáveis globais que funcionam para uma sessão e variáveis locais que funcionam para uma tentativa.
 
O arquivo de sessão permite o planejamento de uma grande variedade de situações de escolha e pode ser editado diretamente, para programar uma nova sessão a partir de modificações de uma sessão já pronta, ou pode-se utilizar a interface de edição.
 
## Como se planeja um Arquivo de Sessão?
 
Definem-se primeiro os valores globais. Quantas tentativas terá a sessão? Serão tentativas de escolha simples ou condicional? Recomenda-se que durante o planejamento de uma sessão, se identifiquem semelhanças entre tentativas. Usualmente um tipo de tentativa é reapresentado várias vezes em uma sessão. Tentativas com um mesmo conjunto de alternativas podem ser repetidas e alternadas, e as posiçes em que as alternativas aparecem na tela podem ser randomizadas. A interface de edição e visualização de arquivos de sessão pode economizar tempo e trabalho quanto maiores forem as semelhanças entre as tentativas de uma sessão. Tal etapa de planejamento é importante para o melhor aproveitamento da interface. O planejamento das sessões obedece princípios da área de pesquisa do pesquisador, o software admite qualquer tipo de tentativa legível, o ensino e os testes são fruto de planejamento anterior ao momento em que o pesquisador prepara o arquivo de sessão. 

## Como se escreve um Arquivo de Sessão?
 
É necessário conhecer a estrutura e a linguagem do Arquivo de Sessão. Esses são conhecimentos indispensáveis para que pequenas alterações ou o reaproveitamento de outros arquivos de sessão sejam alcançadas com êxito.
É importante ter em mente que, quando o arquivo de sessão contém um grande número de linhas, torna-se humanamente impossível escrever diretamente um arquivo de sessão em tempo hábil e sem erros mesmo conhecendo sua estrutura e linguagem. Para arquivos de sessão complexos (maiores do que 1.500 linhas), recomenda-se o uso da interface de edição/visualização de arquivos de sessão. Mesmo que o arquivo de sessão seja longo, partes do texto que se repetem podem ser substituídas com a utilização da ferramenta localizar/modificar do editor de texto.

## Quando devo utilizar a interface de edição e visualização de arquivos de sessão do EAM?

 - Quando houver a necessidade de escrever arquivos de sessão do início, por não haver ou não se tiver acesso a um arquivo de sessão que possa ser reaproveitado;
 - Tendo  acesso  a  um  arquivo  de  sessão  que  possa  ser  reaproveitado;
 - quando houver a necessidade de editar, aleatorizar ou conferir a posição de muitos estímulos;
 - editar, aleatorizar ou conferir a ordem de muitas tentativas;
 - editar ou conferir os mesmos parâmetros de diferentes tentativas; 
 - editar ou conferir os mesmos parâmetros de diferentes blocos.
 
## Quando devo utilizar a edição direta do arquivo de sessão e não utilizar a interface de edição e visualização?

Recomenda-se  a  edição direta dos  arquivos  de sessão  por  meio do  NotePad++ ou Notepad do Windows© quando houver necessidade de:
 - edição ou conferência do nome da pasta de estímulos;
 - edição ou conferência de um único parâmetro de um bloco, ou tentativa, etc;
 - localização  e  substituição  de  uma  matriz  de  estímulos  por  outra  (códigos  das posições na Secção [Positions] e nas chaves *Bnd=).

## Existem softwares livres que podem ajudar na tarefa de edição de um Arquivo de Sessão?
 
Sim. Recomenda-se o uso do software NotePAd++ (http://notepad-plus-plus.org/download/v6.5.html) para a localização e substituição de parâmetros. É possível também utilizar a opção de localização e substituição do Notepad, software padrão de edição de texto do Windows ©, e de qualquer outro programa de edição de arquivos do tipo ".txt".
 
## Qual a estrutura dos Arquivos de Sessão?
 
Cada arquivo possui uma estrutura no formato de “arquivos de configuração *.ini”:
  
    [Secção1]
        Chave=​parâmetro valor1 valor2
        Chave2=​
 
    [Secção2]
        Chave 2=​parâmetro valor1
        Chave=​parâmetro
 
 
OBS.: Atenção ao uso de tabulação entre chaves e parâmetros, o espaço é utilizado pelo software como referência para alguns parâmetros e valores.
 
OBS.: Atenção para letras maiúsculas e minúsculas e acentos, pois são aspectos sensíveis da linguagem, ou seja, afetam a configuração do arquivo.

## A ordem dessa estrutura é importante?
 
A ordem de aparecimento de cada [Secção] no arquivo de sessão não afeta sua configuração. Entretanto, há uma convenção de apresentá-las de acordo com a estrutura hierárquica do mais geral para o mais específico, com objetivo de facilitar a leitura. Cada [Secção] possui seu próprio conjunto de chaves. A ordem das chaves de uma mesma secção também não é importante. Frisa-se que a ordem de escrita dos valores de um parâmetro é importante.

## Exemplo de Arquivo de Sessão (textos entre colchetes [] não são lidos pelo programa; entre chaves {} foram explicações acrescentadas):

[Main]

Name=	DSS VIC NOVO TREINO
Type=	CRT
HootMedia=	EstÌmulos N.N
HootData=	DADOS VICT”RIA
NumBlc=	2

[Positions]

Rows=	4
Cols=	4
NumPos=	16

P1=	162 290 100 100
P2=	162 490 100 100
P3=	162 690 100 100
P4=	162 890 100 100
P5=	362 290 100 100
P6=	362 490 100 100
P7=	362 690 100 100
P8=	362 890 100 100
P9=	562 290 100 100
P10=	562 490 100 100
P11=	562 690 100 100
P12=	562 890 100 100
P13=	762 290 100 100
P14=	762 490 100 100
P15=	762 690 100 100
P16=	762 890 100 100
[Blc 1]

[{As oito primeiras linhas são variáveis de sessão: nome, tipo, pasta de arquivos, número de blocos na sessão, posição dos estímulos na tela, no caso estão programadas 16 posições em uma matriz 4 por 4. As linhas P1 a P16 mostram as coordenadas das posições na tela. 0 0 é o canto superior esquerdo. P1 a P4 são as janelas da linha superior, P5 a P8 segunda linha, P9 a P12 terceira linha e P13 a P16 a linha de baixo}]

Name=	Bloco 1
BkGnd=	0
ITI=	5000
NumCrt=	2
NumTrials=	30 0
ConsecutiveHitCriterion=	10
ConsecutiveMissCriterion=	0
MaxTrialCriterion=	30

[{As linhas 100 a 118 referem-se às variáveis do Bloco 1: 100 Bloco; 101 cor do fundo; 102 valor do IET em milisegundos, intervalo entre tentativas ou ITI intertrial interval; 103 Janela correta 2 (segunda janela da primeira linha; 104 número de tentativas do bloco; 105 critério de encerramento por acertos consecutivos; 106 critério de encerramento por erros consecutivos; 107 máximo de tentativas do bloco}]

[Blc 1 - T1] [{Aqui começa a tentativa 1 do Bloco 1}]

Name=	Tentativa 1
Kind=	SIMPLE [{Tipo: pode ser simples ou condicional}]
BkGnd=	0 [{cor do fundo}]
Cursor=	-1 [{-1 cursor invisível; 0 cursor visível}]
AutoNxt=	-1 [{?}]
CustomNxtValue=	0 [{vai para a próxima tentativa}]
NumComp=	3 [{número de escolhas, no caso de 1 a 16}]

C1Bnd=	762 290 100 100 [{posição da comparação 1, S+ ou certa}]
C1Stm=	D4.jpg 0 255 [{nome do arquivo a aparecer na posição 1}]
C1Sch=	FR 2 [{esquema ou requisito de respostas, no caso so exigidos 2 toques na comparação 1}]
C1IET=	Escolher 0 255 [{?}]
C1Usb=	3 [{porta USB acionada}]
C1Csq=	0 [{consequência programada: 0 acionamento externo, 1 consequência na tela}]
C1Msg=	D4 [{arquivo a ser mostrado como consequência}]
C1Res=	HIT [{Se a resposta ocorrer na C1 = acerto}]
C1Nxt=	0 [{próxima tentativa: 0 próxima, ?}]
C1TO=	[{?}]

C2Bnd=	162 690 100 100 [{posição da comparação 2, S- ou errada}]
C2Stm=	D5.jpg 0 255
C2Sch=	FR 2
C2IET=	Escolher 0 255
C2Usb=	0  [{porta USB desligada}]
C2Csq=	0
C2Msg=	D5  [{mensagem para erro}]
C2Res=	MISS  [{Se a resposta ocorrer na C2 = erro}]
C2Nxt=	CRT  [{se a resposta foi em C2 apresentar de novo a tentativa, correção}]
C2TO=	

C3Bnd=	362 690 100 100 [{posição da comparação 3, S- ou errada}]
C3Stm=	A6.jpg 0 255
C3Sch=	FR 2
C3IET=	Escolher 0 255
C3Usb=	0
C3Csq=	0
C3Msg=	A6
C3Res=	MISS
C3Nxt=	CRT
C3TO=	

[Blc 1 - T2] [{Aqui começa a tentativa 2 do Bloco 1}]

Name=	Tentativa 1
Kind=	SIMPLE
BkGnd=	0
Cursor=	-1
AutoNxt=	-1
CustomNxtValue=	0

NumComp=	3

C1Bnd=	162 890 100 100
C1Stm=	C4.jpg 0 255
C1Sch=	FR 2
C1IET=	Escolher 0 255
C1Usb=	3
C1Csq=	0
C1Msg=	C4
C1Res=	HIT
C1Nxt=	0
C1TO=	

C2Bnd=	362 490 100 100
C2Stm=	D5.jpg 0 255
C2Sch=	FR 2
C2IET=	Escolher 0 255
C2Usb=	0
C2Csq=	0
C2Msg=	D5
C2Res=	MISS
C2Nxt=	CRT
C2TO=	

C3Bnd=	162 690 100 100
C3Stm=	B6.jpg 0 255
C3Sch=	FR 2
C3IET=	Escolher 0 255
C3Usb=	0
C3Csq=	0
C3Msg=	B6
C3Res=	MISS
C3Nxt=	CRT
C3TO=	

[Blc 1 - T3] [{Aqui começa a tentativa 3, do Bloco 1, etc}]

[{...}]

[Blc 1 - T30]  [{Aqui começa a tentativa 30 do Bloco 1}]

Name=	Tentativa 1
Kind=	SIMPLE
BkGnd=	0
Cursor=	-1
AutoNxt=	-1
CustomNxtValue=	0

NumComp=	3

C1Bnd=	762 290 100 100
C1Stm=	B4.jpg 0 255
C1Sch=	FR 2
C1IET=	Escolher 0 255
C1Usb=	3
C1Csq=	0
C1Msg=	B4
C1Res=	HIT
C1Nxt=	0
C1TO=	

C2Bnd=	162 890 100 100
C2Stm=	B5.jpg 0 255
C2Sch=	FR 2
C2IET=	Escolher 0 255
C2Usb=	0
C2Csq=	0
C2Msg=	B5
C2Res=	MISS
C2Nxt=	CRT
C2TO=	

C3Bnd=	762 490 100 100
C3Stm=	D6.jpg 0 255
C3Sch=	FR 2
C3IET=	Escolher 0 255
C3Usb=	0
C3Csq=	0
C3Msg=	D6
C3Res=	MISS
C3Nxt=	CRT
C3TO=	

[Blc 2]  [{Aqui começa o Bloco 2}]

Name=	Bloco 2
BkGnd=	0
ITI=	5000
NumCrt=	2
NumTrials=	30 0
ConsecutiveHitCriterion=	10
ConsecutiveMissCriterion=	0
MaxTrialCriterion=	30

[Blc 2 - T1]

Name=	Tentativa 1
Kind=	SIMPLE
BkGnd=	0
Cursor=	-1
AutoNxt=	-1
CustomNxtValue=	0

NumComp=	12  [{Número de comparações nas tentativas do Bloco 2 = 12}]

C1Bnd=	362 890 100 100  [{Aqui começa a comparação 1 da tentativa 1 do Bloco 2}]
C1Stm=	C4.jpg 0 255
C1Sch=	FR 2
C1IET=	Escolher 0 255
C1Usb=	3
C1Csq=	0
C1Msg=	C4
C1Res=	HIT
C1Nxt=	0
C1TO=	

C2Bnd=	362 490 100 100 [{Aqui começa a comparação 2 da tentativa 1 do Bloco 2}]
C2Stm=	D2.jpg 0 255
C2Sch=	FR 2
C2IET=	Escolher 0 255
C2Usb=	0
C2Csq=	0
C2Msg=	D2
C2Res=	MISS
C2Nxt=	CRT
C2TO=	

[{...}]

C12Bnd=	162 890 100 100 [{Aqui começa a comparação 12 da tentativa 1 do Bloco 2}]
C12Stm=	D12.jpg 0 255
C12Sch=	FR 2
C12IET=	Escolher 0 255
C12Usb=	0
C12Csq=	0
C12Msg=	D12
C12Res=	MISS
C12Nxt=	CRT
C12TO=	

[Blc 2 - T2] [{Aqui começa a tentativa 2 do Bloco 2}]

Name=	Tentativa 1
Kind=	SIMPLE
BkGnd=	0
Cursor=	-1
AutoNxt=	-1
CustomNxtValue=	0

NumComp=	12

C1Bnd=	562 290 100 100
C1Stm=	A4.jpg 0 255
C1Sch=	FR 2
C1IET=	Escolher 0 255
C1Usb=	3
C1Csq=	0
C1Msg=	A4
C1Res=	HIT
C1Nxt=	0
C1TO=	

 [{...}]
 
C12Bnd=	362 690 100 100
C12Stm=	B12.jpg 0 255
C12Sch=	FR 2
C12IET=	Escolher 0 255
C12Usb=	0
C12Csq=	0
C12Msg=	B12
C12Res=	MISS
C12Nxt=	CRT
C12TO=	

[Blc 2 - T3]  [{Aqui começa a tentativa 3 do Bloco 2}]

Name=	Tentativa 1
Kind=	SIMPLE
BkGnd=	0
Cursor=	-1
AutoNxt=	-1
CustomNxtValue=	0

NumComp=	12

C1Bnd=	162 490 100 100
C1Stm=	A4.jpg 0 255
C1Sch=	FR 2
C1IET=	Escolher 0 255
C1Usb=	3
C1Csq=	0
C1Msg=	A4
C1Res=	HIT
C1Nxt=	0
C1TO=	

[Blc 2 - T30]  [{Aqui começa a tentativa 30 do Bloco 2}]

Name=	Tentativa 1
Kind=	SIMPLE
BkGnd=	0
Cursor=	-1
AutoNxt=	-1
CustomNxtValue=	0

NumComp=	12

C1Bnd=	162 890 100 100
C1Stm=	E4.jpg 0 255
C1Sch=	FR 2
C1IET=	Escolher 0 255
C1Usb=	3
C1Csq=	0
C1Msg=	E4
C1Res=	HIT
C1Nxt=	0
C1TO=	

C2Bnd=	562 490 100 100
C2Stm=	E2.jpg 0 255
C2Sch=	FR 2
C2IET=	Escolher 0 255
C2Usb=	0
C2Csq=	0
C2Msg=	E2
C2Res=	MISS
C2Nxt=	CRT
C2TO=	

C3Bnd=	162 490 100 100
C3Stm=	E3.jpg 0 255
C3Sch=	FR 2
C3IET=	Escolher 0 255
C3Usb=	0
C3Csq=	0
C3Msg=	E3
C3Res=	MISS
C3Nxt=	CRT
C3TO=	

C4Bnd=	562 290 100 100
C4Stm=	E1.jpg 0 255
C4Sch=	FR 2
C4IET=	Escolher 0 255
C4Usb=	0
C4Csq=	0
C4Msg=	E1
C4Res=	MISS
C4Nxt=	CRT
C4TO=	

C5Bnd=	162 690 100 100
C5Stm=	E5.jpg 0 255
C5Sch=	FR 2
C5IET=	Escolher 0 255
C5Usb=	0
C5Csq=	0
C5Msg=	E5
C5Res=	MISS
C5Nxt=	CRT
C5TO=	

C6Bnd=	362 690 100 100
C6Stm=	E6.jpg 0 255
C6Sch=	FR 2
C6IET=	Escolher 0 255
C6Usb=	0
C6Csq=	0
C6Msg=	E6
C6Res=	MISS
C6Nxt=	CRT
C6TO=	

C7Bnd=	162 290 100 100
C7Stm=	E7.jpg 0 255
C7Sch=	FR 2
C7IET=	Escolher 0 255
C7Usb=	0
C7Csq=	0
C7Msg=	E7
C7Res=	MISS
C7Nxt=	CRT
C7TO=	

C8Bnd=	362 290 100 100
C8Stm=	E8.jpg 0 255
C8Sch=	FR 2
C8IET=	Escolher 0 255
C8Usb=	0
C8Csq=	0
C8Msg=	E8
C8Res=	MISS
C8Nxt=	CRT
C8TO=	

C9Bnd=	762 290 100 100
C9Stm=	E9.jpg 0 255
C9Sch=	FR 2
C9IET=	Escolher 0 255
C9Usb=	0
C9Csq=	0
C9Msg=	E9
C9Res=	MISS
C9Nxt=	CRT
C9TO=	

C10Bnd=	562 890 100 100
C10Stm=	E10.jpg 0 255
C10Sch=	FR 2
C10IET=	Escolher 0 255
C10Usb=	0
C10Csq=	0
C10Msg=	E10
C10Res=	MISS
C10Nxt=	CRT
C10TO=	

C11Bnd=	362 890 100 100
C11Stm=	E13.jpg 0 255
C11Sch=	FR 2
C11IET=	Escolher 0 255
C11Usb=	0
C11Csq=	0
C11Msg=	E13
C11Res=	MISS
C11Nxt=	CRT
C11TO=	

C12Bnd=	762 890 100 100
C12Stm=	E12.jpg 0 255
C12Sch=	FR 2
C12IET=	Escolher 0 255
C12Usb=	0
C12Csq=	0
C12Msg=	E12
C12Res=	MISS
C12Nxt=	CRT
C12TO=	
 [{Final do arquivo de sessão}]

# Perguntas frequentes sobre os relatórios de sessão.

## Quais são os relatórios do EAM? 
O EAM possui dois tipos de arquivos de relatório `Dados_001.txt`  e `Ticks_001.txt`. 

## O EAM salva por cima dos arquivos existentes?
O EAM nunca salvará um arquivo por cima de outro já existente. Por exemplo, ao nomear como `Dados_001.txt`, se este arquivo já existe, o novo arquivo será automaticamente renomeado para `Dados_002.txt`. 

## Qual o formato dos arquivos de relatório?
O arquivo segue um formato tabelado, com o caracter ASCII DEC 9 (TAB) como separador. Para visualizar os relatórios rapidamente, recomenda-se o uso de gerenciadores de planilhas como o programa Excel do pacote Microsoft© Office ou Gnumeric.  

## Como analisar os dados dos relatórios? 
Nunca altere o conteúdo dos arquivos de relatório originalmente produzidos. Faça uma cópia de segurança dos arquivos a serem analisados. Em seguida, recomenda-se o uso de macros, scripts em Python, a linguagem R, ou outras linguagens que possibilitem a automação da análise dos relatórios, e de uma eventual formatação se necessária. 

## Como está estruturado o arquivo de relatório `Dados_001`? 
O arquivo possui um cabeçalho, um corpo e um rodapé.

#### Cabeçalho: 

```bash
# Nome do sujeito definido no início da sessão pelo usuário. 
Sujeito: Bongo
  
# Nome da sessão definida no Arquivo de Sessão `[Main] > Name=` pelo usuário.
# Caso a chave `[Main] > Name=` seja omitida do arquivo, o nome do Arquivo de Sessão é utilizado. 
Sessão: 001 
  
# Data de criação do arquivo de relatório (Dados_001),
# de acordo com o relógio do sistema operacional do computador. 
Data:dd/m/aaaa 
  
# Tempo do início da sessão, de acordo com o relógio do sistema operacional do computador. 
Hora de Início:hh:mm:ss AM/PM
``` 

#### Rodapé:
```bash
# Tempo de término da sessão, de acordo com o relógio do sistema operacional do computador. 
Hora de Término: hh:mm:ss AM/PM
```
#### Corpo:
O corpo é formado por colunas e linhas. Cada coluna é uma variável de registro referente a um bloco ou a uma tentativa da sessão.

##### Blocos

> Nome do Bloco. 

Definido no Arquivo de Sessão: `[Blc 1] > Name= Nome do Bloco`. Apenas o nome é mostrado, logo acima das tentativas do bloco. 

##### Tentativas

> Núm.Tent. 

Número da tentativa. Composto por dois números. O primeiro é o número da tentativa no arquivo de sessão de acordo com a numeração das secções das tentativas: `[Blc 1 - T1], [Blc 1 - T2] ... [Blc 1 - Tn]`. O segundo é o número de acordo com o Contador Cumulativo de Tentativas interno do programa. 

> Nom.Tent. 

Nome da tentativa. Definido no Arquivo de Sessão: `[Blc 1 - T1] > Name=`. 

##### Modelo

> Pos.Mod. 

Mensagem do relatório do modelo que convencionalmente deve incluir o nome do estímulo e a posição (ex. A1 – 1, A2 – P3, etc.). Definido no Arquivo de Sessão: `[Blc 1 - T1] > SMsg=`. 

> Res.Mod. 

Mensagem do relatório do modelo cujo esquema de respostas foi cumprido. Convencionalmente deve incluir o nome do estímulo e a posição (ex. A1 – 1, A2 – P3, etc.). Definido no Arquivo de Sessão: `[Blc 1 - T1] > SMsg=`. 
 
> Lat.Mod. 

Latência. Tempo em milisegundos entre a apresentação do estímulo e a primeira resposta ao estímulo. Um estímulo pode ser entendido como uma caixa com comprimento e altura em pixels (width height) posicionada em um ponto (top, left) na tela do monitor. 

> Dur.Mod. 

Duração da resposta ao estímulo. No caso de esquemas que permitem múltiplas respostas, o tempo em milisegundos entre a primeira e última resposta. Para obter o tempo entre respostas específicas (ex., entre a segunda e terceira), conferir relatório de Ticks_001 correspondente). 

> Tmp.Mod. 

Latência + Duração da resposta ao estímulo. Confira os itens: `Lat.Mod.` a `Dur.Mod`. 

> Atraso 

Nome do atraso entre modelo e comparações definido no Arquivo de Sessão `[Blc 1 - T1] > Delay=`. 


OBS.: As variáveis de registro relacionadas ao modelo estão disponíveis apenas de acordo com o tipo de tentativa MTS.

#### Discriminação simples

> Pos.Cmp. 

Conjunto de mensagens de relatório de todos os estímulos de comparação de uma tentativa. Convencionalmente, cada mensagem deve incluir o nome do estímulo e a posição (ex. A1 – 1, A2 – P3, etc.). Definido no Arquivo de Sessão: [Blc 1 - T1] > C1Msg=, C2Msg= ... CnMsg=. 

A mensagem ‘GONOGO’ produz o caracter ‘1’ para GO e ‘2’ para ‘NOGO’ se, e somente se, houver o cumprimento de esquemas concorrentes (ex. FTFR, VTVR, etc). 


> Res.Cmp. 

Mensagem do relatório da comparação cujo esquema de respostas foi cumprido. Convencionalmente deve incluir o nome do estímulo e a posição (ex. A1 – 1, A2 – P3, etc.). Definido no Arquivo de Sessão: `[Blc 1 - T1] > C1Msg=`, `C2Msg=` ... `CnMsg=`. 

> Lat.Cmp. 

Latência. Tempo em milisegundos entre a apresentação do estímulo e a primeira resposta ao estímulo. Um estímulo pode ser entendido como uma caixa com comprimento e altura em pixels (width height) posicionada em um ponto (top, left) na tela do monitor. 

 
> Dur.Cmp. 

Duração da resposta ao estímulo. No caso de esquemas que permitem múltiplas respostas, o tempo em milisegundos entre a primeira e última resposta. Para obter o tempo entre respostas específicas (ex., entre a segunda e terceira), conferir relatório de `Ticks_001` correspondente). 


> Tmp.Cmp. 

Latência + Duração da resposta ao estímulo. 

Conferir itens: `Lat.Mod.` e `Dur.Mod`. 

> Disp. 

Código binário (2^8) enviado para a interface pela porta paralela. Por exemplo, 00000000, 00000001. 

> UDsp. 

Caracter (1, 2, 3 ou 4) enviado para a interface pelo protocolo RS232, pela porta USB. Permite a identificação de acertos e erros quando comparado ao nome da tentativa (Nom.Tent) e a resposta a comparação (Res.Cmp.). 

 
> Res.Frq. 

Composto por um conjunto de Contadores de Respostas e coordenadas das respostas em relação a tela do monitor.
Permite a contagem de acertos mais facilmente se a convenção de configurar o primeiro estímulo sempre como correto for respeitada: 

```bash
# Exemplo
Res.Frq. 
C1=0 C1=1 C2= 0 Cn=0 BK=3 509-393 484-338 424-365 
```

As coordenadas `top-left` de respostas ao fundo da tela, no qual `top` refere-se ao pixel vertical de cima para baixo, e `left` horizontal da esquerda para direita.

> 509-393 484-338 424-365 
 

## Como está estruturado o arquivo de relatório `Ticks_001`? 

Esse arquivo contém informações sobre cada resposta ao longo de uma sessão. Com ele é possível obter o tempo entre cada resposta.

##### Tentativas

> Tempo_ms 

Tempo em milisegundos entre a resposta e a resposta anterior. O tempo da primeira resposta é igual a Latência no arquivo `Dados_001`. 

> Stm.Tipo 

Categoria da resposta: 

- `M1` : resposta ocorreu no estímulo modelo. 

- `C1`, `C2` ... `Cn`: resposta ocorreu em um estímulo de comparação. 

- `-` = resposta ocorreu no fundo da tela. 

 

> FileName 

O nome do arquivo de estímulo onde da caixa onde a resposta ocorreu (ex.: A1.jpg). 

> Left.... 

Left da Coordenada Left-Top, de acordo com a resolução da tela no momento do toque. 


> Top..... 

Top da Coordenada Left-Top, de acordo com a resolução da tela no momento do toque. 

`top` refere-se ao pixel vertical de cima para baixo, e `left` horizontal da esquerda para direita.

 
