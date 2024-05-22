# Curso: Teste Unitário

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
