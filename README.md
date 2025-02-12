# embarcatech_2025_u4c7_PWM
**Relatório do Projeto: Controle de Servomotor por PWM**

**1. Introdução**
Este projeto tem como objetivo a implementação do controle de um **servomotor** utilizando **modulação por largura de pulso (PWM)** no microcontrolador **RP2040**, por meio do **Pico SDK**. A atividade foi conduzida no **simulador Wokwi** e explorou a manipulação precisa do servomotor, ajustando sua posição com base em diferentes ciclos de trabalho (duty cycle). Também foi realizado um experimento com a **Ferramenta Educacional BitDogLab** para observar o comportamento de um **LED RGB** sob diferentes condições.

**2. Objetivos**
- Configurar o **PWM na GPIO 22** com frequência de **50 Hz** (período de 20 ms).
- Ajustar o ciclo de trabalho do PWM para posicionar o **servomotor** nos ângulos de **0º, 90º e 180º**.
- Implementar uma **rotina de movimentação periódica** entre os ângulos extremos.
- Garantir uma movimentação suave do servomotor, incrementando o duty cycle em **±5 µs** a cada **10 ms**.
- Realizar um experimento no **BitDogLab** para observar o impacto do PWM no LED RGB (**GPIO 12**).
- Desenvolver um **código bem estruturado e documentado** para submissão no GitHub.

**3. Materiais Utilizados**
- **Microcontrolador Raspberry Pi Pico W**
- **Servomotor (simulado no Wokwi)**
- **LED RGB (BitDogLab - GPIO 12)**
- **Ambiente de desenvolvimento VS Code com Pico SDK**

**4. Desenvolvimento e Implementação**

### **4.1 Configuração do PWM**
- Foi definida a **frequência de 50 Hz** para a GPIO 22.
- Os ciclos de trabalho foram ajustados para os seguintes tempos de **pulso ativo**:
  - **500 µs** (0º)
  - **1.470 µs** (90º)
  - **2.400 µs** (180º)
- Cada posição foi mantida por **5 segundos** antes da transição.

### **4.2 Movimentação Contínua do Servomotor**
- Foi implementada uma **rotina de varredura entre 0º e 180º**, garantindo que o deslocamento ocorresse de forma **suave**.
- A posição foi ajustada em pequenos incrementos de **±5 µs** a cada **10 ms**.

### **4.3 Experimento com o LED RGB (BitDogLab)**
- O LED RGB foi conectado à **GPIO 12** para analisar o impacto da variação do PWM em sua iluminação.
- Foram observadas mudanças na intensidade da luz conforme o ciclo de trabalho do PWM era ajustado.

**5. Resultados Obtidos**
- O **controle do servomotor via PWM** funcionou conforme esperado, permitindo a **mudança precisa de posições**.
- A **movimentação suave** do servo foi implementada com sucesso, garantindo uma transição fluida.
- A **variação do PWM** influenciou a intensidade do **LED RGB**, comprovando a relação entre ciclo de trabalho e brilho.
- O **código foi devidamente comentado e estruturado**, seguindo as boas práticas para submissão no **GitHub**.

**6. Conclusão**
O projeto permitiu uma compreensão aprofundada sobre o uso do **PWM no RP2040**, demonstrando sua aplicação tanto no **controle de servomotores** quanto na **modulação de intensidade de LEDs**. A experiência no **BitDogLab** reforçou a relação entre o ciclo de trabalho do PWM e a resposta dos dispositivos conectados. A implementação no **simulador Wokwi** permitiu validar o comportamento esperado antes da execução em hardware real. Com isso, foram consolidados conhecimentos essenciais sobre **controle de dispositivos por PWM** em sistemas embarcados.
**7. link do vídeo: 
**8. Referências**
- Documentação do **Pico SDK**
- Datasheets do **RP2040 e servomotor**
- Materiais da disciplina sobre **PWM e controle de servomotores**

