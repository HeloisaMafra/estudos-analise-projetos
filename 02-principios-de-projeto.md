# 2. Princípios de Projeto de Software

## 2.1 O que são princípios de projeto?

Princípios de projeto de software são orientações que ajudam a organizar a estrutura interna de um sistema. O objetivo é tornar o software mais compreensível, testável, extensível e fácil de manter.

Um bom projeto não depende apenas de funcionar hoje: também deve facilitar correções e mudanças futuras.

## 2.2 Modularidade

A **modularidade** consiste em dividir um sistema em partes menores, com responsabilidades definidas. Cada módulo concentra uma parte do problema e se relaciona com os demais por interfaces ou contratos claros.

**Exemplo:** em um sistema de delivery, podem existir módulos para cadastro de clientes, cardápio, pedidos e pagamentos.

**Benefício:** uma alteração no cardápio pode ser feita sem exigir mudanças desnecessárias em todo o sistema.

## 2.3 Coesão

A **coesão** indica o quanto as responsabilidades de um módulo estão relacionadas entre si. Em geral, busca-se alta coesão: um módulo deve ter um propósito claro e bem delimitado.

**Exemplo:** um módulo de autenticação deve concentrar responsabilidades relacionadas à entrada e à verificação da identidade dos usuários, em vez de também calcular frete e gerar relatórios financeiros.

## 2.4 Acoplamento

O **acoplamento** representa o grau de dependência entre módulos. Em geral, busca-se baixo acoplamento, para que mudanças em um módulo provoquem o mínimo possível de alterações nos demais.

**Exemplo:** se a tela de pedidos depende diretamente de muitos detalhes internos do módulo de pagamento, mudar o pagamento pode exigir alterações na tela. Uma interface bem definida ajuda a reduzir essa dependência.

**Atenção:** baixo acoplamento não significa ausência total de dependências; significa que elas são controladas e bem definidas.

## 2.5 Abstração e encapsulamento

**Abstração** é destacar as características relevantes de algo e deixar detalhes desnecessários em segundo plano.

**Encapsulamento** é agrupar dados e comportamentos e controlar como o estado interno de um objeto pode ser acessado ou alterado.

Esses conceitos ajudam a reduzir a complexidade e a proteger as regras internas do sistema.

## 2.6 Separação de responsabilidades

Cada parte do sistema deve ter responsabilidades claras. Misturar interface, regras de negócio e acesso a dados em um único bloco pode tornar o código difícil de testar e manter.

**Exemplo:** em uma aplicação web, a interface apresenta os dados, a lógica de negócio aplica as regras e a camada de persistência conversa com o banco de dados. Essa separação pode variar conforme a arquitetura escolhida.

## 2.7 Simplicidade e manutenção

Um projeto deve resolver o problema real sem complexidade desnecessária. Soluções simples tendem a ser mais fáceis de compreender, testar e modificar.

Isso não significa ignorar requisitos importantes, mas evitar funcionalidades e abstrações que não trazem benefício claro.

## 2.8 Variáveis globais e modularidade

O uso excessivo de variáveis globais pode dificultar o isolamento dos módulos, porque diferentes partes do programa podem ler ou alterar o mesmo estado. Isso aumenta as dependências e pode tornar os erros mais difíceis de localizar.

Quando possível, prefira passar os dados necessários por parâmetros e manter o estado próximo da parte responsável por ele.

## 2.9 Resumo

Entre os princípios importantes estão modularidade, alta coesão, baixo acoplamento, abstração, encapsulamento, separação de responsabilidades e simplicidade. Eles contribuem para sistemas mais organizados e fáceis de evoluir.

## Perguntas para revisão

1. Qual é a diferença entre coesão e acoplamento?
2. Por que dividir um sistema em módulos pode facilitar a manutenção?
3. Como o excesso de variáveis globais pode prejudicar um projeto?
4. Qual é a diferença entre abstração e encapsulamento?
