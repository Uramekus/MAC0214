Devido a Greve, o mês de outubro foi bem curto e ao mesmo tempo bem mais longo!


Aproveitei parte do tempo da greve pra ler os manuais de video da intel em https://www.intel.com/content/www/us/en/docs/graphics-for-linux/developer-reference/1-0/overview.html.
Porém acabei o fazendo com bem menos pressão de tempo visto as incertezas que estavam sob a permanencia da greve e sequer se o semestre ainda iria existir ou ser cancelado no final de tudo.
Ao mesmo tempo, esse tipo de leitura tecnica e densa acaba realmente pedindo um maior tempo de digestão e de testes manuais, pois existe um gap enorme entre o que há documentado e o que deve ser feito, e isso demanda iterar e entender a logica do que está escrito

Visto que não planejo copiar codigo do Linux, não posso simplesmente consultar o funcionamento do código lá toda hora quando há duvidas sob o que fazer no manual, mas porém tenho como objetivo aproveitar da emulação de gpu com time sharing que a intel implementou no kernel linux 
e com isso veio o desafio de entender especificamente como funciona essa parte do código devido a um bug da emulação ![](kmesg.png)


Com isso entendi que a maquina de estados criada pelo kernel do gvt-g tem um bug, mas é quando a sequencia feita é de forma inesperada/não suportada pela intel, mandei um email a um conhecido do time da intel e estou esperando respostas a respeito.

# Mudanças no Driver

Agora, da parte do driver em si o que acabou me assustando muito é o quanto mudou e o quanto acabou ficando parecido ao que esixtia antigmaente mas mudou em detalhas de uma forma que acaba mais atrapalhando que ajudando, tinha uma noção muito primitiva do que realmente seria necessário para fazer o hardware funcionar pois o documento da Intel dava passos "simples" que estavam todos sendo feitos, mas existiam problemas nos detalhes de cada um dos passos que o impedia de funcionar de um jeito esperado, resultando sempre em uma tela preta


