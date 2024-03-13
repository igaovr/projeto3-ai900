# projeto3-ai900
## Criar um recurso de serviços de IA do Azure

Você pode usar os recursos de análise de imagem do Azure AI Vision com um recurso multisserviços de serviços de IA do Azure. Se ainda não o fez, crie um recurso de serviços de IA do Azure na sua subscrição do Azure.

Em outra guia do navegador, abra o portal do Azure em https://portal.azure.com, entrando na conta Microsoft associada à sua assinatura do Azure.
    
Clique no+Criar um recursobotão e busca porServiços de IA do Azure( , . e Selecione aCriare aServiços de IA do Azure- Plano. Você será levado a uma página para criar um recurso de serviços de IA do Azure. Configure-o com as seguintes configurações:
        Assinatura: Sua assinatura do Azure.
        Grupo de recursos: Selecione ou crie um grupo de recursos com um nome exclusivo.
        Região : Leste dos EUA.
        Nome : Digite um nome único.
        Nível de preços : Padrão S0.
        Ao marcar esta caixa, reconheço que li e entendi todos os termos abaixo: Selecionado.
    Selecione Revisão + criar, em seguida, Criar e aguardar a conclusão da implantação.

Conecte seu recurso de serviço do Azure AI ao Vision Studio

Em seguida, conecte o recurso de serviço de IA do Azure que você provisionou acima ao Vision Studio.

Em outra guia do navegador, navegue até o Vision Studio.

Entre com sua conta e certifique-se de que você está usando o mesmo diretório que aquele em que você criou seu recurso de serviços de IA do Azure.

Na página inicial do Vision Studio, selecione Ver todos os recursos no título Gettingcome com Visão.

![vision-resources](https://github.com/igaovr/projeto3-ai900/assets/147111827/596d3f8e-554d-4e45-90db-cb93fdf03144)

No modo Selecionar um recurso para trabalhar com a página, passe o cursor do mouse sobre o recurso que você criou acima na lista e, em seguida, marque a caixa à esquerda do nome do recurso e selecione Selecionar como recurso padrão.

    Nota: Se o recurso não estiver listado, talvez seja necessário atualizar a página.
<img width="400" alt="default-resource" src="https://github.com/igaovr/projeto3-ai900/assets/147111827/41e4caff-44a2-43aa-bd19-e6e728372d16">

Feche a página de configurações selecionando o “x” no canto superior direito da tela.

## Gerar legendas para uma imagem

Agora você está pronto para usar o Vision Studio para analisar imagens tiradas por uma câmera na loja Northwind Traders.

Vejamos a funcionalidade de legendas de imagem do Azure AI Vision. As legendas de imagem estão disponíveis através dos recursos Legendas de legendas e legendas de denso.

Em um navegador da web, navegue até o Vision Studio.

No início da página de destino da Visão, selecione a guia Análise de imagem e selecione o bloco Adicionar legendas a imagens.

<img width="400" alt="add-captions" src="https://github.com/igaovr/projeto3-ai900/assets/147111827/3b4bb4bd-8072-4c78-94a6-69d1c69e1afd">

Sob o subtítulo Try It Out, reconheça a política de uso de recursos lendo e marcando a caixa.

Selecione https://aka.ms/mslearn-images-for-analysis para baixar image-analysis.zip. Abra a pasta no seu computador e localize o arquivo chamado store-camera-1.jpg ; que contém a seguinte imagem:

![store-camera-1](https://github.com/igaovr/projeto3-ai900/assets/147111827/c4eb476f-63df-4707-9fe2-9bab8e76a7ae)

Carregue a imagem store-camera-1.jpg arrastando-a para a caixa Arrastar e soltar arquivos aqui, ou navegando para ela no seu sistema de arquivos.

Observe o texto de legenda gerado, visível no painel Atributos de atributos à direita da imagem.

A funcionalidade Legenda fornece uma única frase em inglês legível por humanos descrevendo o conteúdo da imagem.

Em seguida, use a mesma imagem para executar legendas Dense. Retorne à página inicial do Vision Studio e, como fez antes, selecione a guia Análise de imagem e selecione o bloco de legenda de desmantela.

O recurso Legendas Denses difere da capacidade de legenda na medida em que fornece múltiplas legendas legíveis por humanos para uma imagem, uma descrevendo o conteúdo da imagem e outras, cada uma cobrindo os objetos essenciais detectados na imagem. Cada objeto detectado inclui uma caixa delimitada, que define as coordenadas de pixel dentro da imagem associada ao objeto.

Passe o mouse sobre uma das legendas na lista de atributos detectados e observe o que acontece dentro da imagem.
<img width="400" alt="dense-captioning" src="https://github.com/igaovr/projeto3-ai900/assets/147111827/08e261bf-1645-4669-8f6c-95f7f1fd5953">

Mova o cursor do mouse sobre as outras legendas da lista e observe como a caixa delimitadora se desloca na imagem para destacar a parte da imagem usada para gerar a legenda.

## Imagens de marcação

O próximo recurso que você vai tentar é a funcionalidade Extract Tags. As etiquetas de extração são baseadas em milhares de objetos reconhecíveis, incluindo seres vivos, cenário e ações.

Retorne à página inicial do Vision Studio e selecione o extrato de tags comuns do bloco de imagens na guia Análise de imagem.

No modelo que você deseja experimentar, deixe o modelo Prebuilt do produto vs. gap selecionado. No idioma Escolha o seu idioma, selecione Inglês ou um idioma de sua preferência.

Abra a pasta contendo as imagens que você baixou e localize o arquivo chamado store-image-2.jpg, que se parece com isso:

![store-camera-2](https://github.com/igaovr/projeto3-ai900/assets/147111827/0e79f18c-83be-4d9b-b8fd-05200b8c0f0c)

Carregue o arquivo store-camera-2.jpg.

Revise a lista de tags extraídas da imagem e a pontuação de confiança para cada uma no painel de atributos detectados. Aqui, a pontuação de confiança é a probabilidade de que o texto do atributo detectado descreva o que está realmente na imagem. Observe na lista de tags que inclui não apenas objetos, mas ações, como compras, vendas e pé.

![detect-attributes](https://github.com/igaovr/projeto3-ai900/assets/147111827/706ae4ab-39ef-467f-88e5-9b2018a1c29d)

## Detecção de objetos

Nesta tarefa, você usa o recurso de detecção de objeto da análise de imagem. A detecção de objetos detecta e extrai caixas delimitadas com base em milhares de objetos e seres vivos reconhecíveis.

Retorne à página inicial do Vision Studio e selecione o bloco Detectar objetos comuns em imagens na guia Análise de imagem.

No modelo que você deseja experimentar, deixe o modelo Prebuilt do produto vs. gap selecionado.

Abra a pasta contendo as imagens que você baixou e localize o arquivo chamado store-camera-3.jpg, que se parece com isso:

![store-camera-3](https://github.com/igaovr/projeto3-ai900/assets/147111827/fc4bbb76-fb63-4819-8406-52556af76084)



Carregue o arquivo store-camera-3.jpg.

Na caixa Atribuídos, observe a lista de objetos detectados e suas pontuações de confiança.

Passe o mouse sobre os objetos na lista de atributos detectados para destacar a caixa delimitadora do objeto na imagem.

Mova o controle deslizante do valor do Limiar até que um valor de 70 seja exibido à direita do controle deslizante. Observe o que acontece com os objetos na lista. O controle deslizante de limite especifica que apenas objetos identificados com uma pontuação de confiança ou probabilidade maior do que o limite devem ser exibidos.



