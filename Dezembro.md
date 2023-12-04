No mês de dezembro houve a consolidação do que foi feito em agosto, com um merge do código de ethernet e procura de bugs no código do Android, também houve o começo de um driver de wifi.


Finalmente, após conseguirmos em comunidade testar em todas as variantes de hardware possíveis, o patch sob o commit dos drivers realtek em agosto foi amalgamado ao código nascente.

Isso demorou tempo devido a procura por pessoas que tem outras variantes do hardware que seria testado, mas eventualmente conseguimos a maioria delas e todo mundo está confiante com a mudança:

http://git.9front.org/plan9front/plan9front/0231537cbac846087f5ac132aba5c97ec9d4cffa/commit.html

Sobre o programa de conexão remota de Android ainda existem muitos problemas com o código, tanto com o original quanto com minhas modificações, mas alguma das novas APIs do Android podem futuramente solucionar uma parte desses problemas, em reunião no primeiro sabado de dezembro discutimos o que poderia ser feito ainda antes de modificar qualquer outro código.

Comecei com o conceito do driver de wifi, ainda tenho só um código esqueleto que não faz nada além de copiar o firmware para a memoria e escrever em alguns registradores PCI Express, quero fazer um parser do firmware do controlador Wireless mas creio que isso está muito longe, nenhum aspecto lógico do hardware/firmware é documentado e a Intel não parece estar disposta a divulgar essa informação facilmente para universitários ou clientes que não assinaram um _non disclosure agreement_


Eventualmente sei que vou olhar o código do OpenBSD nesse caso do wifi pois a maioria dos nossos outros drivers de WiFi são inspirados diretamente de lá, mas ainda falta uma semana de _boilerplate_ para começar com isso.
