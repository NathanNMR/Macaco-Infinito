# 🐒 Macaco Infinito

Um teste de **velocidade e precisão de digitação em português**, inspirado no [teorema do macaco infinito](https://pt.wikipedia.org/wiki/Teorema_do_macaco_infinito).

O projeto é 100% front-end, feito com **HTML, CSS e JavaScript puro**, sem cadastro, back-end, framework ou processo de build.

## ✨ Funcionalidades

- Testes de **15, 30, 60 ou 120 segundos**
- Cálculo de **WPM (palavras por minuto)**
- Medição de **precisão**
- Feedback visual caractere por caractere
- Cursor animado na palavra atual
- Tela de resultado ao final do teste
- Reinício rápido com botão ou tecla `Tab`
- Uso de `Espaço` ou `Enter` para avançar
- Banco com **mais de 600 palavras em português**
- Layout responsivo para desktop, tablet e celular
- Suporte melhorado a teclados virtuais Android e iOS
- Sem dependências externas

## 📱 Correções para mobile

A versão anterior podia apresentar saltos de tela, perda de foco e comportamento irregular ao abrir o teclado virtual.

As principais causas eram:

- uso de `scrollIntoView()` durante a digitação, que podia rolar a página inteira;
- input invisível com `position: fixed` e `z-index: -1`;
- viewport móvel sem tratamento específico para teclado virtual;
- layout de estatísticas excessivamente vertical em telas pequenas.

A versão atual:

- mantém a rolagem somente dentro da área de palavras;
- usa uma área de entrada integrada ao painel de digitação;
- reage ao redimensionamento de `visualViewport` quando disponível;
- usa `100dvh` e `safe-area-inset-bottom` para melhor adaptação a celulares;
- mantém as estatísticas compactas em telas pequenas;
- evita que o teclado virtual desloque o conteúdo de maneira inesperada.

## 🚀 Como executar

Clone o repositório:

```bash
git clone https://github.com/NathanNMR/Macaco-Infinito.git
cd Macaco-Infinito
```

Depois, abra o arquivo `index.html` diretamente no navegador.

Também é possível iniciar um servidor local:

```bash
python -m http.server 8000
```

E acessar:

```text
http://localhost:8000
```

## 🌐 GitHub Pages

Como o arquivo principal agora se chama corretamente `index.html`, o projeto pode ser publicado diretamente pelo GitHub Pages.

1. Abra **Settings → Pages**
2. Em **Build and deployment**, escolha **Deploy from a branch**
3. Selecione a branch `main`
4. Selecione a pasta `/ (root)`
5. Salve

Após a publicação, o endereço esperado é:

```text
https://nathannmr.github.io/Macaco-Infinito/
```

## 🗂️ Estrutura

```text
Macaco-Infinito/
├── index.html
├── LICENSE
└── README.md
```

O projeto permanece propositalmente simples: toda a interface, estilos e lógica ficam em um único arquivo.

## 🛠️ Tecnologias

- HTML5
- CSS3
- JavaScript (Vanilla)
- Web APIs: `visualViewport`, eventos de teclado e input

## 🧠 Sobre o nome

O **teorema do macaco infinito** afirma, de forma simplificada, que um macaco pressionando teclas aleatoriamente por tempo infinito acabaria produzindo qualquer texto possível.

Aqui a ideia é o oposto do acaso: praticar repetidamente até digitar cada vez mais rápido e com mais precisão.

## 💡 Próximas ideias

- histórico de resultados com `localStorage`
- gráfico de evolução
- modo com frases
- dificuldade por tamanho das palavras
- temas claro/escuro
- ranking local
- suporte a outros idiomas

## 📄 Licença

Distribuído sob a licença MIT. Consulte [LICENSE](LICENSE).

---

Feito por [NathanNMR](https://github.com/NathanNMR).
