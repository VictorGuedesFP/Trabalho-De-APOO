**Requisitos (RF, RNF)**

Requisitos Funcionais (RF)

1.  Cadastro e atualização de novos produtos.  
2.  Controle de produtos no estoque.  
3.  Geração de relatórios personalizados.  
4.  Alertas para produtos próximos do vencimento e produtos em baixo estoque.  
5.  Cadastrar as informações de fornecedores.  
6.  Cadastrar usuários respeitando os diferentes tipos de acesso.  
7.  Estar integrado ao sistema de vendas.

### Requisitos Não Funcionais (RNF)

1.  Interface intuitiva.  
2.  Performance rápida para transações e relatórios.  
3.  Segurança e criptografia de dados.  
4.  Alta disponibilidade (sistema disponível 24/7).  
5.  Backup e recuperação de dados.  
6.  Modularidade e facilidade de manutenção.  
7. Permitir que diversos usuários acessem o sistema simultaneamente.

**Detalhamento de requisitos**

|  Requisito 1 \- Cadastro e atualização de novos produtos. Descrição: O gerente deve adicionar as informações do carregamento de produtos ao sistema. Se todas as informações sobre os produtos estiverem devidamente corretas, o sistema deve atualizar o estoque de produtos no banco de dados, adicionando eles. |
| :---- |
| **Fonte:** O gerente |
| **Usuário:** O gerente |
| **Informações de entrada:** Nome do produto, quantidade, data de validade, fornecedor, marca, data de chegada ao local, preço de compra, preço de venda alocado, código de barras. |
| **Informações de saída:**  Validação do cadastro dos produtos. Mensagens de erro, caso ocorra. |
| **Restrições lógicas:** Caso o código de barras inserido já corresponda à algum produto dentro do estoque, o sistema deve emitir uma mensagem de erro, exigindo correções Caso a data de validade inserida seja de uma data anterior a atual do sistema, ele deve emitir uma mensagem de erro, exigindo correções |

| Requisito 2 \- Controle de produtos no estoque.  Descrição: O sistema deve realizar o processo de controle de estoque, informando ao gerente a quantidade atual de cada produto no estoque, sendo possível filtrar os resultados baseado na data de validade. Caso um produto sofra avarias, ou mesmo atinja a data de validade, o sistema deve permitir que o gerente possa selecioná-lo e removê-lo do estoque. |
| :---- |
| **Fonte:** O gerente |
| **Usuário:** O gerente |
| **Informações de entrada:** Selecionar se deseja organizar os resultados baseado na data de validade, selecionar os produtos que deseja que sejam removidos. |
| **Informações de saída:**  Validação da remoção do produto em estoque. Informar os dados dos produtos que ainda estão no estoque. |
| **Restrições lógicas:** Não há |

| Requisito 3 \- Geração de relatórios personalizados. Descrição: O sistema deve gerar relatórios personalizados, com opções para que o relatório seja da quantidade de produtos que saíram do estoque, da quantidade que foi comprada e inserida no estoque, dos que vão atingir o prazo de validade ou mesmo que já venceram, e dos produtos que estejam com baixo estoque. |
| :---- |
| **Fonte:** O gerente. |
| **Usuário:** O gerente. |
| **Informações de entrada:** Selecionar as opções de relatórios (Quantidade de produtos que entraram e saíram, quantidade de produtos prestes a atingir o prazo de validade, quantidade de produtos que estejam com baixo estoque). |
| **Informações de saída:**  Mostrar todos os produtos, com base na opção que foi selecionada. |
| **Restrições lógicas:** Não há |

| Requisito 4 \-  Alertas para produtos próximos do vencimento e produtos em baixo estoque.  Descrição: Caso o gerente não veja os relatórios ou se esqueça, o sistema deve emitir um alerta caso um estoque de produto esteja próximo da data de validade, ou que esse estoque esteja com poucos produtos. |
| :---- |
| **Fonte:** O sistema |
| **Usuário:** O gerente |
| **Informações de entrada:** Opção para selecionar quantos dias antes do prazo de validade deseja receber o alerta. Opção para selecionar quantos produtos deve restar no estoque para receber o alerta. |
| **Informações de saída:**  Uma notificação que mostre o motivo do alerta, e os lotes de produtos (dependendo da causa). |
| **Restrições lógicas:** Não há |

| Requisito 5 \- Cadastrar as informações de fornecedores.  Descrição: O gerente deve cadastrar as informações de todos os fornecedores no sistema, e atualizá-lo no banco de dados. |
| :---- |
| **Fonte:** O gerente |
| **Usuário:** O gerente |
| **Informações de entrada:** Nome do fornecedor, Número de contato, tipo de produto que fornece, localização, certificados. |
| **Informações de saída:** Validação do cadastro do fornecedor. |
| **Restrições lógicas:** Não há. |

| Requisito 6 \- Cadastrar usuários respeitando os diferentes tipos de acesso. Descrição: O gerente deve informar ao sistema algumas informações para o cadastro de funcionários. O sistema deve respeitar que um funcionário comum não possui acesso às mesmas funções que o gerente. Após a passagem das informações, o sistema deve confirmar os novos usuários no banco de dados. |
| :---- |
| **Fonte:** O gerente |
| **Usuário:** O gerente |
| **Informações de entrada:** Nome do funcionário, data de nascimento, função, login, senha. |
| **Informações de saída:**  Validação do cadastro no banco de dados. |
| **Restrições lógicas:**  Caso um funcionário tenha a mesma senha que outro, os sistema deve emitir uma mensagem de erro, exigindo alterações. |

| Requisito 7 \- Estar integrado ao sistema de vendas. Descrição: O sistema deve estar integrado ao processo de venda, sendo que cada vez que uma venda foi realizada e concluída, o sistema deve retirar a quantidade do produto do estoque. |
| :---- |
| **Fonte:** O sistema |
| **Usuário:** Não há |
| **Informações de entrada:** Vai obter as informações dos produtos que foram vendidos, através do sistema de vendas. |
| **Informações de saída:** Não há. |
| **Restrições lógicas:** Não há |

