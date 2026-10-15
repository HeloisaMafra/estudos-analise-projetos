# 3. Casos de Uso

## 3.1 O que é um caso de uso?

Um **caso de uso** descreve uma funcionalidade ou um objetivo que um ator pode realizar utilizando um sistema. Ele ajuda a registrar o comportamento esperado do sistema do ponto de vista de quem interage com ele.

Casos de uso podem ser representados em diagramas UML e também descritos em texto, com etapas e condições.

## 3.2 Ator

Um **ator** representa um papel externo que interage com o sistema. Pode ser uma pessoa, outro sistema ou um dispositivo.

O ator representa um papel, não necessariamente uma pessoa específica.

**Exemplos em um sistema de biblioteca:**
- Leitor
- Bibliotecário
- Sistema externo de notificações

## 3.3 Caso de uso

O caso de uso representa um objetivo, como:
- Consultar catálogo
- Reservar livro
- Registrar empréstimo
- Devolver livro

O nome costuma começar com um verbo para indicar a ação ou o objetivo.

## 3.4 Limite do sistema

No diagrama, o limite do sistema é normalmente representado por um retângulo que contém os casos de uso. Os atores ficam fora dele. Essa divisão ajuda a distinguir as funcionalidades internas do sistema dos papéis externos que interagem com ele.

## 3.5 Relacionamentos

### Associação

Uma linha entre um ator e um caso de uso indica que o ator participa daquela funcionalidade.

### `<<include>>`

Indica que um caso de uso inclui obrigatoriamente o comportamento de outro caso de uso como parte de seu fluxo.

**Exemplo ilustrativo:** “Finalizar pedido” inclui “Calcular total”, quando esse cálculo é sempre necessário para concluir o pedido.

### `<<extend>>`

Indica um comportamento adicional que pode ser inserido em outro caso de uso sob determinadas condições. O caso de uso base pode ser compreendido sem a extensão.

**Exemplo ilustrativo:** “Aplicar cupom promocional” pode estender “Finalizar pedido” quando o cliente escolhe usar um cupom.

A escolha entre `include` e `extend` depende do comportamento real do sistema, não apenas de evitar repetição no desenho.

## 3.6 Exemplo de descrição textual

**Caso de uso:** Reservar livro

**Ator principal:** Leitor

**Pré-condição:** O leitor está identificado no sistema.

**Fluxo principal:**
1. O leitor pesquisa o catálogo.
2. O sistema apresenta os livros encontrados.
3. O leitor seleciona um livro disponível para reserva.
4. O sistema registra a solicitação.
5. O sistema confirma a reserva.

**Fluxo alternativo:** Se o livro não puder ser reservado, o sistema informa a indisponibilidade e apresenta as opções possíveis.

**Pós-condição:** A reserva fica registrada, se a operação for concluída com sucesso.

## 3.7 Benefícios e limites

Casos de uso ajudam a:
- identificar funcionalidades a partir dos objetivos dos atores;
- conversar com usuários e responsáveis pelo sistema;
- delimitar o escopo;
- apoiar a elaboração de testes de aceitação.

Por outro lado, um diagrama de casos de uso não descreve todos os detalhes internos, a estrutura das classes ou a sequência técnica completa do programa. Para isso, outros modelos e documentos podem ser necessários.

## 3.8 Resumo

Casos de uso descrevem como atores externos interagem com um sistema para alcançar objetivos. Eles ajudam a organizar requisitos funcionais e a comunicar o escopo da solução.

## Perguntas para revisão

1. O que é um ator?
2. Qual é a função do limite do sistema?
3. Qual é a diferença entre `include` e `extend`?
4. Por que um caso de uso pode ter fluxos alternativos?
