# Watermark_Remover

[Readme Português](readme_ptbr.md)

[Readme English](README.md)

https://kirkdesu.github.io/Watermark_Remover/

Não sou o criador, apenas criei o repositório

I'm not the creator, I just created the repository

# Watermark Extractor

https://kirkdesu.github.io/Watermark_Remover/EXTRACTOR.html

## Uso:

Você precisará de duas amostras da marca d'água em diferentes fundos uniformes. Essas duas amostras devem vir da sua fonte de imagem; editar em um fundo diferente por conta própria não dará os resultados desejados. Uma vez que você tenha suas duas amostras, os seguintes passos são necessários:

### Carregar Imagem 1 & Carregar Imagem 2:
Carregue as respectivas amostras no extrator. A Imagem 2 será sobreposta na Imagem 1 com uma opacidade de 50%.

Se você tiver a opção "alongamento de contraste" marcada, as imagens que você vê serão editadas para melhor visibilidade de marcas d'água muito claras (ou escuras). Isso é feito esticando a faixa de cores da imagem carregada para a faixa completa entre preto e branco. Esta opção só funciona bem se você tiver cortado suas amostras para apenas as marcas d'água antes de carregá-las aqui.

### Defina as cores de fundo:
Para resultados ótimos, as cores de fundo devem ser especificadas corretamente. Com os botões "Cor de fundo da imagem #", você pode definir a cor usando o menu de escolha de cores do seu sistema. A lupa ao lado funcionará como um seletor de cores, semelhante aos programas usuais de edição de imagens. Isso significa que você só precisa clicar no ícone da lupa e, em seguida, clicar em um ponto na imagem onde a cor de fundo está claramente visível, e a ferramenta selecionará a cor que você clicou.
(Não consegui encontrar um símbolo de conta-gotas em unicode, então usei a lupa, rs.)

### Posicione as imagens para alinhar as marcas d'água:
Assim como no removedor de marca d'água, arraste e solte para mover grosseiramente e use as teclas de seta para ajustes finos. Os vários modos de mesclagem e filtros podem ajudar.

### Posicione a caixa de extração:
Provavelmente, você já notou a caixa azul até agora. Ela é usada para marcar a área de onde a marca d'água será extraída. Posicione-a arrastando e soltando (não há teclas de seta aqui) e redimensione-a usando o canto inferior direito. Se ela sair da página, isso não deve ser um problema e será cortada nos pontos mais próximos onde ambas as imagens são visíveis novamente.

### Clique em "Extrair":
A marca d'água extraída será baixada (infelizmente sem pré-visualização aqui).

## Notas adicionais:

Os arquivos de marca d'água serão compatíveis com as ferramentas do FIRE. Obrigado pela matemática por trás disso, FIRE.

# Watermark Remover

https://kirkdesu.github.io/Watermark_Remover/UNWATERMARKER.html

## USO BÁSICO:

O uso básico é primeiro carregar uma imagem (ou várias) pressionando o botão ou arrastando e soltando na janela do navegador. Em seguida, carregue a amostra da marca d'água usando o respectivo botão e posicione-a arrastando com o mouse ou usando as teclas de seta do teclado. Finalmente, pressione o botão "Remover Marca d'Água" para obter o resultado.

## MODO DE LOTE:

Se você carregar mais de uma imagem, o removedor de marcas d'água entrará no modo de lote. Ou seja, ele passará por todas as imagens carregadas uma após a outra. Dependendo se você habilitou a configuração "Modo de lote completo", isso pode acontecer de duas maneiras. Se estiver habilitado, ele passará automaticamente por todos os arquivos sem interrupção ao clicar em "remover marca d'água" na primeira imagem. Durante isso, a marca d'água será posicionada automaticamente em relação à "posição padrão da marca d'água" selecionada. Se "modo de lote completo" estiver desativado, ele ainda passará por todas as imagens selecionadas, mas de maneira semelhante à remoção de marca d'água individual. Isso significa que ele parará e dará tempo para reposicionar a marca d'água, ajustar configurações ou até mesmo carregar diferentes arquivos de marca d'água, e só avançará para o próximo arquivo quando você clicar em um dos botões "remover marca d'água" ou "pular" (onde essa imagem *não* será processada).

## DESCRIÇÃO COMPLETA:

O seguinte explica em mais detalhes o que cada botão faz. Desde a versão 1.1, alguns deles estão ocultos atrás da "Mostrar opções avançadas". (Estou com preguiça de reescrever essas descrições para refletir isso, rs.)

