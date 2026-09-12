Curso Treinamento C# Avançado no nextwave(LuisDEV)

### Estruturas de C#, POO avançado
 - Sobre o Treinamento C# Avançado
   - O Treinamento C# Avançado é um treinamento para quem deseja se tornar referência técnica na linguagem, estando pronto para responder perguntas em entrevistas técnicas e aplicando conceitos em seus projetos
   - Conteúdos
     - Estruturas do C#
     - OOP avançada
     - Delegates e Events
     - Async-Await e Multithreading
 - Estruturas de C#
   - Além dos tipos mais básicos da linguagem, existem alguns que em maior ou menos grau vamos vir a utilizar, mas que exigem maior compreensão de suas características
   - Entender isso é primordial para nos destacarmos como profissionais, afinal, o conhecimento nos ajuda tanto em nossos projetos quando em entrevistas
   - As estruturas tratadas neste treinamento são
     - Enumerações
     - Struct
     - Record
     - Tuplas
- Enumerações
  - Permite a definição de constantes nomeadas, fortemente tipadas
  - Entre os seus principais benefícios estão
    - Legibilidade de código: permite a definição de nomes claros para valores constantes, tornando o seu código mais legível e auto-explicativo, ao contrário do uso de strings ou números mágicos
    - Segurança em Tipagem: garante que apenas valores válidos de enums são atribuídos, permitindo detectar erros em tempo de compilação ao invés de execução
    - Suporte ao Intellisense: facilidade de utilização do enum com a ajuda do Intellisense
    - Facilidade de Refatoração: permite atualização do valor em apenas um lugar e será atualizado em todos seus usos
 - Permite a definição de constantes nomeadas, fortemente tipadas
 - Entre as suas principais limitações estão
   - Formatação em String: necessidade de utilizar atributos para definir formatação de um valor de enum para string
   - Limitação de valores: como são baseados em inteiros, tem uma quantidade limitada de valores únicos a serem utilizados
   - Compatibilidade com bancos de dados: apesar de que algumas ferramentas ORM resolvam esse problema, algumas exigem configuração adicional. Além disso, eles podem não mapear de forma correta caso não utilize uma ORM, dependendo do uso.

- Struct
  - Structs, ao contrário de classes, são de tipo de valor em C#
  - Entre os seus principais benefícios estão
    - Performance: eles são armazenados na stack, e tem uma sobrecarga menor na memória quando comparados com classes, que são alocadas na Heap, resultando em melhor performance em cenários onde temos várias instâncias criadas e destruídas rapidamente
    - Não Nulas: elas não podem ser nulas, então evitamos problemas de referência nulo que podem ocorrer com classes
    - Semântica de Valor: struct são copiados por valor, evitando problemas causados por alterações de instâncias/referências
    - Sobrecarga na Performance: apesar de structs oferecerem benefícios de performance em certos cenários, eles podem ter problemas de performance, como:
      - Comportamento de Cópia: como eles são copiados por valor, caso você passe um struct como parâmetro ou atribua a uma nova variável será feita uma cópia completa dele. Nesses cenários, pode apresentar problemas de formance, especialmente para structs grandes
      - A Microsoft indica um struct a ter no máximo 16 bytes
    - Sobrecarga na Memória: em alguns cenários, a sobrecarga na memória pode superar os benefícios do armazenamento na stack
      - Alocação na Stack vs Heap: a stack tem um tamanho limitado,logo, se o struct for muito grande, poderá resultar em problemas de overflow
        - A cópia de struct grandes resultam na cópia de muitos campos, aumentando o consumo de memória

- Record
  - Records são um tipo de referência, que oferece uma maneira simplificada de criar classes imutáveis
  - Entre os seus principais benefícios estão
    - Sintaxe Concisa: introduzem uma sintaxe mais concisa para a criação de classes de dados imutáveis. É possível definir uma record com menos código, reduzindo a verbosidade
    - Semântica Imutável Padrão: elas são imutáveis por padrão. Isso significa que seus valores não podem ser modificados após a criação, evitando erros comuns relacionados a mutabilidade
    - Métodos de Igualdade e Comparação Automatizados: As records geram automaticamente os métodos Equals, GetHashCode e ToString, o que simplifica a comparação e a utilização em coleções, sem a necessidade de implementação manual.
    - Desempenho: usar records para todas as classes de dados pode não ser apropriado em todas as situações. Para classes de dados pequenas e frequentemente mutáveis, a criação de records pode ser excessiva
    - Compatibilidade com Padrões Existentes: introduzir records em um código existente pode exigir ajustes em partes do código que lidam com igualdade e comparação personalizada
    - Decisão de uso: records são imutáveis por padrão, o que pode ser um desafio se você precisar de uma classe mutável. Você terá que recorrer ao uso de classes normais em tais casos, decidindo caso a caso

