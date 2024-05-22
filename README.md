# Curso: Teste Unitário

## Assert
Na estrutura de construção dos testes com o XUnit, utilizamos o Assert para verificar se as condições esperadas são verdadeiras durante a execução de um teste. O objetivo do Assert é garantir que o comportamento do código testado esteja de acordo com o que é esperado, trazendo retorno imediato.

O Assert possui vários métodos que nos auxiliam a fazer essas verificações e que utilizamos de acordo com a nossa necessidade de verificação. Confira alguns dos mais utilizados:

Assert.Equal: Verifica se dois valores são iguais.

Assert.NotEqual: Verifica se dois valores não são iguais.

Assert.True: Verifica se uma expressão é verdadeira.

Assert.False: Verifica se uma expressão é falsa.

Assert.Null: Verifica se um valor é nulo.

Assert.NotNull: Verifica se um valor não é nulo.

Assert.Contains: Verifica se uma coleção contém um determinado elemento.

Assert.Throws: Verifica se um método lança uma exceção específica.

Assert.Empty: Verifica se uma coleção está vazia.

Assert.StartsWith: Verifica se uma string começa com determinado prefixo.

Assert.EndsWith: Verifica se uma string termina com determinado sufixo.

Você pode conferir uma breve explicação sobre cada um dos métodos do Assert no próprio VisualStudio ao digitar Assert. e passar o cursor sobre as opções que aparecerão como sugestão de completar automaticamente.

## Outras notações do XUnit

O XUnit trabalha com notações para identificar os testes que estão sendo escritos e conhecemos duas: Fact e Theory. Porém existem diversas outras notações do XUnit que podem ser utilizadas, como por exemplo:

[TestFixture] - uma classe que contém um conjunto de testes de unidade relacionados;

[Test] - utilizada para identificar testes distintos dentro de uma mesma classe de teste;

[Ignore] - utilizada para ignorar um teste específico durante a execução;

[Collection] - utilizada para agrupar testes em coleções específicas.

Existem diversas outras notações do XUnit que podem ser utilizadas de acordo com a complexidade e a necessidade de cada projeto e casos de teste. 

## Give-When-Then ajuda

O padrão Give-When-Then ajuda a estruturar os testes de maneira bem clara e compreensível seguindo uma abordagem descritiva que informa o comportamento esperado de um sistema em termos de entrada (give), ação (when) e saída (then). Nessas etapas temos:

Give: fase onde é configurado o cenário para o teste;
When: fase onde é executada a ação que se deseja testar;
Then: fase onde é verificado o resultado da ação anterior.
Os dois padrões são bem parecidos, porém possuem algumas diferenças básicas: por exemplo, o padrão AAA é mais focado na estruturação do teste em termos de organização do código e na execução do teste em si, destacando a preparação do ambiente de teste, a execução da ação e a verificação do resultado. Já o padrão Give-When-Then é mais orientado ao comportamento e coloca mais ênfase na descrição do comportamento do sistema em termos de entradas e saídas.

No final, a decisão sobre qual padrão utilizar vai sempre depender da equipe envolvida no processo e também das particularidades de cada projeto.

## TDD ("Test-Driven Development")
Tdd, ou "Test-Driven Development" (em português, Desenvolvimento Orientado a Testes), é uma abordagem de desenvolvimento de software que enfatiza a criação de testes automatizados antes da implementação do código de produção. O processo TDD segue um ciclo iterativo e incremental, composto por três etapas principais: Red, Green, e Refactor.

- Red (Vermelho): Nesta fase, você escreve um teste automatizado que captura uma pequena parte do comportamento desejado do sistema. No entanto, o código de produção ainda não foi implementado, então o teste deve falhar (ficar "vermelho").

- Green (Verde): Agora, o objetivo é fazer com que o teste escrito na fase anterior passe. Você implementa apenas o código necessário para que o teste automatizado tenha êxito. O foco é escrever o código mínimo necessário para atender aos requisitos do teste.

