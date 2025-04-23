- A notar: scanf(%45s", &buffer) permite um exploit de buffer overflow, já que permite escrever 45 bytes num buffer com tamanho 32. O programa chama da função, utilizando a variável buffer como argumento.

![Filler](Images/CTF 5/First.png)

*Fig. 1 - Função main*


- Com isto em mente devemos mudar o endereço da nossa função, fun, para o endereço do readtxt e torná-lo num cat flag.txt.
Encontrámos então o endereço deste nosso ficheiro.

![Filler](Images/CTF 5/Second.png)

*Fig. 2 - Endereço encontrado*


- Posteriormente, alteramos o valor do payload e corremos o exploit-template.py localmente.

![Filler](Images/CTF 5/Third.png)

*Fig. 3 - Exploit executado localmente*


![Filler](Images/CTF 5/Fourth.png)

*Fig. 4 - Resultado do exploit local*


- Como o exploit foi executado com sucesso, excutámo-lo em remote.

![Filler](Images/CTF 5/Fifth.png)

*Fig. 5 - Exploit executado no remote*


- Obtivemos então a seguinte flag:

![Filler](Images/CTF 5/Sixth.png)

*Fig. 6 - Flag final obtida*