#### `sed
Permite **editar texto em fluxo** , ou seja, modificar arquivos **linha a linha** sem abrir um editor interativo.

`sed 's/Uva/Abacate/' frutas.txt 
**Substitui** a palavra **Uva** pela palavra Abacate  

`sed '/^$/d' frutas.txt
**Deleta** as linhas vazias do começo ao final do arquivo.

`sed -i 's/Uva/Abacate/g' frutas.txt
**Substitui** diretamente no arquivo (em definitivo)

------------------------------------------------------------------------

#### `sha256sum

Os comandos **`sha256sum`e`sha512sum no Linux funcionam de forma semelhante ao md5sum

Eles são usados principalmente para **verificar a integridade e proteção** dos arquivos, garantindo que não foram prejudicados ou alterados.

## Diferença entre SHA-256 e SHA-512

| Algoritmo   | Tamanho do hash                        | Segurança                                       | Velocidade                                     |
| ----------- | -------------------------------------- | ----------------------------------------------- | ---------------------------------------------- |
| **SHA-256** | 256 bits → 64 caracteres hexadecimais  | Muito seguro, padrão atual em várias aplicações | Mais rápido que SHA-512 em sistemas de 32 bits |
| **SHA-512** | 512 bits → 128 caracteres hexadecimais | Ainda mais seguro (mais difícil quebrar)        | Mais rápido em sistemas de 64 bits             |

------------------------------------------------------------------------

#### ``sort

Serve para **Ordenar** linhas de texto em um arquivo ou da entrada padrão (stdin).

`sort frutas.txt
Ordena as frutas em ordem alfabética.

`sort -n numeros.txt
Ordena em ordem númerica

`sort -r numeros.txt
Ordena em ordem reversa

`sort -t ":" -k2 departments.txt
**-t** **":"**= Define dois pontos como separador
**-k2** = Diz que a consulta será ordenada pela segunda coluna

![[Pasted image 20250823225032.png]]