- Refactor (Refatorar): Com o teste passando, você pode refatorar o código para melhorar sua qualidade, eficiência e legibilidade. O objetivo é garantir que o código continue atendendo aos requisitos, mas agora de uma maneira mais clara e eficiente.

O ciclo Red-Green-Refactor é repetido várias vezes ao longo do desenvolvimento do software. Cada iteração adiciona pequenos incrementos de funcionalidade ao sistema (conhecidos como baby steps) e garante que as alterações não quebrem o que já foi implementado. Isso ajuda a manter o código sempre em um estado funcional e facilita a detecção rápida de erros.

Para demonstrar esse processo, confira a figura a seguir:

![image](https://github.com/Arthur-Sena/Curso-TesteUnitario/assets/57300757/d0233a91-0515-496c-8d94-b76ce19bb939)

alt text: A imagem é um fluxograma com o título TDD (Test Driven Development). Abaixo, há o subtítulo “Nova funcionalidade”, que apresenta um fluxograma. Na etapa 1, “Escrever testes”, há um círculo vermelho com o “X”, com a descrição “Etapa vermelha: Testes falhando”. Há uma seta apontando para a direita, onde há um círculo em verde, na etapa 2, com o símbolo de “check”, e a descrição “Escrever  o código mínimo”. Na terceira e última etapa, há um círculo na cor lilás com a descrição “Refatorar o código”.

Aplicando o TDD ao projeto, conseguimos:

- Feedback rápido: Os testes automatizados fornecem feedback instantâneo sobre a funcionalidade implementada.
- Código mais seguro e robusto: Como cada alteração é validada por testes automatizados, o risco de introdução de erros é reduzido.
- Documentação viva: Os testes automatizados servem como documentação atualizada e viva do comportamento do sistema.
- Facilita a refatoração: A abordagem de refatoração contínua ajuda a melhorar a qualidade do código ao longo do tempo.

O TDD é amplamente utilizado em metodologias ágeis e é considerado uma prática importante para garantir a qualidade do software. Para saber mais sobre TDD e sua aplicação em projeto .NET, você pode acessar este artigo na documentação da Microsoft.

## Cobertura de testes

A cobertura de testes é uma medida usada para avaliar a eficácia dos testes em um código-fonte. Refere-se à porcentagem de código que é executada durante a execução de um conjunto de testes automatizados. A cobertura de testes é essencial para garantir a qualidade do código e a estabilidade do produto final.

A cobertura de testes em .NET fornece uma métrica objetiva para avaliar a qualidade dos testes de um projeto. Isso ajuda as equipes de desenvolvimento a identificar áreas do código que não estão sendo devidamente testadas e aprimorar seus conjuntos de testes para alcançar uma cobertura mais abrangente.

### Testes de mutação

Testes de mutação são uma técnica avançada de teste de software que visa avaliar a eficácia dos testes de unidade identificando lacunas na cobertura do código. Os testes de mutação são particularmente úteis para garantir que os testes não apenas verifiquem a implementação atual do código, mas também sejam robustos o suficiente para detectar mudanças semânticas significativas que possam introduzir bugs.

Os testes de mutação seguem o seguinte fluxo ao serem aplicados:

- Introdução de mutações: Um processo automatizado é usado para introduzir pequenas alterações no código-fonte, conhecidas como mutações.

- Execução dos testes: Depois que as mutações são introduzidas no código-fonte, os testes de unidade existentes são executados novamente. Se um teste de unidade falhar após a introdução de uma mutação, isso indica que o teste conseguiu detectar a mudança no comportamento do código.

- Análise dos resultados: Os resultados dos testes de mutação são analisados para determinar a eficácia dos testes existentes. Se um grande número de mutações não são detectadas pelos testes, isso sugere que há lacunas na cobertura de teste e que os testes podem não ser robustos o suficiente para detectar todas as variações no comportamento do código.

- Refinamento dos testes: Com base nos resultados da análise, as pessoas desenvolvedoras podem refinar os testes de unidade existentes ou adicionar novos testes para melhorar a cobertura e garantir que o código seja mais robusto contra alterações.

Os testes de mutação são particularmente úteis em linguagens como C# devido à sua forte tipagem estática e às características do compilador que podem ocultar certos tipos de erros durante a compilação. Ao introduzir mutações no código-fonte e verificar se os testes conseguem detectá-las, as pessoas desenvolvedoras podem aumentar a confiança na qualidade e na robustez do código.

## Biblioteca Bogus

Bogus é uma biblioteca popular no ecossistema .NET, especialmente útil no contexto de testes de unidade. Ela é projetada para gerar dados falsos de maneira fácil e conveniente, ajudando a criar cenários de teste realistas e complexos.

Alguns dos recursos que essa biblioteca nos oferece, são:

- Geração de Dados Aleatórios: Bogus fornece uma variedade de geradores para criar dados falsos, incluindo nomes, endereços, números de telefone, e-mails, números de cartão de crédito, entre outros. Isso permite simular uma ampla gama de situações de teste com facilidade.
- Configuração Flexível: Você pode personalizar os dados gerados de acordo com suas necessidades. A biblioteca oferece muitas opções de configuração para controlar o formato e o tipo de dados gerados, permitindo que você crie conjuntos de dados específicos para seus testes.
- Suporte a Internacionalização: Bogus suporta geração de dados em vários idiomas e formatos. Isso é útil para testar aplicativos que têm requisitos de localização e internacionalização.
- Integração com Frameworks de Teste: A biblioteca é facilmente integrada com frameworks de teste populares, como o xUnit. Isso simplifica a incorporação de dados falsos em seus casos de teste existentes.

A utilização de dados falsos gerados pelo Bogus pode melhorar a cobertura de teste e a robustez de seus testes de unidade, permitindo simular uma variedade de cenários que podem ser difíceis de alcançar com dados reais. Isso ajuda a garantir que seu código seja testado de forma abrangente e confiável.

## Boas práticas

Aplicar boas práticas em testes de unidade é crucial para garantir a qualidade e a robustez do software desenvolvido. Os testes de unidade desempenham um papel fundamental no ciclo de desenvolvimento de software, pois permitem aos desenvolvedores verificar se cada componente individual do código funciona conforme o esperado.

Em .NET, as boas práticas em testes de unidade envolvem diversos aspectos, desde a organização e estruturação dos testes até a escolha das técnicas e ferramentas adequadas. Durante este curso aplicamos algumas dessas boas práticas, como:

- Organização e Estruturação: É essencial organizar os testes de forma clara e coesa. Uma estrutura bem organizada facilita a manutenção e a compreensão dos testes, além de tornar mais fácil localizar e corrigir possíveis falhas.
- Testes Independentes e Isolados: Cada teste deve ser independente e isolado, ou seja, não deve depender do resultado de outros testes para ser executado corretamente. Isso garante que os testes possam ser executados em qualquer ordem e que as falhas possam ser identificadas e corrigidas de forma precisa.
- Test-Driven Development (TDD): Essa prática promove a escrita de código mais limpo, modular e testável, além de garantir uma cobertura de teste mais abrangente desde o início do desenvolvimento.
- Cobertura de Código: A cobertura de código ajuda a identificar áreas do código que não estão sendo testadas adequadamente, permitindo que os desenvolvedores priorizem esforços para melhorar a qualidade do teste.
- Automação dos Testes: Isso garante que os testes sejam executados regularmente e de forma consistente, ajudando a identificar regressões e problemas de forma rápida e eficiente.

Além dessas boas práticas que aplicamos durante este curso existem outras que também são super importantes para o desenvolvimento de softwares com maior qualidade e segurança.
