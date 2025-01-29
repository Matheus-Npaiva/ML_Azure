# Machine Learning e AI em Azure
Automatização de machine learning no Azure

## Azure AI

Este projeto demonstra o uso de serviços de Inteligência Artificial (IA) da Azure para previsão de aluguel de bicicletas.

## Primeiro passo

* Criar a sua conta no microsoft Azure
Para testar os 30 dias gratuitos do Microsoft Azure, basta criar a sua conta, inserir seus dados e depois fornecer seus dados de cartão de crédito, será cobrado apenas uma pequena taxa para validar o seu cartão, após isso o valor será estornado.
   
## Dentro do Microsoft Azure
* Após acessar a sua conta já com um plano, vá para a tela inicial e procure por Azure Machine Learning.
* Procure onde está escrito 'Create' e clique em 'New workspace'.
* Dentro da criação do seu novo workspace terá várias opções a primeira delas é a 'Subscription' você não precisa alterar isso, logo em baixo terá o 'Resource group', clique em 'Create new' e crie com um nome a sua escolha.
* Logo em baixo terá a parte 'Workspace details', em 'Name' você pode colocar o nome a seu critério, na 'Region' você também pode escolher, no meu caso eu selecionei a região 'East US'
* Nas opções 'Storage account', 'Key vault' e 'Application insights' você pode selecionar o workspace já criado anteriormente.
* Após isso não precisa alterar mais nada, apenas clique no botão 'Next' na parte inferior da página até chegar na última aba que por sua vez basta clicar em 'Create' e aguarde o deploy, após o deploy clique em launch studio.
  
## Dentro do Launch Studio
* Se for sua primeira vez dentro do launch studio será necessário criar um espaço de trabalho 

<div align="center">
 <img src="https://github.com/user-attachments/assets/c1836c58-360b-4375-a705-986b9db7e682" width="700px" />
</div>
* No meu caso eu já tenho meus diretórios, basta clicar no botão em azul como mostra a imagem acima.

## Dentro do seu espaço de trabalho no Launch Studio
* Vá para a aba da esquerda e procure por computação.
* Em computação procure por cluster em computação e clique em 'Novo', após clicar em novo será aberto uma tela semalhante a essa apresentado abaixo:
<div align="center">
 <img src="https://github.com/user-attachments/assets/5ddd7cb8-9b8a-4dd0-981e-81bda0022fe6" width="700px" />
</div>
* Mantenhas as mesmas opções que eu selecionei, altere apenas as especificações de acordo com sua necessidade, vá para a próxima aba e dê um nome para sua computação e já pode finalizar esta parte.

## Conjunto de dados
Para este treinamento eu usei o conjunto de dados fornecido pela própria microsoft, que é de aluguel de bicicletas, na barra da esquerda tem a opção 'Dados' que eu recomendo fortemente que você carregue o conjunto de dados antes de criar de fato do modelo de machine learning, meu conjunto de dados pode ser encontrado em 'aka.ms/bike-rentals' após acessar esse link o conjunto de dados será baixado.

## Treinando o modelo
Na aba da esquerda terá a opção 'ML automatizado' clique nesta oçpão para fazer seu treinamento de máquina.
* Clique em Novo trabalho de ML automatizado para começar.
* Dentro da criação dê um nome do trabalho e de experimento, não precisa alterar as marcas.
* Na próxima etapa você deverá selecionar o tipo de tarefa a ser feita, no meu caso eu selecionei a 'regressão', mas ela varia de acordo com o seu problema, logo abaixo terá o seu conjunto de dados que carregamos anteriormente.
* Nas configurações de tarefas, você terá várias opções, não vou abordar detalhadamente aqui esse assunto porque isso varia muito conforme o seu problema, no meu caso eu selecionei 'Random forest' e 'LightGBM', com a métrica do erro quadrático médio padronizado.
* Na aba de computação basta apenas selecionar a computação que criamos anteriormente, criar a computação antes de fazer ML automatizado evita alguns problemas.
* Por fim basta concluir e esperar alguns minutos até que fique pronto nosso modelo de aprendizado de máquina.

## Fazendo o deploy do modelo

* Para fazer o deplou do modelo basta ir na aba da direita e procurar por 'Modelos' selecionar o seu modelo e clicar em 'Implantar' e depois em 'Serviço Web'.
<div align="center">
 <img src="https://github.com/user-attachments/assets/a72d1e91-be57-46c5-ac89-a868674d59a9" width="700px" />
</div>

* Nesta parte basta dar um nome e uma descrição a seu critério.
* Na opção 'Tipos de computação' devemos selecionar 'Instância de Contêiner do Azure' e aguardar o deploy do modelo (isso levará um tempo).
## Finalização
Por fim teremos nosso modelo implementado, para consultar nosso modelo basta ir em 'Pontos de extremidade' que fica na aba da esquerda da página. Para implementar nosso modelo em produção podemos utilizar uma API, o link será fornecido nessa aba, o arquivo .json do modelo estará disponível no meu git. Espero que isso tenha te ajudado de alguma maneira, até mais!

