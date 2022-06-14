# O que é blockchain?

<img src="https://i.imgur.com/Pn1B0t8.png" />

Um blockchain é um banco de dados compartilhado, distribuído e permanente compartilhado entre vários nodes (nós) em uma rede de computadores. Eles registram dados de uma maneira que torna probabilistamente impossível modificar ou hackear o sistema.

Especificamente, blockchain registra dados como uma cadeia de blocos. Cada bloco contém um grupo de transações, que podem estar transferindo ativos pela rede, ou atualizando informações salvas na blockchain.

Blockchains foram popularizados por uma pessoa anônima (ou grupo) Satoshi Nakamoto, quando eles lançaram a Bitcoin Network em 2008. Bitcoin é uma rede de criptomoedas, e lida principalmente com transferência de ativos BTC em toda rede, sem intermediário confiável ou uma autoridade. enquanto garante que a própria rede é segura por si só, e não pode ser hackeada. (Obs: A rede bitcoin é também tem a maior recompensa de bugs do mundo, se você puder hacker, você será trilhonários).

Com tempo, o design do Bitcoin inspirou outras, mais capazes, redes blockchains aparecerem, como a Ethereum, Nos vamos aprender bastante sobre Ethereum nas próximas sessões.

# Gerênciamento de estados.

<img src="https://i.imgur.com/VQySjQu.png" />

Então, uma blockchain começa como um estado de Genesis (Gênesis) quando elas são lançadas. A gênesis da Bitcoin ocorreu em 2009 quando a rede pública foi lançada. A gênesis da Ethereum aconteceu em 2015, quando foi lançada.

Toda transação em uma blockchain modifica o estado global que é replicada para todos os nodes (nós).

Como existem milhares de transações, elas são agrupadas em blocos, daí o nome. Esses blocos são encadeados de maneira verificável criptograficamente para que sejam historicamente rastreáveis. O estado atual de uma rede pode ser recalculado a qualquer momento partindo do block gênese e fazendo a transição do estado de acordo com as informações de cada block até o momento.

# Nodes (nós)

Uma rede blockchain é gerenciada de forma autônoma por meio de uma rede destribuída ponta-ponta (peer-to-peer) de nós de computador. Sem entrar em muitos detalhes, você pode simplesmente pensar em que cada node em uma rede mantém uma cópia do livro de transações global. Portanto, cada node pode ser um verificador individual e auditar transações que acontecem na rede e garantir que não houve comportamento ilícito. Outro tipo de node, chamado `mining node`, é responsável por agrupar novas transações sendo feitas em uma rede em um bloco, e propondo que o bloco seja incluído no livro-razão (bloco geral) global por todos os demais. Mineração é computacionalmente dificil, e muito importante fazer de forma segura, então os minerados cujos blocos são aceitos recebem um token por seu "trabalho duro".

O uso de uma blockchain confirma que cada unidade de valor foi transferida apenas uma vez, e os mecanismos engenhosos apresentados por Satoshi Nakamoto resolveram o problema de longa data de gastos duplos descentralizados.

# Decentralização

Ao armazenar dados em uma rede ponta a ponta de nodes, o blockchain é uma rede descentralizada. Isso traz benefícios significativos em relação a abordagem tradicional de armazenamento de dados de maneira centralizada. Existem exemplos significativos de problemas com a centralização, alguns deles:

- Violação de dados em sistemas centralizados expõem muitos dados.
- Autoridades centralizadas podem censurar e interromper o discurso.
- A dependência de uma "autoridade central" significa que os problemas maiores deles (upstream) afetam os problemas dos consumidores (downstream) (por exemplo: Queda na AWS significa que a maior parte da Internet cai com ela.)

Em contrapartida, a descentralização traz os benefícios opostos.

- Sem censura, pois não existe uma única autoridade ou intermediário que possa censurá-lo.
- Sem tempo de inatividade, pois a rede geral está sendo execudade em milhares de nodes pelo mundo.
- Altamente resistente a ataques, tornando inviável manipular ou destruir dados.

# Casos de uso
- Criptomoedas
- Smart Contracts (contratos inteligentes)
- Decentralized Finance (finanças descentralizadas).
- Jogos
- Supply Chain Tracking ("rastreamento da cadeia de suprimentos")
- Counterfeiting Protection (Proteção contra falsificações).
- Dados privados.
- Governos descentralizados.
- Verifiable ownership of assets ("propriedades verificável de ativos").

Para aprender mais sobre blockchains: nos fortementes sugerimos os seguintes recursos::

- [But how does bitcoin actually work? by 3Blue1Brown](https://www.youtube.com/watch?v=bBC-nXj3Ng4)
- [Blockchain Demo by Anders Brownworth
](https://andersbrownworth.com/blockchain)
- [A Gentle Introduction to Blockchain Technology by Bits On Blocks](https://bitsonblocks.net/2015/09/09/gentle-introduction-blockchain-technology/)
- [How does a blockchain work by Simply Explained](https://www.youtube.com/watch?v=SSo_EIwHSd4)
