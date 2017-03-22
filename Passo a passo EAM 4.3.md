# COMO INSTALAR O EAM 

O EAM não necessita de instalação já que o software é um auto executável. Para que o software funcione em seu computador, 
basta somente copiar a pasta com dois arquivos pré-existentes que são o “eam 4.3” e o “inpout32.dll”. Após esse processo 
cole no local desejado pelo usuário. Dê um clique duplo no icone "eam 4.3" e ele executará e ficará pronto para ser 
configurado, porém, é necessário antes de iniciar uma configuração de sessão para criar diretórios de dados e estímulos.

# CRIANDO DIRETÓRIOS

Assim que a pasta do EAM 4.3 estiver criada, acesse-a. Dentro dessa pasta você encontrará somente 2 arquivos 
(eam 4.3 e o inpout32.dll).

1. Abra o software;
2. clique em "arquivos > novo arquivo de configuração" e uma janela chamada "nova sessão" irá aparecer. 
3. Dentro dessa janela você irá nomear a sessão. 
4. Após nomeada a sessão, dê um duplo clique em "pasta de dados" e uma nova janela chamada "Procurar pasta" abrirá. 
5. Procure a pasta EAM 4.3 e dê um único clique em cima dela. 
6. Clique em "Criar Nova Pasta" e nomeie a pasta com o nome chamada "Dados" e clique em "OK". 
7. Em seguida, dê um duplo clique em "Pasta de Estímulos" e uma nova janela chamada "Procurar Pasta" abrirá. 
8. Procure a pasta EAM 4.3 e dê um duplo clique em cima dela e em seguida dê um único clique na pasta "Dados". 
9. Clique em "Criar Nova Pasta" e nomeie a pasta com o nome "Estímulos" e clique em OK. 
10. Depois de criadas as pastas clique em "Avançar" e os diretórios estarão criados.

# ARQUIVOS DOS DIRETÓRIOS

## Pasta - Estímulos

Nesta pasta serão encontrados arquivos em mídia (imagem, animação, audio ou vídeo).

Quando o usuário estiver procurando as mídias na internet para serem usados na sua sessão, o mesmo deve ficar atento 
para o formato suportado pelo software. Para cada mídia, formatos específicos são exigidos. Caso o usuário queira usar
imagens como estímulos, o mesmo deverá optar pelos seguintes formatos: JPEG ou BMP com dimensões variando entre 1
40 a 180 x 140 a 180 (é importante manter a altura e o comprimento iguais ex: 160x160, para que a imagem não fique 
distorcida). Se quiser uma animação o formato deve ser: GIF. Para os arquivos de audio, o formato deve ser: MAV ou MID. 
Por fim, se for utilizar vídeos, o formato deve ser: MPG, AVI, MOV ou WMV.

Obs. 
O software não restringe o uso de mídias (sons, vídeos ou animações) com base em tamanho e duração.
O software restringe o uso de mídias com base em extenções (.bmp,.wav,.mov,.gif, e assim por diante).
As extenções permitidas podem ser conferidas [aqui](https://github.com/eep-lab/eam/blob/master/Units/uKey.pas#L366-L384).

Entretanto, considerando um computador com processador Pentium Core 2 Duo com 2gb de memória (DDR2),
recomenda-se o uso de mídias com no máximo 2 mb para que o carregamento e descarregamento das mídias
ocorram com o mínimo de atraso (~200 ms). Tamanhos maiores tenderão a gerar maiores atrasos entre tentativas.

Ainda precisamos colocar em teste esses tipos de mídia para ver
quais as exigências mínimas e máximas suportadas por outros computadores rodando o software.

Obs. 2: O software carrega e descarrega vídeos, sons e imagens em tempo real.
Isso significa que o computador deve possuir mais processamento e memória
para que mídias grandes (> 2 mb) sejam carregadas e descarregadas com o mínimo de atraso entre tentativas.


## Pasta - Dados

Dentro da pasta Dados, é onde serão salvos os arquivos em formato “txt” após rodar a sessão, chamados “Dados_001.txt” e 
“Ticks_001.txt”, referentes a eventos específicos que aconteceram durante a sessão, como: número de tentativas, quantas 
vezes o sujeito errou ou acertou, o tempo que levou para o sujeito escolher um estímulo, atraso, correções, entre outras 
coisas. Para mais informações acesse o GitHub>eep-lab/eam_docs>Como está estruturado o arquivo de relatório Dados_001?). 

Obs.
É importante lembrar que esse arquivo gerado pelo software não é o arquivo de configuração, pois o arquivo de configuração 
é o arquivo salvo “txt” que contém a estrutura da sessão e não o que ocorreu durante a sessão.

Por fim, após seguir esses passos o software estará pronto para que o usuário configure uma sessão.
