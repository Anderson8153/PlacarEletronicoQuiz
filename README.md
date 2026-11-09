🏆 Placar Eletrônico Quiz ESP32 (v8)
Sistema interativo de Placar Eletrônico e Gamificação para Quizzes e Dinâmicas em Equipe, integrado com microcontroladores ESP32 / Arduino via WebSockets e Interface Web responsiva.

https://anderson8153.github.io/PlacarEletronicoQuiz/


📌 Visão Geral
Este projeto é uma solução completa para controle de pontuação, gerenciamento de rodadas, temporizador e acionamento físico por botões (buzzers). É ideal para eventos, gincanas, escolas, igrejas ou encontros corporativos.
O sistema opera com duas telas simultâneas (Painel do Operador e Tela da Plateia/Telão) e suporta entradas por teclado/mouse e por botões físicos conectados via ESP32.


✨ Principais Funcionalidades
⏱️ Cronômetro Interativo: Tempo ajustável com alertas sonoros e visuais nos segundos finais.
🎛️ Modo Multi-Janela / Dual-Screen: Tela exclusiva para a plateia (Telão) sincronizada em tempo real com o painel do operador.
🔌 Integração ESP32 via WebSocket: Resposta instantânea dos botões físicos das equipes sem atraso (latency-free).
🔊 Efeitos Sonoros Integrados: Sons para tempo esgotado, resposta correta, erro e acionamento dos botões (buzzers).
🎨 Personalização Dinâmica: Suporte a temas visuais (Escuro/Claro), nomes e cores personalizadas das equipes.
💾 Persistência de Dados: Estado do jogo salvo automaticamente no navegador (`localStorage`).



🛠️ Tecnologias Utilizadas
Front-end: HTML5, CSS3, JavaScript (Vanilla ES6+).
Estilização: Tailwind CSS (via CDN).
Ícones: Lucide Icons.
Comunicação em Tempo Real: WebSockets API.
Hardware Integrado (Opcional): ESP32 / ESP8266 + Arduino IDE / PlatformIO.



📂 Estrutura de Arquivos
```text
quiz-esp32/
├── index.html        # Aplicação principal (Painel do Operador + Tela da Plateia)
└── README.md         # Documentação do projeto


🚀 Como Executar o Projeto
Opção 1: Direct Link (GitHub Pages)
Se o projeto já estiver publicado no GitHub Pages, basta acessar a URL:
`https://<seu-usuario>.github.io/<seu-repositorio>/`
Opção 2: Localmente no Navegador
Baixe ou clone este repositório:

bash
   git clone https://anderson8153.github.io/PlacarEletronicoQuiz/

   
Dê um duplo clique no arquivo `index.html` para abrir diretamente no navegador (Chrome, Edge, Firefox ou Safari).


🔌 Configuração do Hardware (ESP32)
O sistema pode receber comandos diretamente de botões físicos via WebSocket rodando na porta `81` (ou configurável na interface).
Mapeamento Sugerido dos Pinos (GPIO):
Componente	Pino ESP32 (GPIO)	Função
Botão Equipe 1	`GPIO 12`	Aciona o buzzer da Equipe 1
Botão Equipe 2	`GPIO 13`	Aciona o buzzer da Equipe 2
Botão Equipe 3	`GPIO 14`	Aciona o buzzer da Equipe 3
Botão Equipe 4	`GPIO 27`	Aciona o buzzer da Equipe 4
> 💡 \*Nota:\* Utilize resistores de Pull-Up internos no código C++ (`INPUT\_PULLUP`) para conectar os botões diretamente ao GND.
Formato da Mensagem WebSocket:
O ESP32 envia dados em formato JSON simples para a aplicação Web:

json
{
  "team": 1,
  "action": "buzzer"
}



🤝 Como Contribuir
Faça um Fork deste repositório.
Crie uma branch para sua nova funcionalidade (`git checkout -b feature/nova-funcionalidade`).
Faça o Commit de suas alterações (`git commit -m 'Adiciona nova funcionalidade'`).
Envie as alterações (`git push origin feature/nova-funcionalidade`).
Abra um Pull Request.


📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
