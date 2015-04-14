# Perguntas frequentes sobre os relatórios de sessão. 

## Quais são os relatórios do EAM? 
O EAM possui dois tipos de arquivos de relatório `Dados_001.txt`  e `Ticks_001.txt`. 

## O EAM salva por cima dos arquivos existentes?
O EAM nunca salvará um arquivo por cima de outro já existente. Por exemplo, ao nomear como `Dados_001.txt`, se este arquivo já existe, o novo arquivo será automaticamente renomeado para `Dados_002.txt`. 

## Qual o formato dos arquivos de relatório?
O arquivo segue um formato tabelado, com o caracter ASCII DEC 9 (TAB) como separador. Para visualizar os relatórios rapidamente, recomenda-se o uso de gerenciados de ficheiros como o programa Excel do pacote Microsoft© Office ou Gnumeric.  

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
#### Corpo
O corpo é formado por colunas e linhas. Cada coluna é uma variável de registro referente a um bloco ou a uma tentativa da sessão.

#### Blocos

> Nome do Bloco. 

Definido no Arquivo de Sessão: `[Blc 1] > Name= Nome do Bloco`. Apenas o nome é mostrado, logo acima das tentativas do bloco. 

#### Tentativas

> Núm.Tent. 

Número da tentativa. Composto por dois números. O primeiro é o número da tentativa no arquivo de sessão de acordo com a numeração das secções das tentativas: `[Blc 1 - T1], [Blc 1 - T2] ... [Blc 1 - Tn]`. O segundo é o número de acordo com o Contador Cumulativo de Tentativas interno do programa. 

> Nom.Tent. 

Nome da tentativa. Definido no Arquivo de Sessão: `[Blc 1 - T1] > Name=`. 

#### Modelo

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

#### Tentativas

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

 