### "Carregar Imagem":
Carrega a imagem para remover a marca d'água. Se você selecionar vários arquivos, a ferramenta passará por todos eles um após o outro. Você também pode arrastar e soltar os arquivos na janela.

### "Carregar Marca d'Água":
Carrega o arquivo da marca d'água a ser usado. Eles são os mesmos do extrator do FIRE ou das ações do PhotoShop do tangerine.

### "Posição padrão da marca d'água":
Especifica onde a marca d'água será colocada após ser carregada, para que você não precise arrastá-la por toda a página até o canto oposto. Usá-la após a marca d'água ter sido carregada não terá efeito.

### Posicionando a Marca d'Água:
Você pode arrastar e soltar a marca d'água uma vez que ela tenha sido carregada. Para ajustes finos de posicionamento, use as teclas de seta do teclado para movê-la em 1px. No entanto, como isso ainda pode não ser ajuste fino o suficiente para algumas marcas d'água, você pode segurar a tecla CTRL enquanto usa as teclas de seta para mover em passos de 0,05px para realmente colocá-la no lugar certo. Além disso, verifique a opção de Alinhamento Automático de Subpixels.

### "Modo de mesclagem de pré-visualização":
Para ajudar no posicionamento, você pode alternar entre "normal" (a marca d'água é simplesmente sobreposta na imagem) e "diferença" (que funciona de maneira diferente e enfatiza desalinhamentos). Observe que a pré-visualização que você vê *não* representa o resultado final da remoção da marca d'água.

### "Contraste da pré-visualização":
Aumenta (ou diminui) o contraste da pré-visualização. Não afeta o resultado final. Clique no símbolo de seta giratória para redefinir.

### "Brilho da pré-visualização":
Aumenta (ou diminui) o brilho da pré-visualização. Não afeta o resultado final. Clique no símbolo de seta giratória para redefinir.

### "Limite de transparência":
Píxeis com um valor alfa menor que esse valor (= mais transparente) não serão processados. A razão é que você não pode distinguir pequenas mudanças, então elas não precisam ser processadas, acelerando um pouco a remoção da marca d'água. Além disso, a maioria deles vem da compressão JPEG, o que significa que eles não fazem parte da marca d'água em primeiro lugar.

### "Suavização opaca":
Para algumas marcas d'água muito opacas (especialmente pesadas em JPEG), pode haver artefatos feios na imagem resultante. Esta opção tenta ocultar o pior deles, medindo os píxeis especialmente opacos com o pixel anterior. A força/mistura da mediação é determinada por quanto o alfa está acima do limite. O valor padrão é alto o suficiente para não interferir com a marca d'água do bilibili, uma das mais comuns, porém muito opacas. Como tal, o valor padrão não suavizará tão fortemente, então brinque com ele se realmente precisar. 255 desativará.

### "Confirmar resultados":
Com isso, ele não descartará as imagens de origem uma vez que foram desmarcadas, mas pedirá confirmação (os botões aparecerão no lugar do botão "Remover Marca d'Água"). "Sim" confirmará as alterações, salvará o resultado e passará para a próxima imagem (se aplicável). "Não" reverterá para a imagem original, descartando quaisquer alterações. Útil se a marca d'água for difícil de posicionar.

### "Alinhamento automático de subpixels":
A ferramenta tentará ajustar o alinhamento dos subpixels por conta própria, você só precisa trazer a marca d'água a uma distância de 1px do seu ponto ideal (em outras palavras, você ainda precisa ajustar com precisão de pixel). Como tem implicações de desempenho para marcas d'água maiores (o código não é muito otimizado) e tem a possibilidade de fazer marcas d'água já perfeitamente alinhadas parecerem um pouco piores, está desativado por padrão.

### "Modo de lote completo":
Se vários arquivos de entrada forem escolhidos, passe por eles um após o outro sem parar. O posicionamento da marca d'água será determinado com base na configuração de "posição padrão da marca d'água". Inicie o processamento posicionando a marca d'água na primeira imagem e, em seguida, clicando em "remover marca d'água". Se desativado, o modo de lote semi será usado, onde você pode ajustar a posição da marca d'água para cada imagem individualmente, como de costume.

### "Salvar como ZIP no modo de lote":
Ao executar um trabalho em lote de qualquer modo (modo de lote completo ou semi), salve
