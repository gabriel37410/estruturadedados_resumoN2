=====Pilhas=====

    É uma lista linear em que todas as inserções, retiradas e, geralmente, todos os acessos são feitos em apenas um extremo da lista.

    Os itens são colocados um sobre o outro. O item inserido mais recentemente está no topo e o inserido menos recentemente no fundo.

    O modelo intuitivo é o de um monte de pratos em uma prateleira, sendo conveniente retirar ou adicionar pratos na parte superior.

    Propriedade: o último item inserido é o primeiro item que pode ser retirado da lista.

    Existe uma ordem linear para pilhas, do “mais recente para o menos recente”.

    É ideal para processamento de estruturas aninhadas de profundidade imprevisível.

    Uma pilha contém uma seqüência de obrigações adiadas. A ordem de remoção garante que as estruturas mais internas serão processadas antes das mais externas.

    Existem várias opções de estruturas de dados que podem ser usadas para representar pilhas. As duas representações mais utilizadas são as implementações por meio de vetores e de estruturas encadeadas.


=====Listas=====

    ==Linear==
    Lista linear é uma estrutura de dados na qual elementos de um mesmo tipo de dado estão organizados de maneira sequencial. Não necessariamente, estes elementos estão fisicamente em sequência, mas a idéia é que exista uma ordem lógica entre eles.

    ==Dinâmica==
    Lista encadeada é uma estrutura de dados linear e dinâmica. Ela é composta por uma sequência de células que contém seus dados e também uma ou duas referências que apontam para a célula anterior ou posterior. Há diversos modelos de lista como por exemplo lista encadeada simples e listas duplamente encadeada.

    Para se "ter" uma lista encadeada, basta guardar seu primeiro elemento, e seu último elemento aponta para uma célula nula.

    Para manipularmos estas listas nomeadamente: inserir dados ou remover dados temos que ter sempre atenção em ter um ponteiro que aponte para o 1º elemento e outro que aponte para o fim, isto porque se queremos inserir ou apagar dados que estão no inicio ou no fim da lista então a operação é rapidamente executada caso seja um nó que esteja no meio da lista pois terá que haver uma procura até encontrar a posição desejada.

    Lista encadeada simples: Uma lista encadeada simples é aquela que contém apenas uma referencia por celula. Esta referencia aponta para a próxima celula da lista, ou para um valor nulo (vazio) quando se trata de uma celula final.

    Lista duplamente encadeada: Listas duplamente encadeadas ou lista de duas vias, são um modelo mais sofisticado das listas simples, cada celula possui dois ponteiros, um que aponta para a celula anterior (ou null se é o primeiro valor ou a lista está vazia) e outro que aponta para a próxima celula (ou null se é o último valor ou a lista está vazia).


=====Alocação de Memoria=====

    O espaço de endereços de um processo em execução é dividido em várias áreas distintas. As mais importantes são:

    -Text: contém o código do programa e suas constantes. Esta área é alocada durante a chamada exec e permanece do mesmo tamanho durante toda a vida do processo.
    -Data e BSS: são as áreas onde o processo armazena suas variáveis globais e estáticas. Têm tamanho fixo durante a execução do processo.
    -Stack: contém a pilha de execução, onde são armazenadas os parâmetros, endereços de retorno e variáveis locais de funções. Pode variar de tamanho durante a execução do processo.
    -Heap: contém áreas de memória alocadas a pedido do processo, durante sua execução. Varia de tamanho durante a vida do processo.

    Em um programa em C temos por exemplo basicamente três tipos de alocação de memoria: estática, automática e dinâmica.

    -Alocação estática: 
      A alocação estática ocorrem com variáveis globais (alocadas fora de funções) ou quando variáveis locais (internas a uma função) são alocadas usando o modificador static. Uma variável alocada estaticamente mantém seu valor durante toda a vida do programa, exceto quando explicitamente modificada.
    -Alocação automática: 
      Por default, as variáveis definidas dentro de uma função (variáveis locais e parâmetros) são alocadas de forma automática na pilha de execução do programa (stack) a cada chamada da função, sendo descartadas quando a função encerra. Se a função for chamada recursivamente, as variáveis locais e parâmetros serão novamente alocados na pilha, em áreas distintas para cada nível de recursão.Isso permite preservar os valores anteriores dos mesmos no retorno dos níveis de recursão.
    -Alocação dinâmica: 
      Quando o processo requisita explicitamente um bloco de memória para armazenar dados; o controle das áreas alocadas dinamicamente é manual ou semi-automático, o programador é responsável por liberar as áreas alocadas dinamicamente. A alocação dinâmica geralmente usa a área de heap. O programa solicita explicitamente áreas de memória ao sistema operacional, as utiliza e depois as libera quando não forem mais necessárias, ou quando o programa encerrar. A memoria pode ser alocada dinamicamente através da chamada malloc, é a memoria pode ser liberada através da chamada free.