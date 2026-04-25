# Custom Splash Screen - Flutter 🚀

Este projeto foi desenvolvido por **Henrique Molinari** com o objetivo de demonstrar a criação de uma **Splash Screen não nativa** no Flutter.

Diferente da abordagem tradicional que utiliza as configurações do sistema operacional (Android/iOS), este método consiste em criar a tela de abertura como um Widget manual dentro do diretório `lib`, permitindo total liberdade criativa e controle de fluxo.

## 📌 Diferenciais desta Abordagem

* **Personalização Total:** Liberdade para usar qualquer Widget do Flutter (animações, vídeos, GIFs).
* **Lógica Interna:** Possibilidade de carregar dados de uma API ou verificar login enquanto a Splash é exibida.
* **Consistência:** Garante que a tela de abertura seja idêntica em qualquer dispositivo sem precisar configurar arquivos nativos complexos.

## 🛠️ Tecnologias e Conceitos

* **Flutter/Dart:** Framework e linguagem base.
* **POO (Programação Orientada a Objetos):** Código estruturado em classes e arquivos independentes para facilitar a manutenção e escalabilidade.
* **Navegação:** Uso do `Navigator` para gerenciar a transição fluída entre telas.

## 📂 Organização do Projeto

Seguindo as boas práticas de separação de responsabilidades e as ideias de POO, a Splash Screen possui seu arquivo próprio dentro da estrutura:

```text
lib/
├── screens/
│   └── splash_screen.dart   # Arquivo da Splash "desenhada à mão"
├── main.dart                # Ponto de entrada do App
└── home_page.dart           # Destino após o carregamento
```

## 🚀 Como Funciona a Lógica

1. **Ciclo de Vida:** O componente é construído como um `StatefulWidget`.
2. **Timer:** No método `initState()`, é definido um `Future.delayed` para controlar o tempo de exibição.
3. **Transição:** Após o tempo estipulado, o aplicativo utiliza `Navigator.pushReplacement` para navegar até a próxima tela, garantindo que o usuário não retorne para a Splash ao apertar o botão "voltar".

## 🏗️ Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/henrique-molinari/seu-repositorio.git
   ```
2. Instale as dependências:

   ```bash
   flutter pub get
   ```
3. Execute o projeto:

   ```bash
   flutter run
   ```

---

Desenvolvido por: [Henrique Molinari](https://www.linkedin.com/in/henrique-molinari).
