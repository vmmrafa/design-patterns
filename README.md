# Padrões utilizados em projetos

### Strategy
    - Você cria um interface e as classes que irão implementar os métodos
    
### Chains Of Responsibility
    - Bem utilizado para lista de comandos, você tem um interface com um método
    para sempre chamar o próxima classes que irá executar o mesmo método porem regras
    diferentes.
    
### Template Method
    - Você monta um modelo de metodos para as classes filhas faça a implementação deles 
    colocando a condição de cada.

### Decorator
    - Você consegue compor diferentes ações para o mesma ação. Por exemplo,
    impostos compostos.Veja a classe TesteDeImpostosComplexos.java.

### States
    - A principal situação que faz emergir o Design Pattern State é a necessidade 
    de implementação de uma máquina de estados. Geralmente, o controle das possíveis 
    transições são vários e complexos, fazendo com que a implementação não seja 
    simples. O State auxilia a manter o controle dos estados simples e organizados 
    através da criação de classes que representem cada estado e saiba controlar as 
    transições.