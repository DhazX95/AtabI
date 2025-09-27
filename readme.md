<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=faaff5&height=200&section=header&text=AtabI%20-%20Bookmarklet%20&fontSize=40&textColor=FFFFFF" />
</p>

### AtabI é um bookmarklet simples que permite abrir um modal na sua página com uma interface integrada que contém uma busca do Google, tudo sem sair da página atual. Ele utiliza um iframe para exibir a interface do Google, tornando a navegação mais fácil sem interromper seu fluxo.

---

## Funcionalidade

Modal Popup: Ao clicar no bookmarklet, um modal aparece sobre a página atual.

Busca Google Integrada: Dentro do modal, um iframe é carregado com a página de busca do Google.

Fechar Modal: O modal pode ser fechado clicando no botão de fechar ou clicando fora da área do modal.

Como Usar

Crie um novo bookmark no seu navegador.

Na URL, cole o seguinte código JavaScript:

```javascript
javascript:(function(){if(document.getElementById('bookmarkletModalOverlay')){document.getElementById('bookmarkletModalOverlay').style.display='flex';return;}var css='.bookmarklet-modal-overlay{display:flex;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.65);justify-content:center;align-items:center;z-index:2147483647;font-family:sans-serif}.bookmarklet-modal-container{background:#fff;border-radius:12px;box-shadow:0%208px%2024px%20rgba(0,0,0,.3);width:90%;max-width:900px;height:80%;max-height:600px;display:flex;flex-direction:column;overflow:hidden;animation:popIn%20.25s%20ease-out;position:relative}@keyframes%20popIn{from{transform:scale(.9);opacity:0}to{transform:scale(1);opacity:1}}.bookmarklet-header{background:#4285f4;color:#fff;padding:10px%2016px;font-weight:600;display:flex;justify-content:space-between;align-items:center;cursor:move;user-select:none}.bookmarklet-close-button{background:none;border:none;font-size:22px;cursor:pointer;color:#fff;font-weight:bold;transition:transform%20.2s}.bookmarklet-close-button:hover{transform:scale(1.2)}.bookmarklet-iframe-wrapper{flex-grow:1}.bookmarklet-iframe-wrapper%20iframe{width:100%;height:100%;border:none}.bookmarklet-resize{width:14px;height:14px;background:transparent;border-right:3px%20solid%20#ccc;border-bottom:3px%20solid%20#ccc;position:absolute;right:4px;bottom:4px;cursor:se-resize}';var%20style=document.createElement('style');style.textContent=css;document.head.appendChild(style);var%20modalOverlay=document.createElement('div');modalOverlay.id='bookmarkletModalOverlay';modalOverlay.className='bookmarklet-modal-overlay';var%20modalContainer=document.createElement('div');modalContainer.className='bookmarklet-modal-container';var%20header=document.createElement('div');header.className='bookmarklet-header';header.innerHTML='<span>%F0%9F%94%8E%20Google%20Search</span>';var%20closeButton=document.createElement('button');closeButton.className='bookmarklet-close-button';closeButton.innerHTML='&times;';closeButton.onclick=function(){modalOverlay.style.display='none'};header.appendChild(closeButton);var%20iframeWrapper=document.createElement('div');iframeWrapper.className='bookmarklet-iframe-wrapper';var%20iframe=document.createElement('iframe');iframe.src='https://www.google.com/search?igu=1';iframeWrapper.appendChild(iframe);var%20resizeHandle=document.createElement('div');resizeHandle.className='bookmarklet-resize';modalContainer.appendChild(header);modalContainer.appendChild(iframeWrapper);modalContainer.appendChild(resizeHandle);modalOverlay.appendChild(modalContainer);document.body.appendChild(modalOverlay);modalOverlay.addEventListener('click',function(e){if(e.target===modalOverlay)modalOverlay.style.display='none'});document.addEventListener('keydown',function(e){if(e.key==='Escape')modalOverlay.style.display='none'});var%20isDragging=false,offsetX,offsetY;header.addEventListener('mousedown',function(e){isDragging=true;offsetX=e.clientX-modalContainer.getBoundingClientRect().left;offsetY=e.clientY-modalContainer.getBoundingClientRect().top;document.body.style.userSelect='none'});document.addEventListener('mousemove',function(e){if(isDragging){modalContainer.style.position='absolute';modalContainer.style.left=(e.clientX-offsetX)+'px';modalContainer.style.top=(e.clientY-offsetY)+'px'}});document.addEventListener('mouseup',function(){isDragging=false;document.body.style.userSelect=''});var%20isResizing=false,startX,startY,startW,startH;resizeHandle.addEventListener('mousedown',function(e){isResizing=true;startX=e.clientX;startY=e.clientY;startW=modalContainer.offsetWidth;startH=modalContainer.offsetHeight;e.preventDefault()});document.addEventListener('mousemove',function(e){if(isResizing){modalContainer.style.width=(startW+(e.clientX-startX))+'px';modalContainer.style.height=(startH+(e.clientY-startY))+'px'}});document.addEventListener('mouseup',function(){isResizing=false})})();
```

Dê um nome ao bookmark, como "AtabI".

Quando estiver em qualquer página da web, basta clicar no bookmark "AtabI" para abrir o modal com a busca do Google.

## Recursos

Fechar o modal: Clicando no botão de fechar no canto superior direito ou fora do modal.

Integração com o Google: A interface dentro do iframe carrega a busca do Google, permitindo que você faça buscas diretamente no modal.

## Personalização

Você pode personalizar a URL dentro do iframe, caso queira carregar outros conteúdos, modificando a linha:

iframe.src = 'https://www.google.com/search?igu=1';

## Como Funciona o Código

O bookmarklet funciona da seguinte maneira:

CSS Dinâmico: Um estilo é criado e adicionado ao documento para estilizar o modal.

Estrutura do Modal: O código cria dinamicamente um modal com um botão de fechar e um iframe que exibe a busca do Google.

Interação com o Modal: O modal pode ser fechado clicando no botão de fechar ou clicando fora do conteúdo do modal.

Exibição em Tela Cheia: O modal ocupa a maior parte da tela, proporcionando uma experiência imersiva.

## Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=faaff5&height=150&section=footer" />
</p>
