# programmingTips

montar de volta dado float enviado pela serial big edian / little edian fazer inversão

~~~
/******************************************************************************
Converter dado bytes recebidos pela serial de volta para float
https://www.onlinegdb.com/online_c_compiler
by: Francisval G.
*******************************************************************************/
#include <stdio.h>

int main()
{
    char dado[] = "\x00\xE0\xB8\xBF"; // \0x para inserir o dado em hex, mas pode inserir em decimal bytes[0]=0 ...
    float *p; // cria um ponteiro float    
    p = (float*)(&dado); // coloca no ponteiro floa o endereço do vetor de char (dado tem que ter exatamente 4 bytes)    
    printf("%f", *p); // imprime o conteudo de dado em float
    return 0;
}
~~~
