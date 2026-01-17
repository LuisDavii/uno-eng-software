# 🃏 UNO - Projeto de Engenharia de Software

Bem-vindo ao repositório do projeto **UNO**. Este projeto foi desenvolvido como parte da disciplina de Engenharia de Software, com o objetivo de aplicar conceitos de orientação a objetos, lógica de jogo e boas práticas de desenvolvimento.

##  Sobre o Projeto
Esta é uma implementação do clássico jogo de cartas **UNO** via API REST. O sistema simula uma partida completa, gerenciando o baralho, a mão dos jogadores, as regras de descarte e as ações das cartas especiais, com foco na arquitetura de software robusta.

###  Funcionalidades Principais
* **Gerenciamento de Baralho:** Criação, embaralhamento e distribuição de cartas.
* **Mecânica de Jogo:** Turnos rotativos, compras de cartas e verificação de vitória.
* **Validação de Jogadas:** Verifica rigorosamente se a carta jogada corresponde à cor ou ao número, garantindo a integridade das regras.
* **Cartas Especiais:** Implementação completa de *Pular*, *Inverter*, *+2*, *Curinga* e *+4*.
* **Monitoramento:** Acompanhamento de partidas em tempo real via sistema de observadores.

###  Arquitetura e Padrões de Projeto (Design Patterns)
Este projeto destaca-se pelo uso de padrões de engenharia para resolver problemas comuns:
* **Fachada (Facade):** A classe `CardFacade` centraliza a complexidade de manipulação e regras das cartas.
* **Strategy:** O padrão Strategy foi utilizado para isolar os efeitos das cartas especiais (como `SkipCardEffect` e `ReverseCardEffect`), facilitando a manutenção e testes.
* **Observer:** Implementado através do `MatchTracker`, permitindo que o sistema monitore e gere estatísticas das partidas ativas e finalizadas sem acoplamento direto.
* **Testes e Validação:** O código conta com validações de regras de negócio para garantir que o fluxo do jogo (turnos, compras e penalidades) ocorra sem erros.

---

##  Tecnologias Utilizadas
* **Linguagem:** Python 3.8+
* **Framework Web:** FastAPI
* **Servidor:** Uvicorn
* **Bibliotecas:** Pydantic (para modelagem de dados)
* **IDE Recomendada:** VS Code ou PyCharm

---

##  Como Executar o Projeto

### Pré-requisitos
Certifique-se de ter o **Python** instalado na sua máquina.

### Passo a passo
1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/LuisDavii/uno-eng-software.git](https://github.com/LuisDavii/uno-eng-software.git)
    ```

2.  **Acesse a pasta do projeto:**
    ```bash
    cd uno-eng-software
    ```

3.  **Instale as dependências:**
    ```bash
    pip install fastapi uvicorn
    ```

4.  **Execute o jogo (Servidor API):**
    ```bash
    python main.py
    ```
    *O servidor iniciará em `http://localhost:8000`. Você pode acessar a documentação interativa em `http://localhost:8000/docs` para testar os endpoints.*

---

##  Colaboradores
Este projeto foi desenvolvido por:

* **Luis Davi** - [Link para o GitHub](https://github.com/LuisDavii)
* **Clara Aquino** - [Link para o GitHub](https://github.com/claraaqn)

---

##  Licença
Este projeto é de uso educacional.
