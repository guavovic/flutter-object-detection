<p align="center">
  <img src="docs/assets/icone.svg" alt="" width="160">
</p>

<h1 align="center">Vera</h1>

<p align="center">
  <a href="https://github.com/guavovic/vera/releases"><img src="https://img.shields.io/github/v/release/guavovic/vera?include_prereleases&style=flat-square&label=release&color=ffff00" alt="Release"></a>
  <a href="https://github.com/guavovic/vera/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/guavovic/vera/ci.yml?branch=main&style=flat-square&label=CI" alt="CI"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/guavovic/vera?style=flat-square&label=licen%C3%A7a&color=ffff00" alt="Licença"></a>
</p>

<p align="center">Aplicativo de celular, feito para pessoas cegas e com baixa visão, que diz em voz alta o que a câmera está apontando. Você aponta, e a Vera mostra na tela e fala o que há à frente: o objeto, onde ele está e de que cor é.</p>

<p align="center">
  <b><a href="https://github.com/guavovic/vera/releases">Versões</a></b>
  &nbsp;•&nbsp;
  <a href="docs/decisions">Decisões de arquitetura</a>
</p>

## Destaques

- **Ao vivo:** a câmera analisa o que vê sem tirar foto, e um toque na tela fala o que está à frente.
- **Objeto, posição e cor:** cada objeto é dito com o nome em português, o lado em que está e a cor, como "Cadeira, à esquerda, cor azul".
- **Sem internet:** o reconhecimento roda no próprio aparelho, e nenhuma imagem sai do celular.
- **Cor em português:** nomes curtos e familiares, escolhidos pela cor mais próxima no espaço CIELAB.
- **Voz e tela juntas:** letra grande e caixas de alto contraste para quem enxerga um pouco.

## Como foi feito

Começou como um trabalho de faculdade que só dizia o nome da cor de uma foto. Hoje ele funciona ao vivo e continua em desenvolvimento.

A primeira versão era um arquivo só, com o projeto copiado em quatro pastas dentro do repositório. A Vera foi reconstruída em etapas, cada uma com a decisão registrada num ADR:

- **Câmera ao vivo**, dentro do app, que entrega os quadros para análise sem tirar foto.
- **Objetos reconhecidos no próprio aparelho**, sem internet e sem enviar imagem para fora, com os nomes em português e a posição de cada um.
- **Nomes de cor em português**, escolhidos pela referência mais próxima no espaço de cor CIELAB, que se aproxima de como a gente percebe as cores.
- **Voz e tela juntas**, com letra grande e caixas de alto contraste para quem enxerga um pouco.
- **Testes e CI** a cada mudança, com análise do código, testes e compilação do aplicativo.

## Tecnologias

- **Aplicativo:** Flutter e Dart, no Android.
- **Reconhecimento de objetos:** TensorFlow Lite, com o modelo EfficientDet-Lite0.
- **Voz:** síntese de voz do aparelho, em português do Brasil.
- **Entrega:** GitHub Actions.

---

<sub>Licença [MIT](LICENSE) · Feito por [Gustavo Victor](https://github.com/guavovic)</sub>
