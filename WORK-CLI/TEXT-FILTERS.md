#### `seq  1 100 > numeros.txt

Cria o arquivo numeros.txt já preenchido com uma **sequência** de 1 a 100.

------------------------------------------------------------------------
#### `bzip2 -k compact.txt

**Compacta** o arquivo compact.txt no formato ==bz2==. O **-k** é de (keep), para ao converter, ==manter== na pasta o arquivo que foi compactado.
Arquivo compactado: **compact.txt.bz2**

#### `bzcat compact.txt.bz2
Consigo ver o conteúdo do arquivo que está compactado.

#### `bzcat compact.txt.bz2 | wc -w
## **Detalhes**

- **`wc`** significa **word count** (contagem de palavras).
    
- A opção **`-w`** faz com que ele conte apenas ==palavras==.

`wc` pode contar **linhas** (`-l`), **palavras** (`-w`) e **caracteres** (`-m` ou `-c` dependendo da versão).

#### `bzcat compact.txt.bz2 > recebendo.txt

Vai **jogar o conteúdo** do arquivo compact **para dentro** do arquivo recebendo.txt 

------------------------------------------------------------------------
`cat
 **Exibe** conteúdo de arquivos: `cat arquivo.txt

`cat arquivo1.txt arquivo2.txt > arquivo_combinado.txt
**Concatena** o conteúdo dos dois arquivos **direcionando** para um novo arquivo

`cat -n recebendo.txt
Exibe o conteúdo do arquivo em linhas numeradas
Ex: 
**1** Conteúdo arquivo1
**2** Conteúdo arquivo2

`cat -b recebendo.txt
A flag **-b** irá numerar apenas as linhas ==não vazias==.

`cat -E numeros.txt
Imprime com **caracteres de fim de linha** visíveis

Saída: 
		1,2,3==$==
		4,5,6==$==
		7,8,9==$==

------------------------------------------------------------------------
`cut
"**Cortar**" o documento e trazer apenas aquilo que você quer. É importante você analizar um documento antes de utilizar o comando, para verificar qual delimitador os dados estão utilizando e encontrar o melhor possível.

`cut -d "," -f 2 numeros.txt

**-d** = ==delimitador== será uma vírgula **' , '**
**-f** =  Pegue o segundo **2** ==field== (campo) de cada linha do arquivo **numero.txt**

Saída:
		2
		5
		8

`cut -d ',' -f 2,3 numeros.txt
Pego o ==field== 2 e 3

------------------------------------------------------------------------