- Tuplas
  - Tuplas são uma estrutura de dados que permite agrupar um conjunto ordenado e heterogêneo de elementos em uma única unidade.
  - Entre os seus principais benefícios estão
    - Praticidade: são convenientes para agrupar valores relacionados sem a necessidade de criar estruturas complexas.
    - Performance: em muitos casos, as tuplas podem ser mais eficientes em termos de memória e desempenho do que criar classes ou mesmo structs
    - Código mais limpo: ajudam a simplificar o código ao eliminar a necessidade de criar classes ou structs simples apenas para agrupar valores.
    - Retorno Múltiplo: permitem retornar vários valores de um método ou função sem a necessidade de criar tipos personalizados.
    - Semântica limitada: as tuplas não têm semântica rica como classes ou structs, o que pode dificultar a compreensão do código em cenários mais complexos. Se não tiver retorno nomeado, torna o código de difícil manutenção
      - É importante entender a questão a ordem de elementos, principalmente na desestruturação de Tuplas

- Herança e Polimorfismo
  - A herança e o polimorfismo são conceitos fundamentais na programação orientada a objetos, incluindo a linguagem C#
  - Apesar de serem considerados básicos, são conceitos que quando compreendidos a fundo, permitem o seu uso em níveis altos de programação
  - Esses conceitos permitem criar hierarquias de classes e a capacidade de tratar objetos de diferentes classes de maneira uniforme
  - Os principais benefícios de Herança
    - Reutilização de código: permite que classes herdem membros e métodos de outras classes, evitando a duplicação de código e promovendo a reutilização
    - Hierarquia de classes: permite criar uma hierarquia de classes, onde classes mais específicas podem herdar comportamentos e propriedades de classes mais gerais. Isso ajuda a modelar o domínio de maneira mais eficaz
    - Polimorfismo: é a base para o polimorfismo, que permite que objetos de classes derivadas sejam tratados como objetos da classe base, facilitando o desenvolvimento de código genérico e flexível.
  - Os principais desafios de Herança
    - Acoplamento Forte: pode levar a um acoplamento forte entre classes, o que pode dificultar a manutenção e a evolução do código. Mudanças na classe base podem afetar as classes derivadas
    - Hierarquias Complexas: à medida que a hierarquia de classes cresce, pode se tornar complexo entender e manter a relação entre as classes. Isso pode levar a estruturas de herança confusas e difíceis de gerenciar
    - Herança Múltipla Limitada: C# não suporta herança múltipla de classes, o que pode ser um desafio quando há a necessidade de herdar comportamentos de várias classes.
  - Os principais benefícios de Polimorfismo
    - Flexibilidade: permite que um objeto de uma classe derivada seja tratado como um objeto da classe base, proporcionando flexibilidade na manipulação de objetos diferentes de maneira uniforme.
      - Alguns padrões de projeto são fortemente associados com esse benefício, como Strategy e Factory Method
    - Código Genérico: permite escrever código genérico que pode trabalhar com objetos de várias classes derivadas, o que aumenta a eficiência e a reutilização
    - Extensibilidade: O polimorfismo facilita a extensão do comportamento das classes derivadas sem afetar o código existente que lida com objetos da classe base
  - Os principais desafios de Polimorfismo
    - Complexidade: pode tornar o código mais complexo, pois os detalhes específicos das classes derivadas podem não ser evidentes no código que manipula objetos da classe base
    - Desempenho: em alguns casos, a resolução dinâmica de métodos associados ao polimorfismo pode introduzir uma sobrecarga de desempenho em comparação com chamadas de métodos diretos
    - Entendimento: em situações complexas, pode ser desafiador entender como um método específico será executado e qual será o comportamento real

- Composição
  - A composição envolve criar classes que contêm objetos de outras classes como membros internos. Em vez de herdar comportamento, uma classe se relaciona com outras classes através de composição, delegando responsabilidades para os objetos que contém
  - Os principais benefícios da Composição
    - Flexibilidade: permite combinar diferentes objetos para criar novos comportamentos sem herança direta.
    - Baixo Acoplamento: as classes são menos acopladas, facilitando a substituição de componentes e a manutenção
    - Módulos Reutilizáveis: Os objetos podem ser criados e reutilizados independentemente em várias partes do código
  - Os principais desafios de Composição
    - Gerenciamento: é necessário gerenciar a criação, destruição e vida útil dos objetos compostos.
    - Maior Complexidade: em algumas situações, a composição pode levar a um código mais complexo, com muitos objetos interdependentes
      - Sabe aquela situação onde uma classe tem vários objetos sendo recebidos via injeção de dependência? Estamos falando disso!

