# Simulador Algoritmos de Escalonamento
Esse programa foi feito para o estudo dos Algoritimos de escalonamento de processos da matéria de Sistemas Operacionais do Curso de Ciências da Computação da UniCEUB Brasilia, o código foi feito em `C`.

----------------------------------
Informação dos Autores
----------------------------------
Nome: Angelo Soares Dorfey\
E-mail: usbangelo@sempreceub.com

---------------------------------
Descrição da Aplicação
---------------------------------
Uma simples implementação em C de alguns algoritmos de escalonamento de processos. 
Algoritmos de Escalonamento Implementados:

Algoritmos implementados:

 * First In, First Out (FIFO)
> Prioriza ordem de chegada.
> Primeiro que entra é o primeio que sai.
> Desvantagem: Tempo médio de espera grande.
    > Sensação de multiprogramação prejudicada se os primeiros processos forem muito longos.

 * Prioridade #Preemptivo
> Fila ordenada de processos.
> O processo de menor valor de prioridade obtem prioridade maior na fila de processos.
> Valor maior prioridade é executado na fila usando Round Robin.
> Desvantagem:
    >Postergação infinita (se um processo tiver um valor alto com inumero processos na frente, talvez ele nunca possa ser executado).

 * Round Robin (RR) #Preemptivo
> Processos entram no final da fila, são executados através de chamadas do sistema.
> Utiliza fatias de tempo (quantum / valor razoavel entre 20-50mseg).
> Fatias de tempo controladas por interrupções, caso os processos que não concluam eles são parados e outros são executados.
> Desvantagem:
    > Como definir a duração das fatias de tempo?
        > - Se for muito pequeno os alguns processos podem se prejudicar com pouco processamento.
        > + Se for muito grande o tempo, perde a noção de multiprogramação.

 * Smallest Job First (SJF)
> Prioriza tempo de execução.
> Começa pelo processo com menos tempo de execução.
> Organiza fila do menor para o maior em nivel de prioridade, reduzindo tempo de espera.
> Desvantagem:
    > Como definir o tempo de execução (não é possivel saber no mundo real)
    > Soluções: Aproximação baseada nas médias de tempo das ultimas execuções do processador.

Métricas avaliadas:
1. Identificação do processo;
2. Tempo de duração do processo;
3. Prioridade;
4. Tempo de execução;
5. Tempo de espera.

-----------------------------------------------------
Compilação e Execução do programa
-----------------------------------------------------
Para execultar o programa no Linux use os seguintes comandos no terminal e pasta do arquivo: 

Compile o arquivo `.c` usando `gcc`:
```
gcc simulador-escalonamentop.c -o simulador-escalonamentop
```

Para executar o programa:
```
./simulador-escalonamentop
```