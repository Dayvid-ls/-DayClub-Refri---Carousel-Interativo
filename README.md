# DayClub Refri 🍹

Carrossel interativo de sabores de refrigerante (Morango, Abacate e Laranja). Desenvolvido com HTML, CSS e JavaScript puro, com transições suaves e animações ao trocar de item.

## Tecnologias usadas
- HTML5
- CSS3 (animações, variáveis CSS, keyframes)
- JavaScript (manipulação do DOM, eventos de clique)

## Funcionalidades
- Slider/carrossel com três sabores
- Navegação por botões "anterior" ( < ) e "próximo" ( > )
- Animação de entrada dos elementos (fruta e título) ao trocar de slide
- Fundo com cor dinâmica definida por variável CSS (`--background`)
- Layout responsivo (imagens ocupam proporções relativas)
- Esconde itens inativos com `display: none` e exibe apenas o ativo

## Como executar
1. Baixe todos os arquivos mantendo a estrutura:
2. Abra o arquivo `index.html` em qualquer navegador moderno.

## Funcionalidades em detalhe

| Elemento | Ação |
|----------|------|
| Botão `>` (next) | Avança para o próximo sabor (cíclico: após Laranja volta para Morango) |
| Botão `<` (prev) | Volta para o sabor anterior (cíclico: antes de Morango vai para Laranja) |
| Item ativo | Exibe a fruta flutuante, o título e o refrigerante correspondente |
| Animações | Ao ativar um item, a fruta e o título surgem de baixo para cima (keyframe `toActive`) |
| Cor de fundo | Cada item define sua própria cor via atributo `style="--background: #EA3D41"` (vermelho para morango, verde para abacate, laranja para laranja) |

## Animações e estilos
- **Keyframe `toActive`**: desloca o elemento de `top: 100%` (fora da tela, embaixo) para sua posição normal, com fade-in.
- A classe `.active` é aplicada a apenas um `.item` por vez.
- Imagem do refrigerante (`refri`) fica centralizada atrás da fruta (menor z-index).
- Fruta (`fruit`) posicionada com `left: 15%` e `width: 70%` para ser visualmente destacada.
- Título com fonte enorme (`12rem`) e centralizado absoluto.

## Observações
- As imagens estão referenciadas com caminho `/img/img2/...`. Certifique-se de que a pasta `img` esteja na raiz do projeto.
- O projeto é puramente visual e não possui funcionalidade de "compra" ou backend.
- O carrossel funciona de forma cíclica (ao chegar no último, volta ao primeiro).

## Possíveis melhorias futuras
- Adicionar indicadores visuais (bolinhas) para mostrar qual sabor está ativo
- Implementar navegação por teclado (setas esquerda/direita)
- Adicionar descrição nutricional ou ingredientes para cada sabor
- Tornar o slider compatível com toque (swipe) em dispositivos móveis
- Otimizar imagens para carregamento mais rápido
- Adicionar efeito de transição entre os slides (fade ou deslize)

---