- Interfaces e Classes Abstratas
  - As interfaces definem contratos que as classes que a implementam devem seguir, especificando métodos e propriedades que devem ser fornecidos
  - Entre os seus principais benefícios estão
    - Contratos Claros: definem contratos bem definidos que as classes devem cumprir, promovendo a consistência no código
    - Múltiplas Implementações: uma classe pode implementar várias interfaces, permitindo que ela cumpra múltiplos contratos
    - Desacoplamento: promovem baixo acoplamento, permitindo que as classes se comuniquem sem conhecer os detalhes internos umas das outras
    - Testabilidade: facilitam a criação de testes de unidade, pois as dependências podem ser substituídas por implementações de interface mock
  - Entre as suas principais limitações estão
    - Código Repetitivo: implementar uma interface em várias classes pode levar a código repetitivo se os métodos são semelhantes, levando a uma análise se vale a pena utilizar uma classe abstrata nesse cenários
    - Mudanças na Interface: mudanças podem afetar várias classes que a implementam, exigindo ajustes em várias partes do código
    - Complexidade Adicional: em projetos pequenos e com tempo de vida curto, interfaces podem adicionar complexidade desnecessária.
  - As classes abstratas fornecem uma base para outras classes, mas não podem ser instanciadas diretamente. Elas podem conter métodos abstratos (sem implementação) que devem ser implementados pelas classes derivadas
  - Entre os seus principais benefícios estão
    - Compartilhamento de Código: podem fornecer implementações comuns de métodos que podem ser compartilhados por várias subclasses
    - Definição de Estrutura: podem definir uma estrutura básica para classes derivadas seguirem
    - Métodos Abstratos: podem conter métodos abstratos que as subclasses devem implementar, garantindo a conformidade com a estrutura da classe base
  - Entre as suas principais limitações estão
    - Restrições de Herança: as subclasses só podem herdar de uma classe abstrata, limitando a flexibilidade em comparação com interfaces
    - Acoplamento com a Hierarquia de Classes: modificar a classe abstrata pode afetar todas as subclasses, o que pode levar a um alto grau de acoplamento

- Generics
  - Os generics são um recurso do C# que permitem criar classes, interfaces e métodos que funcionam com tipos de dados específicos, sem comprometer a segurança de tipos
  - Entre os seus principais benefícios estão
    - Reutilização de Código: permitem criar código reutilizável que funciona com diversos tipos de dados, eliminando a necessidade de duplicar código para diferentes tipos
    - Segurança na Tipagem: mantêm a segurança de tipos em tempo de compilação, evitando erros de tipo em tempo de execução e aumentando a confiabilidade do código
    - Performance: podem melhorar o desempenho, pois evitam a necessidade de conversões de tipo desnecessárias
    - Flexibilidade: classes genéricas podem ser usadas com uma ampla variedade de tipos de dados, proporcionando uma maior flexibilidade na criação de estruturas de dados e algoritmos
  - Entre as suas principais limitações estão
    - Complexidade: o uso incorreto de genéricos pode levar a código mais complexo e difícil de entender, especialmente quando há uma variedade de tipos envolvidos
      - Infelizmente é comum encontrar projetos que buscam a todo custo generalizar tudo, mesmo em cenários não compatíveis. Isso resulta em código de difícil manutenção, cheio de condicionais
      - Eu chamo isso carinhosamente de "Código Megazord"
    - Restrições: algumas operações podem ser restritas por limitações de tipo ou restrições genéricas, o que pode exigir soluções alternativas ou abordagens diferentes
    - Curva de Aprendizado: entender e aplicar corretamente generics pode exigir um certo nível de conhecimento e experiência, especialmente ao lidar com cenários avançados

- Delegates
  - Delegates são tipos de referência que permitem que você encapsule e passe métodos como parâmetros para outros métodos. Um delegate possui uma assinatura que corresponde à assinatura do método que ele pode referenciar, permitindo que você chame diferentes métodos usando o mesmo delegate
  - Entre os seus principais benefícios estão
    - Reutilização de Código: permitem a reutilização de código, pois você pode passar o mesmo delegate para vários métodos, evitando a duplicação de lógica
    - Flexibilidade: proporcionam flexibilidade ao permitir que diferentes métodos sejam vinculados a um mesmo delegate. Isso permite a substituição de implementações sem alterar o código existente
    - Eventos Personalizados: são a base para a criação de eventos personalizados, permitindo que objetos comuniquem mudanças e interações entre si
    - Separação de Responsabilidades: usar delegates para callback separa a lógica de chamada de métodos da lógica de implementação
  - Entre os seus principais desafios estão
    - Dificuldade de Entendimento: podem tornar o código mais complexo, especialmente quando usados de forma extensiva, o que pode dificultar a compreensão para desenvolvedores menos experientes
    - Depuração: a depuração de problemas relacionados a delegates pode ser desafiadora, uma vez que eles podem apontar para métodos diferentes em diferentes momentos da execução
    - Segurança: podem permitir a chamada de métodos não autorizados, caso não sejam usados com cuidado

- Func, Action, e Predicate
  - São delegates pré-definidos em C#
  - Func
    - Define uma assinatura de método que retorne um valor



