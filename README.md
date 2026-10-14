# Flutter Object Detection

Trabalho de faculdade de 2024, retomado e encerrado em 2026. É um aplicativo Android pensado para pessoas cegas e com baixa visão: a câmera fica aberta e, com um toque na tela, o app diz em voz alta o que está à frente, com o nome do objeto, o lado em que ele está e a cor.

O reconhecimento roda no próprio aparelho, sem internet, com um modelo pronto de detecção de objetos. A cor é dada em português, pela referência mais próxima no espaço de cor CIELAB. O projeto parou numa versão de testes, sem publicação na loja.

**Tecnologias:** Flutter, Dart, TensorFlow Lite (EfficientDet-Lite0) e síntese de voz do Android.

As decisões do projeto estão em [`docs/decisions`](docs/decisions).

---

<sub>Feito por [Gustavo Victor](https://github.com/guavovic)</sub>
