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
javascript:(function(){ const createModal = () => { if (document.getElementById('bookmarkletModalOverlay')) { document.getElementById('bookmarkletModalOverlay').style.display = 'flex'; return; } const css = `.bookmarklet-modal-overlay { display: flex; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background-color: rgba(0, 0, 0, 0.7); justify-content: center; align-items: center; z-index: 2147483647; } .bookmarklet-modal-container { background-color: white; padding: 20px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); position: relative; width: 90%; max-width: 800px; height: 90%; max-height: 600px; display: flex; flex-direction: column; } .bookmarklet-iframe-wrapper { flex-grow: 1; } .bookmarklet-iframe-wrapper iframe { width: 100%; height: 100%; border: none; } .bookmarklet-close-button { position: absolute; top: 10px; right: 10px; background: none; border: none; font-size: 24px; cursor: pointer; color: #333; }`; const style = document.createElement('style'); style.textContent = css; document.head.appendChild(style); const modalOverlay = document.createElement('div'); modalOverlay.id = 'bookmarkletModalOverlay'; modalOverlay.className = 'bookmarklet-modal-overlay'; const modalContainer = document.createElement('div'); modalContainer.className = 'bookmarklet-modal-container'; const closeButton = document.createElement('button'); closeButton.className = 'bookmarklet-close-button'; closeButton.innerHTML = '&times;'; closeButton.onclick = () => modalOverlay.style.display = 'none'; const iframeWrapper = document.createElement('div'); iframeWrapper.className = 'bookmarklet-iframe-wrapper'; const iframe = document.createElement('iframe'); iframe.src = 'https://www.google.com/search?igu=1'; iframeWrapper.appendChild(iframe); modalContainer.appendChild(closeButton); modalContainer.appendChild(iframeWrapper); modalOverlay.appendChild(modalContainer); document.body.appendChild(modalOverlay); modalOverlay.addEventListener('click', (e) => { if (e.target === modalOverlay) { modalOverlay.style.display = 'none'; } }); }; createModal(); })();
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
