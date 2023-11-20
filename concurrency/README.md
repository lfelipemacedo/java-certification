# Concurrency e Multithreading

Concurrency (Concorrência) se refere ao fato de uma aplicação poder fazer mais de uma tarefa ao mesmo tempo.

Ao executar uma aplicação, temos um processo em execução em alguma máquina. Este processo tem seu próprio espaço de memória, chamado **Heap Space**.
O Heap não pode ser compartilhado entre múltiplos processos, tendo cada processo o seu próprio heap space

Dentro de uma aplicação, ou um processo, podemos executar múltiplas unidades de execução, chamadas Threads. Cada aplicação tem ao menos uma thread, chamada de **Main Thread**.

Cada Thread compartilhará o espaço de memória utilizado por seu processo, no caso seu Heap Space, porém cada Thread tem um espaço de memória reservado a ela, chamado **Thread Stack**

## Java Threads - Básico
Podemos criar Threads de 2 formas

- Estendendo a classe Threads
- Criando uma Thread passando um runnable por construtor

A classe Thread implementa a interface Runnable e, com isso, implementa o método *run()*

### Métodos run() e start()
Podemos executar uma thread de forma assíncrona e síncrona e essa é a principal diferença entre os métodos run() e start().
O método start() executa uma thread de forma assíncrona e o método run() de forma síncrona.