># Design Patterns
>### Strategy
>    O padrão Strategy é muito útil quando temos um conjunto de algoritmos similares, 
    e precisamos alternar entre eles em diferentes pedaços da aplicação.
>
>   O Strategy nos oferece uma maneira flexível para escrever diversos algoritmos 
    diferentes, e de passar esses algoritmos para classes clientes que precisam deles.
    Esses clientes desconhecem qual é o algoritmo "real" que está sendo executado, 
    e apenas mandam o algoritmo rodar. Isso faz com que o código da classe cliente 
    fique bastante desacoplado das implementações concretas de algoritmos, 
    possibilitando assim com que esse cliente consiga trabalhar com N diferentes 
    algoritmos sem precisar alterar o seu código.
>### Chains Of Responsibility
>    O padrão Chain of Responsibility cai como uma luva quando temos uma lista de 
    comandos a serem executados de acordo com algum cenário em específico, e sabemos 
    também qual o próximo cenário que deve ser validado, caso o anterior não 
    satisfaça a condição.
>
>   Nesses casos, o Chain of Responsibility nos possibilita a separação de 
    responsabilidades em classes pequenas e enxutas, e ainda provê uma maneira flexível 
    e desacoplada de juntar esses comportamentos novamente.
>### Template Method
>    Quando temos diferentes algoritmos que possuem estruturas parecidas, o Template Method é uma 
    boa solução. Com ele, conseguimos definir, em um nível mais macro, a estrutura do algoritmo e 
    deixar "buracos", que serão implementados de maneira diferente por cada uma das 
    implementações específicas.
> 
>   Dessa forma, reutilizamos ao invés de repetirmos código, e facilitamos possíveis evoluções, 
    tanto do algoritmo em sua estrutura macro, quanto dos detalhes do algoritmo, já que cada 
    classe tem sua responsabilidade bem separada.
>### Decorator
>    Sempre que percebemos que temos comportamentos que podem ser compostos por comportamentos 
    de outras classes envolvidas em uma mesma hierarquia, como foi o caso dos impostos, 
    que podem ser compostos por outros impostos. O Decorator introduz a flexibilidade na 
    composição desses comportamentos, bastando escolher no momento da instanciação, quais 
    instancias serão utilizadas para realizar o trabalho.
>### States
>    A principal situação que faz emergir o Design Pattern State é a necessidade 
    de implementação de uma máquina de estados. Geralmente, o controle das possíveis 
    transições são vários e complexos, fazendo com que a implementação não seja 
    simples. O State auxilia a manter o controle dos estados simples e organizados 
    através da criação de classes que representem cada estado e saiba controlar as 
    transições.
>### Builder
> Sempre que tivermos um objeto complexo de ser criado, que possui diversos atributos, ou que possui uma lógica de criação complicada, podemos esconder tudo isso em um Builder.
>
>Além de centralizar o código de criação e facilitar a manutenção, ainda facilitamos a vida das classes que precisam criar essa classe complexa, afinal a interface do Builder tende a ser mais clara e fácil de ser usada.
>### Observer
> Quando o acoplamento da nossa classe está crescendo, ou quando temos diversas ações diferentes a serem executadas após um determinado processo, podemos implementar o Observer.
>
>Ele permite que diversas ações sejam executadas de forma transparente à classe principal, reduzindo o acoplamento entre essas ações, facilitando a manutenção e evolução do código.
>### Factory
> Usamos uma fábrica quando temos que isolar o processo de criação de um objeto em um único lugar. Essa fábrica pode descobrir como criar o objeto dentro dela própria, mas geralmente ela não precisa de muitas informações para criar o objeto.
> 
> #####Qual seria a diferença entre Factory e Builder?
> 
> Ambos são padrões de projeto que visam resolver problemas de criação de objetos. O que muda de um pro outro é basicamente a semântica.
>
>Geralmente usamos um builder quando precisamos passar diversas informações para a lógica que monta o objeto. No caso da Nota Fiscal, passamos nome, itens, etc.
> ### Flyweight
> 
> É um padrão de projeto de software apropriado quando vários objetos devem ser manipulados em memória sendo que muitos deles possuem informações repetidas. Dado que o recurso de memória é limitado, é possível segregar a informação repetida em um objeto adicional que atenda as características de imutabilidade e comparabilidade (que consiga ser comparado com outro objeto para determinar se ambos carregam a mesma informação).
> 
> #####Qual a diferença de um Factory e Flyweight?
> 
> Uma Factory instancia uma classe que é importante/complexa, e seu processo de criação deve ser isolado.
>
>Um Flyweight serve para quando temos muitas instâncias do mesmo objeto andando pelo sistema, e precisamos economizar. Para tal, o Flyweight faz uso de uma fábrica modificada, que guarda essas instâncias.
> 
> #####Qual a diferença de um Singleton e Flyweight?
> 
> A ideia de ambos é garantir que existam apenas uma única referência para o objeto ao longo do programa.
> 
>A diferença é que o Flyweight garante que existam apenas uma única instância de vários elementos. É um "singleton maior".
> 
> ### Memento
> 
>É um padrão de projeto de software documentado no Catálogo Gang of Four, sendo considerado como um padrão comportamental. Ele permite armazenar o estado interno de um objeto em um determinando momento, para que seja possível retorná-lo a este estado, sem que isso cause problemas com o encapsulamento.
>
>Ele funciona de maneira que uma classe é responsável por salvar o estado do objeto desejado enquanto que uma outra classe fica responsável por armazenar todas essas copias (mementos).
>
>O padrão Memento é implementado se utilizando de três elementos: Originador, Armazenador e o Memento.